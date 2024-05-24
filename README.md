# 3DPole

10.04.2024 -> S-a adăugat un model CAD complet (dimensiunile pot diferi în viața reală, componentele pot diferi în viața reală, nu s-au făcut cablaje și/sau animații în modelul CAD)

11.04.2024 -> S-a adaugat un folder cu manuale ale componentelor, scheme electrice și/sau alte informații legale.

21.05.2024 -> S-a adăugat diagrama de cablare completă ( nu știu cum am ratat asta:3 );

23.05.2024 -> Configurația finală* a software-ului a fost publicată
- Este încă o versiune beta, testarea trebuie făcută pentru Marlin 2.1.x în sine și pentru configurația mea.

  24.05.2024 -> S-a adăugat noua documentaie în română precum și s-au făcut update-uri la documente deja existente.


3D Pole este o imprimanta 3 bazată pe Coordonate Polare construită din materiale “off-the-shelf” și/sau printate 3D.

## Proiectat de Luca Szilagyi de la Colegiul Național “Vasile Lucaciu” Baia Mare sub coordonarea dnei. profesoare Filip Adela



Toate fișierele pentru fișierele imprimabile 3D sunt furnizate în folderul 3D CAD, soft-ul este furnizat în folderul Software (configurația se afla sub irectorul Marlin, mai precis Configuration.h si Configuration_adv.h)

Acest proiect a necesitat piese imprimate 3D personalizate, precum și cabluri sertizate personalizate și firmware configurabil bazat pe Marlin.

!! Imprimanta dispune de protecție termică, dar este încă un prototip, așa că fiți conștienți de riscuri!

!! Sistemul folosește o sursă de alimentare de 24V 12,4 A. În timp ce metaluli firelor nu este expus, este totuși periculos!


# Imprimante Polare

Majoritatea oamenilor au auzit de imprimantele 3D Cartesiane, iar alții știu și despre imprimantele CoreXY.
Adevărul este că toată industria imprimării 3D s-a schimbat foarte mult în ultimii 20 de ani. Avem tipuri aparent nesfârșite de imprimante 3D.

Există imprimante carteziene normale care au crescut odată cu producția chineză de imprimante 3D după expirarea brevetului, există și imprimante CoreXY care au devenit mai populare la mijlocul anului 2020 și imprimantele Delta care au înregistrat o creștere în 2011 și încă una în 2024 odată cu lansarea. de imprimante rapide de la Flsun.

Fiecare tip de imprimantă are propriile defecte și puncte de vânzare, tipul cartezian de imprimantă este ieftină și ușor de întreținut, este, de asemenea, ușor de construit dacă doriți, dar nu este rapidă și multe probleme de calitate a vieții apar cu timpul. CoreXY sunt (cel mai adesea) mari, rapide și în general, dezavantajul lor este prețul și sistemul complex de mișcare. Imprimantele Delta sunt înalte și subțiri, la prima vedere înfricoșătoare, dar de fapt sunt mai rapide decât imprimantele carteziene (și modelele mai noi sunt chiar mai rapide decât cele CoreXY), ușor de întreținut, dar spațiul de imprimare este limitat și tind să fie destul de înalte și greu de incadrat intr-un spatiu normal.

Pe lângă aceste 3 tipuri majore de imprimante (când vorbim de mașini de tip FDM) există mașini cu 5 axe, CoreXZ, mașini de calitate industrială și preferatul meu , Imprimante Polaree.

Imprimantele Polare împrumută ceva de la toate cele 3 mari tipuri de imprimante FDM. Sunt ieftine și ușor de asamblat precum imprimantele carteziene, rapide* și fiabile ca frații lor CoreXY, ușor de extins și cu aspect înfricoșător (când vine vorba de matematică), la fel ca imprimantele Delta.

*Deși pot fi rapide, acest prototip nu este nimic din toate acestea, am ales lentă și robustă, deoarece oferă cele mai bune rezultate, cu multe reglaje, puteți transforma acest proiect într-o mașină rapidă.

