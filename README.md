
# Project-name
Description
### 1. Projekta mērķis (Analyze)
Šis projekts ir tīmekļa vietne, kas ļauj skolas administrācijai un skolēniem ērti pārvaldīt sporta zāles pieejamību, novēršot pārklāšanos un haosu rezervāciju procesos. Sistēma nodrošina caurspīdīgu grafiku un ātru pieteikšanos treniņiem vai pasākumiem, padarot sporta kompleksa izmantošanu efektīvāku.

### 2. Galvenās funkcijas (Requirements)
*Šeit uzskaitiet 5-7 svarīgākās lietas, ko jūsu lietotne vai spēle spēs darīt:*
* **Lietotāju autorizācija:** [Droša pieteikšanās sistēma skolas personālam un audzēkņiem.]
* **Interaktīvs kalendārs:** [Pārskatāms grafiks, kurā redzami visi aizņemtie un brīvie laiki reāllaikā.]
* **Rezervācijas veidne:** [Vienkārša forma "bronešānai", norādot laiku, datumu un pasākuma veidu.]
* **Administratora panelis:** [Iespēja apstiprināt, atcelt vai rediģēt lietotāju veiktās rezervācijas.]
* **Paziņojumu sistēma:** [Automātiski e-pasta vai sistēmas paziņojumi par apstiprinātu rezervāciju.]
* ~~**Resursu pārvaldība:**~~ [Izmests: Tas prasa papildu darbu ar datu vizualizāciju un sarežģītiem datubāzes pieprasījumiem.]
* ~~Analītikas modulis:~~ [Izmests: Tas sarežģī datubāzes struktūru (jāveido saraksti ar bumbām, tīkliem utt.) un rezervācijas formu.]

### V-Modeļa testa plāns (Kvalitātes kontrole)

| Funkcija | Testa darbība (Kā mēs pārbaudīsim?) | Sagaidāmais rezultāts |
| :--- | :--- | :--- |
| Lietotāju autorizācija | Ievadiet derīgu lietotājvārdu un paroli pieteikšanās formā un nospiediet pogu "Pieslēgties". | Lietotājs tiek veiksmīgi autentificēts un novirzīts uz sistēmas sākumlapu. |
| Interaktīvs kalendārs | Atveriet kalendāra sadaļu un pārbaudiet, vai tajā ir redzamas jau eksistējošas rezervācijas. | Kalendārs ielādējas veiksmīgi, skaidri parādot aizņemtos un brīvos laikus. |
| Rezervācijas veidne | Aizpildiet rezervācijas formu ar derīgiem datiem (datums, laiks, pasākums) un nospiediet "Rezervēt". | Dati tiek saglabāti sistēmā un rezervācija parādās kā gaidoša (neapstiprināta). |
| Administratora panelis | Pieslēdzieties kā administrators, atveriet rezervāciju sarakstu un nospiediet "Apstiprināt" vai "Atcelt". | Sistēma nomaina un saglabā izvēlētās rezervācijas statusu. |
| Paziņojumu sistēma | Pārbaudiet lietotāja e-pastu/profilu pēc tam, kad administrators ir apstiprinājis iepriekš izveidoto rezervāciju. | Lietotājs automātiski saņem paziņojumu par apstiprinātu rezervāciju. |

### Spirāles modeļa risku analīze
Šajā posmā mēs identificējam iespējamos projektus apdraudējumus un sagatavojam rīcības plānu to novēršanai saistībā ar sporta zāles rezervācijas sistēmu.

* **1. Tehniskais risks:** Rezervāciju konflikti jeb dubultā rezervācija (piemēram, divi lietotāji vienlaicīgi mēģina pieteikties uz vienu un to pašu brīvo laiku).
* **Risinājums:** Ieviest datubāzes līmeņa transakciju kontroli (bloķēšanu) un reāllaika kalendāra atjaunināšanu. Brīdī, kad viens lietotājs uzsāk rezervācijas procesu, sistēmai šis laiks īslaicīgi jāpadara nepieejams citiem.
* **2. Drošības risks:** Nepilnīga lietotāju lomu nošķiršana (piemēram, skolēns netīšām iegūst piekļuvi administratora panelim un var atcelt citu rezervācijas).
* **Risinājums:** Stingri definēt lietotāju lomas (audzēknis, personāls, administrators) un ieviest obligātas sesijas/piekļuves tiesību pārbaudes servera pusē pirms jebkuras darbības, kas saistīta ar rezervāciju rediģēšanu vai apstiprināšanu.
  
### 3. Izmantotie rīki un metodes
* **Plānošanas rīks:** Trello
* **Versiju kontrole:** GitHub
* **Izstrādes metode:** [Agile], jo [tā ļauj mums elastīgi pielāgoties izmaiņām izstrādes procesā un pakāpeniski uzlabot funkcijas balstoties uz testēšanas rezultātiem.].

### 4. Komandas lomas
* **Product Owner:** [Sofija, Lucenko] — atbild par ideju.
* **Scrum Master / Vadītājs:** [Antons, Morozovs] — atbild par procesu un laiku.
* **Izstrādātāji:** [Daniels Mēters] — atbild par saturu un tehnisko izpildi.

### 5. Darba gaita (Progress)
* [x] Izdomāta ideja
* [x] Izveidots plāns Trello dēlī
* [x] Dokumentācija pabeigta
* [ ] Gatavs prezentācijai
