# Cybersecurity – SOC / Blue Team Lab

Repozytorium dokumentuje moją praktyczną naukę cyberbezpieczeństwa w obszarze Blue Team i pracy analityka SOC L1. Każde ćwiczenie to analiza zdarzeń bezpieczeństwa w moim środowisku laboratoryjnym wraz ze zrzutami ekranu i wnioskami.

Przekwalifikowuję się z międzynarodowej spedycji (10 lat doświadczenia) i uczę się systematycznie od ponad 200 dni.

## Środowisko laboratoryjne

- Ubuntu Linux
- Wazuh (SIEM/XDR)
- Windows (źródło zdarzeń do analizy)
- Wireshark, Nmap
- Python (analiza logów)

## Zakres

- Analiza zdarzeń Windows w Wazuh (Event ID 4624, 4625, 4672, 4688, 4104, 8224)
- Korelacja zdarzeń logowania
- Analiza procesów: Command Line, Parent Process, Process Tree
- PowerShell Script Block Logging i mapowanie na MITRE ATT&CK
- Analiza ruchu sieciowego i wykrywanie skanowania portów
- Automatyzacja analizy logów w Pythonie
- Podstawy oceny bezpieczeństwa systemu Linux

## Spis ćwiczeń

| Nr | Temat | Narzędzia |
|----|-------|-----------|
| Day 1 | Analiza incydentu | Wazuh |
| Day 2 | Network Conversations – analiza rozmów sieciowych | Wireshark |
| Day 3 | Wykrywanie skanowania portów | Nmap, Wireshark |
| Day 4 | SIEM Fundamentals – laboratorium analityka SOC | Wazuh |
| Ex. 1 | Event ID 4624 – udane logowanie | Wazuh |
| Ex. 2 | Event ID 4672 – uprawnienia specjalne | Wazuh |
| Ex. 3 | Event ID 8224 – VSS | Wazuh |
| Ex. 4 | Event ID 4625 – nieudane logowanie | Wazuh |
| Ex. 5 | Korelacja zdarzeń logowania Windows | Wazuh |
| Ex. 6 | PowerShell Script Block Logging i MITRE ATT&CK (Event ID 4104) | Wazuh |
| Ex. 7 | Linux Security Assessment | Ubuntu |
| Ex. 8 | SOC Log Analyzer | Python |
| Ex. 9 | Analiza procesu w Windows – Event ID 4688 | Wazuh |
| Ex. 10 | Analiza Command Line procesu Windows | Wazuh |
| Ex. 11 | Analiza Parent Process i Process Tree | Wazuh |
| Ex. 12 | Process Chain Analysis: PowerShell → cmd.exe → whoami.exe | Wazuh |

## Jak analizuję zdarzenie

1. Co się wydarzyło (zdarzenie, źródło, czas)
2. Czy to normalne, czy podejrzane i dlaczego
3. Jak sklasyfikowałbym i spriorytetyzował alert
4. Co zrobiłbym jako analityk L1 (zamknięcie, dodatkowe dane, eskalacja do L2)

## Kontakt

Remigiusz Krzyś · remigiuszkrzys@gmail.com
