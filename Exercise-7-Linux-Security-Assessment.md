# Ćwiczenie 7 — Linux Security Assessment

## Cel ćwiczenia

Celem ćwiczenia było przeprowadzenie podstawowego audytu bezpieczeństwa systemu Ubuntu Linux działającego w środowisku laboratoryjnym.

Analiza obejmowała konta użytkowników, uprawnienia, usługi systemowe, SSH, otwarte porty, firewall, procesy uprzywilejowane, pliki SUID, logi uwierzytelniania oraz stan aktualizacji bezpieczeństwa.

Ćwiczenie miało na celu rozwijanie praktycznego podejścia do analizy systemu z perspektywy analityka SOC / Cybersecurity.

---

## Środowisko laboratoryjne

- **System:** Ubuntu 24.04 LTS
- **Host:** Ubuntu-Lab
- **Środowisko:** VirtualBox
- **SIEM:** Wazuh 4.14.7
- **IDS:** Suricata
- **Użytkownik:** remigiusz

---

## 1. Analiza użytkowników i grup

Sprawdzono aktualnie zalogowanego użytkownika oraz jego przynależność do grup systemowych.

Konto `remigiusz` posiada m.in. członkostwo w grupach:

- `sudo`
- `adm`
- `wireshark`

Członkostwo w grupie `sudo` oznacza możliwość wykonywania operacji administracyjnych z podwyższonymi uprawnieniami.

Następnie przeanalizowano lokalne konta użytkowników.

Zidentyfikowano między innymi:

- `root`
- `remigiusz`
- `postgres`
- `wazuh`
- `wazuh-indexer`
- `wazuh-dashboard`
- `mosquitto`

Większość kont usługowych posiada powłokę `nologin` lub `/bin/false`, co ogranicza możliwość bezpośredniego logowania.

Konto `postgres` posiada `/bin/bash`, dlatego zostało poddane dodatkowej analizie.

---

## 2. Analiza konta PostgreSQL

Sprawdzono status konta `postgres`.

Wynik:

`postgres L`

Litera `L` oznacza, że konto jest zablokowane.

Pomimo obecności `/bin/bash`, konto `postgres` nie jest przeznaczone do normalnego logowania przy użyciu hasła.

### Ocena

**Benign / Expected Configuration**

Sama obecność powłoki `/bin/bash` nie została uznana za podatność, ponieważ konto jest zablokowane.

---

## 3. Analiza SSH

Przeanalizowano działanie usługi SSH oraz mechanizm `ssh.socket`.

Stwierdzono, że:

- `ssh.service` nie działa jako stale aktywna usługa,
- `ssh.socket` jest aktywny,
- SSH nasłuchuje na porcie 22,
- zastosowany jest mechanizm socket activation.

Efektywna konfiguracja SSH:

```text
PermitRootLogin without-password
PubkeyAuthentication yes
PasswordAuthentication yes