Imprimantele carteziene tradiționale folosesc (după cum sugerează și numele) un sistem cartezian standard cu 3 axe, aveți valoarea X care vă spune cât de stânga sau dreapta este un punct ,valoarea Y care determină mișcarea înainte și înapoi și variabila Z care dictează înălţimea. CoreXY este oarecum același, dar X și Y sunt un sistem 2 în 1 realizat folosind o rutare ingenioasă a curelelor care mișcă capul de imprimare cu precizie cu axa Z deplasând întregul pat în sus și-n jos. Imprimantele Delta au un pat fix  nu par să aibă 3 axe diferite, au 3 axe paralele conectate la capul de imprimare cu 3 brațe, prin deplasarea celor 3 axe în diferite moduri puteți ajunge în orice punct din spațiul de imprimare, deși spațiul de imprimare nu este un cilindru, ci mai mult un con la vârf datorită acestui sistem de mișcare.

Imprimantele Polare arată ca imprimantele carteziene (numai ca aspect) cu 3 axe separate, dar un ochi atent va vedea că axa X este mai scurtă decât de obicei. Datorită unui sistem de mișcare Polară, axa X trebuie să aibă doar jumătate din dimensiunea patului, reducând astfel costurile materialelor, greutatea pe axa de imprimare și făcând o călătorie completă mai rapidă.

![imagine](https://github.com/lucagavril0307/3DPole/assets/163439407/a331d722-1aea-4a5b-ba6b-b6945ba8e72c)

Pentru a obține poziția unui punct în planul XY veți avea nevoie de un unghi și de o distanță (r și Θ), distanța ia valori de la 0 (punctul din mijloc al cercului) și raza cercului (jumătate din dimensiunea patului, deci va fi axa X) în timp ce Θ este un unghi (deci de la 0 la 360 <sau 2π în radiani>, adică rotația patului, deci axa Y). Axa Z dictează doar cât de înalt este punctul menționat.

 # Specificații și informații despre imprimantă

 După cum am explicat mai devreme, este o imprimantă Polară, cu unele caracteristici realizate folosind imprimarea 3D.
 Cum ar putea funcționa asta?
 În primele timpuri ale imprimării 3D a existat o comunitate numită RepRap care dorea să facă imprimarea 3D mai accesibilă, deoarece la acea vreme, era destinată doar industriei sau bogaților. Au proiectat imprimante care ar putea fi ieftine și suficient de bune pentru ca oricine să le facă,. La acel moment nu puteai cumpăra o imprimantă prefabricată, trebuia să o construiești singur. În această perioadă s-au făcut o mulțime de noi descoperiri care au adus imprimarea 3D la ceea ce este astăzi.
 
Comunitatea RepRap a fost o mulțime de entuziaști care au făcut ca proiectele de imprimante i să fie ușor de recreat. Deoarece nu aveau acces la echipamente industriale, majoritatea pieselor dintr-o imprimantă 3d trebuiau imprimate 3d. Ei au decis ca generația 1 de imprimante să fie făcute cu piese  imprimate 3d de la mașini industriale și următoarea generație de imprimante ar putea avea toate piesele de care au nevoie de la mașina de prima generație, așa că, cu o singură mașină puteți face alta care poate face altul și așa mai departe. Tendința a prins din urmă și chiar a ajuns în zilele noastre.
Echipa de design Voron, cunoscută pentru imprimantele lor rapide, are propriul program „Print it forward” în care (pentru o sumă de bani) cineva care are deja o imprimantă Voron va imprima piesele de care aveți nevoie (și piesele estetice dacă doriți) și mai târziu, puteți imprima aceleași piese pe aparatul dvs. pentru altcineva.

![Captură de ecran 2024-05-21 192004](https://github.com/lucagavril0307/3DPole/assets/163439407/4c9d14f6-2ab6-4091-9f7f-9b78919e5185)

Am decis să fac acest proiect în același spirit cu toate piesele printate 3D pentru această imprimantă putând fi realizate pe noua imprimantă.
Unele decizii trebuiau luate în ceea ce privește designul, nu mi-au plăcut niciodată imprimantele voluminoase (sau cele închise - chiar dacă au multe plusuri - deși am una). Axa X este inspirată de axa Ender 3 din două mari motive, pentru a fi clar că împrumută ceva de la imprimantele carteziene și pentru că, dacă nu este stricat, de ce sa il repar?

Designul este testat în timp și cred că arată bine în contrast cu întreaga imprimantă.
În ceea ce privește celelalte părți, sunt modele noi făcute de mine, pe lângă hotend-ul care este un model HERO ME și montura pentru axa X-E0 Care este un Model Ender 3.
