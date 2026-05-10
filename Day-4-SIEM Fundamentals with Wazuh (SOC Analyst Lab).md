Overview

Today I completed my first practical SIEM lab using Wazuh on Ubuntu Linux.
The goal of this lesson was to understand how Security Information and Event Management (SIEM) systems work in real SOC (Security Operations Center) environments.

Instead of only learning theory, I generated real system events, analyzed security logs, and observed how alerts are created and classified.

Technologies Used
Ubuntu Linux
Wazuh SIEM
Linux system logs
SSH authentication logs
PAM authentication events
sudo events
Terminal / Bash
What I Learned
What SIEM Is

I learned that SIEM (Security Information and Event Management) systems:

collect logs,
analyze events,
detect suspicious activity,
generate alerts,
help SOC analysts investigate incidents.

I also learned the difference between:

Term	Meaning
Event	Single activity (login, sudo, SSH)
Alert	Suspicious pattern detected
Incident	Real security threat requiring response
Wazuh Installation and Configuration

I installed and configured Wazuh SIEM on Ubuntu Linux.

During setup I:

installed the Wazuh manager,
configured the dashboard,
accessed the web interface,
explored security monitoring modules.
Security Events Analysis

Inside the Wazuh dashboard I analyzed:

authentication failures,
successful logins,
sudo usage,
PAM events,
brute force indicators.

I learned how SIEM platforms classify alerts by severity levels.

Examples:

Level 3 → informational
Level 5 → suspicious activity
Level 10 → high severity alert
Practical Security Simulations
Failed SSH Login Attempts

I generated failed SSH authentication attempts and analyzed them in Wazuh.

Detected events included:

Failed password
Authentication failure
Password guessing
Brute force
Privilege Escalation Detection

I simulated sudo usage and privilege escalation activity.

Wazuh generated alerts such as:

Successful sudo to ROOT executed
Three failed attempts to run sudo

This demonstrated how SIEM systems detect suspicious privilege escalation behavior.

Key Takeaways
SIEM platforms are critical in modern SOC environments.
Log analysis is one of the most important junior cybersecurity skills.
Security monitoring requires understanding context, not only reading alerts.
Not every alert is an incident.
Wazuh can detect brute force activity, failed logins, and suspicious sudo behavior automatically.
Skills Practiced
SIEM fundamentals
Log analysis
Linux security monitoring
SSH authentication analysis
Brute force detection
Privilege escalation monitoring
Event correlation
SOC workflow basics
Alert investigation
Real-World Relevance

This lab reflects real entry-level SOC analyst responsibilities:

monitoring alerts,
analyzing logs,
identifying suspicious activity,
validating incidents,
understanding severity levels.

It was one of the most practical cybersecurity lessons I have completed so far.

------------------------------------------------------------------------

Dzisiaj ukończyłem swoje pierwsze praktyczne ćwiczenie z zakresu SIEM, korzystając z systemu Wazuh w środowisku Ubuntu Linux.
Celem tej lekcji było zrozumienie, jak systemy zarządzania informacjami i zdarzeniami bezpieczeństwa (SIEM) działają w rzeczywistych środowiskach SOC (Security Operations Center).

Zamiast ograniczać się wyłącznie do teorii, wygenerowałem rzeczywiste zdarzenia systemowe, przeanalizowałem logi bezpieczeństwa oraz obserwowałem, w jaki sposób tworzone i klasyfikowane są alerty.


Dowiedziałem się również, jaka jest różnica między:

Termin    Znaczenie
Zdarzenie    Pojedyncze działanie (logowanie, sudo, SSH)
Alert    Wykryto podejrzany wzorzec
Incydent    Rzeczywiste zagrożenie bezpieczeństwa wymagające reakcji
Instalacja i konfiguracja Wazuh

Zainstalowałem i skonfigurowałem system SIEM Wazuh w systemie Ubuntu Linux.

Podczas konfiguracji:

zainstalowałem menedżera Wazuh,
skonfigurowałem pulpit nawigacyjny,
uzyskałem dostęp do interfejsu internetowego,


Analiza zdarzeń związanych z bezpieczeństwem

W panelu Wazuh przeanalizowałem:

nieudane próby uwierzytelnienia,
udane logowania,
użycie polecenia sudo,
zdarzenia PAM,
wskaźniki ataków typu brute force.

Dowiedziałem się, w jaki sposób platformy SIEM klasyfikują alerty według poziomów ważności.

Przykłady:

Poziom 3 → informacyjny
Poziom 5 → podejrzana aktywność
Poziom 10 → alert o wysokim poziomie ważności


Praktyczne symulacje bezpieczeństwa
Nieudane próby logowania przez SSH

Wygenerowałem nieudane próby uwierzytelnienia przez SSH i przeanalizowałem je w systemie Wazuh.

Wykryte zdarzenia obejmowały:

Błędne hasło
Błąd uwierzytelnienia
Próby odgadnięcia hasła
Atak brute force

Wykrywanie eskalacji uprawnień

Przeprowadziłem symulację użycia polecenia sudo oraz działań związanych z eskalacją uprawnień.

System Wazuh wygenerował następujące alerty:

Pomyślne wykonanie polecenia sudo z uprawnieniami ROOT
Trzy nieudane próby uruchomienia polecenia sudo

Pokazało to, w jaki sposób systemy SIEM wykrywają podejrzane zachowania związane z eskalacją uprawnień.

Najważniejsze wnioski
Platformy SIEM mają kluczowe znaczenie we współczesnych środowiskach SOC.
Analiza logów to jedna z najważniejszych umiejętności dla początkujących specjalistów ds. cyberbezpieczeństwa.
Monitorowanie bezpieczeństwa wymaga zrozumienia kontekstu, a nie tylko odczytywania alertów.
Nie każdy alert oznacza incydent.

Nabyte umiejętności
Podstawy SIEM
Analiza logów
Monitorowanie bezpieczeństwa systemu Linux
Analiza uwierzytelniania SSH
Wykrywanie ataków metodą brute force
Monitorowanie eskalacji uprawnień
Korelacja zdarzeń
Podstawy organizacji 

Związek z praktyką
To ćwiczenie odzwierciedla rzeczywiste obowiązki początkującego analityka SOC:
monitorowanie alertów,
analizowanie logów,
wykrywanie podejrzanej aktywności,
weryfikacja incydentów,
rozumienie poziomów ważności.

Była to jedna z najbardziej praktycznych lekcji dotyczących cyberbezpieczeństwa, w jakich dotychczas uczestniczyłem.
Podstawy pracy w SOC
Badanie alertów
zapoznałem się z modułami monitorowania bezpieczeństwa.
Analiza zdarzeń bezpieczeństwa
