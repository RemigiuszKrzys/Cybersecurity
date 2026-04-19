# 🔍 Day 1 — Mini Incident Analysis (Linux logs + Nmap)

## 🎯 Objective

The goal of this exercise was to analyze system logs and determine whether there are signs of a brute force attack.

---

## 💻 Step 1 — Log Analysis

Command used:

```bash
grep -Ei "failed|failure|invalid|FAILED SU" /var/log/auth.log
```

### Result:

No output was returned.

### Interpretation:

* No failed login attempts detected
* No signs of brute force activity in authentication logs

---

## 🌐 Step 2 — Port Analysis

Command used:

```bash
sudo nmap localhost
```

### Result:

```
631/tcp open ipp
```

### Interpretation:

* Port 22 (SSH) is NOT open
* Only port 631 (printing service - IPP) is open
* No remote login service available

---

## 🧠 Analysis

To identify a brute force attack, we look for:

* Multiple failed login attempts
* Repeated IP addresses
* Attempts in a short time window
* Targeting the same user

### Findings:

* No failed login attempts found
* No suspicious IP addresses
* No repeated patterns
* No exposed SSH service

---

## ✅ Conclusion

There is no evidence of a brute force attack on this system.

---

## 🧠 Key Takeaways

* Absence of evidence is still a result
* Log analysis requires pattern recognition, not single entries
* Open ports define attack surface
* No SSH = no brute force via SSH

---

## 🚀 What I learned

This exercise helped me understand how to:

* Analyze authentication logs
* Identify attack patterns
* Use Nmap for local enumeration
* Think like a SOC analyst

PL Tłumaczenie:

🔍 Dzień 1— Mini analiza incydentu (logi systemu Linux + Nmap)

## 🎯 Cel

Celem tego ćwiczenia była analiza logów systemowych i ustalenie, czy występują oznaki ataku typu brute force.

---

## 💻 Krok 1 — Analiza logów

Użyte polecenie:

```bash
grep -Ei „failed|failure|invalid|FAILED SU” /var/log/auth.log
```

### Wynik:

Nie zwrócono żadnego wyniku.

### Interpretacja:

* Nie wykryto żadnych nieudanych prób logowania
* Brak oznak ataku typu brute force w logach uwierzytelniania

---

## 🌐 Krok 2 — Analiza portów

Użyte polecenie:

```bash
sudo nmap localhost
```

### Wynik:

```
631/tcp open ipp
```

### Interpretacja:

* Port 22 (SSH) NIE jest otwarty
* Otwarty jest tylko port 631 (usługa drukowania — IPP)
* Brak dostępnej usługi zdalnego logowania

---

## 🧠 Analiza

Aby zidentyfikować atak typu brute force, szukamy:

* Wielokrotnych nieudanych prób logowania
* Powtarzających się adresów IP
* Próby w krótkim przedziale czasowym
* Ataki skierowane na tego samego użytkownika

### Ustalenia:

* Nie znaleziono nieudanych prób logowania
* Brak podejrzanych adresów IP
* Brak powtarzających się wzorców
* Brak ujawnionej usługi SSH

---

## ✅ Wniosek

Nie ma dowodów na atak typu brute force na ten system.

---

## 🧠 Kluczowe wnioski

* Brak dowodów to wciąż wynik
* Analiza logów wymaga rozpoznawania wzorców, a nie pojedynczych wpisów
* Otwarte porty definiują powierzchnię ataku
* Brak SSH = brak ataku brute force przez SSH

---

## 🚀 Czego się nauczyłem

To ćwiczenie pomogło mi zrozumieć, jak:

* Analizować logi uwierzytelniania
* Rozpoznawać wzorce ataków
* Używać Nmap do lokalnej enumeracji
* Myśl jak analityk SOC

