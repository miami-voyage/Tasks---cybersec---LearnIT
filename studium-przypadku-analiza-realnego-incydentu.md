1. Nazwa incydentu
*  Incydenty bezpieczeństwa w LastPass (Incydent 1 i Incydent 2).
* "Incident 1 Summary", "Incident 2 Summary"

2. Organizacja i rok
* LastPass, 2022 rok.
* "To Our LastPass Customers", "December 22, 2022"

3. Profil atakującego
*  Brak dokładnych danych / Inny.
* "To date, however, the identity of the threat actor and their motivation remains unknown."

4. Wektor wejścia
* Kompromitacja stacji roboczej pracownika (w Incydencie 1) oraz wykorzystanie podatności w oprogramowaniu firm trzecich (w Incydencie 2).
* Incydent 1: "A software engineer’s corporate laptop was compromised..."
* Incydent 2: "The threat actor targeted a senior DevOps engineer by exploiting vulnerable third-party software."

5. Cel działania
* Kradzież danych własnych firmy (kod źródłowy, sekrety systemowe) oraz kradzież danych klientów (backupy, metadane, zaszyfrowane sejfy z hasłami). Motywacja ostateczna jest nieznana.
* Sekcja WHAT DATA WAS ACCESSED (n"threat actor stole both LastPass proprietary data and customer data"). Brak informacji o żądaniach okupu: - There has been no contact or demands made..."

6. Naruszone elementy CIA (Poufność, Integralność, Dostępność)
* Poufność: Tak, została naruszona na dużą skalę (wyciek danych).
* Integralność: Brak danych (nie wspomniano o modyfikacji danych czy kodów źródłowych w systemach produkcyjnych, jedynie o wdrożeniu złośliwego oprogramowania na urządzeniu pracownika).
* Dostępność: Brak danych (nie wspomniano o przestojach w działaniu usługi dla klientów z powodu ataku).
* Neither incident was caused by any LastPass product defect or unauthorized access to – or abuse of – production systems."

7. Cyber Kill Chain

Reconnaissance - Atakujący wykorzystał dane zebrane w pierwszym incydencie do zidentyfikowania celów do drugiego incydentu. - "...information stolen in the first incident was used to identify targets and initiate the second incident."

Weaponization - brak danych. 

Delivery - Napastnik dostarczył złośliwe oprogramowanie na stację DevOps inżyniera. - "The threat actor leveraged the vulnerability to deliver malware..." (Incydent 2).

Exploitation - Wykorzystanie podatności w oprogramowaniu firm trzecich (third-party software). - "...exploiting vulnerable third-party software." (Incydent 2)

Installation - Instalacja malware na urządzeniu pracownika i obejście istniejących zabezpieczeń. - "...deliver malware, bypass existing controls..."

Command & Control - brak danych. 

Actions on Objectives - Uzyskanie dostępu do środowisk programistycznych i backupów chmurowych, po czym wykradzenie kodu źródłowego, sekretów, metadanych i sejfów klientów. - "...ultimately gain unauthorized access to cloud backups. The data accessed from those backups included..."

8. Co poszło nie tak po stronie obrońców?
* Nie zidentyfikowano pełnego wpływu pierwszego incydentu, co pozwoliło atakującym wykorzystać skradzione dane do przeprowadzenia drugiego, poważniejszego ataku. Zawiodły też zabezpieczenia na stacjach roboczych pracowników (podatne oprogramowanie third-party) oraz kontrole dostępu, które napastnik zdołał ominąć.
* We declared this incident closed but later learned that information stolen in the first incident was used to identify targets and initiate the second incident."

9. Gdzie można było przerwać incydent?
* Na etapie początkowym: poprzez odpowiednie zabezpieczenie laptopa inżyniera (Incydent 1) i aktualizację podatnego oprogramowania firm trzecich.
Pomiędzy incydentami: poprzez natychmiastową rotację wszystkich poświadczeń/sekretów, z którymi powiązane były dane skradzione w pierwszym ataku, zanim zostały one użyte do Incydentu 2.

10. Trzy rekomendacje bezpieczeństwa

    1. Rotacja poświadczeń i certyfikatów: 
    2. Wzmocnienie kontroli dostępu uprzywilejowanego (Privileged Access): 
    3. Dodanie nowych polityk, narzędzi bezpieczeństwa oraz szerszego szyfrowania (zarówno w aplikacji, jak i infrastrukturze backupowej).
    "Rotated relevant secrets and certificates", "Analyzed and changed existing privileged access controls", "expand the use of encryption within our application and backup infrastructure"
