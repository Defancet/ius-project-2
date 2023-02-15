# IUS týmový projekt

Úvod do softwarového inženýrství týmový projekt - komplexní model informačního systému 

## Zadání (neformální specifikace)
Zadání projektu obsahuje neformální specifikaci systému. Neformální specifikaci je možno rozšířit nebo v opodstatněném případě si může student neformální specifikaci upravit. Úprava neformální specifikace nesmí vést k redukci složitost zadání!

## Vlastní řešení projektu

### Seznam jednotlivých zadání
 - Model případu užití
 - ER diagram
 - Diagram tříd
 - Sekvenční diagram
 - Diagram komunikace
 - Stavový diagram

### **Model případů užití**
První částí projektu je vypracovat model případů užití.

Diagram případů užití by měl být na jednu stranu formátu A4, měl by obsahovat více než jednoho aktéra a sadu případů užití. Případy užití volte dostatečně rozdílné, aby bylo poznat, že modelu a jeho smyslu rozumíte. V případě použití include/extend relací si dejte pozor na jejich správnou aplikaci.

Dobrou volbou případů užití dáváte najevo, že problematice rozumíte, zatímco volbou příliš podobných případů užití (např. vytvořit, změnit a zrušit objednávku) ukazujete, že si příliš jisti nejste a navíc si chcete ušetřit práci.

### **ER diagram**
Pomocí ER diagramu se modelují perzistentní data a vztahy mezi nimi. Jedná se o vyšší úroveň dat (abstrakci), která jsou v systému uložena a mohou být dále zpracovávána.

Perzistentní data v informačním systému zůstávají, i po vypnutí systému. ER diagram je základem pro návrh schématu databáze (hlaviček jednotlivých tabulek). Tvoření databázového systému si prakticky vyzkoušíte v předmětu IDS.

Při vypracovávání ER diagramu si dejte pozor, abyste opravdu modelovali data v klidu (při nepochopení ER diagramu, tj. modelování dynamické práce s daty, se může rapidně zhoršit hodnocení.

### **Diagram tříd**
Není nutné modelovat celý systém. Nicméně v modelované části musí být v souladu s ER diagramem a diagramem případů užití (viz níže).

### **Sekvenční diagram a diagram komunikace**
Modelujte sekvenci/komunikaci s minimálně 3 objekty a 5 voláními metod. Oba diagramy musí být v souladu s diagramem tříd a diagramem případu užití.

### **Stavový diagram**
Modelujte stavový diagram s alespoň 4 stavy.

### **Konzistence jednotlivých modelů**
Všechny modely musí splňovat funkcionalitu a být konzistentní, to znamená mimo jiné:
 - Názvy entitních a vztahových množin ER diagramu musí korespondovat se jmény v názvech a popisech případů užití.
 - Ke každému případu užití musí existovat vhodné entitní množiny, se kterými se manipuluje: Například pokud mám případ užití Zadat novou žádost, musím mít v ER diagramu entitní množinu, která obsahuje údaje o zadaných žádostech.
 - Naopak ke každé entitní množině by měl existovat případ užití, který přidá/mění/maže položky příslušné entitní množiny: Pokud mám například entitní množinu Uživatel, je nutnou součástí modelu případu užití možnost správy uživatelů.
 - Názvy tříd a metod v diagramu tříd, sekvenčním diagramu a diagramu komunikace musí být v souladu.
 - Ke každému případu užití musí existovat vhodná metoda v diagramu tříd, která tento UC provádí.
 - Naopak každá metoda, která předpokládá uživatelský vstup, by měla odpovídat nějakému UC.
 - Pokud je sekvence akcí iniciována nějakým případem užití, ten musí být v diagramu případu užití. Stejně tak každé volání metody musí odpovídat příslušné metodě v diagramu tříd.

## Varianta zadání: Chovná stanice

Navrhněte informační systém pro chovnou stanici psů různých plemen. U těchto plemen je nutno uchovávat informace jako průměrná výška, průměrná hmotnost, země původu, atp. Ke každému psovi na stanici (i u těch, kteří byly prodání) je nutné uchovávat údaje o plemeni, jméno, pohlaví, získaná ocenění, číslo, atp. Dále je nutné u psů evidovat kdy byla provedena různá očkování, která mají rozdílnou dobu účinnosti. Tato očkování je nutné evidovat jen po dobu pobytu psa na stanici, ne již po prodeji (to si zajistí nový majitel). Pro každého psa na stanici je nutné též pravidelně provádět měření a vážení, historie těchto údajů musí být dohledatelná s přesným datem. Systém musí být schopen na žádost klienta přes webové rozhraní vytisknout rodokmen psa se zvoleným počtem generací předků. Někteří předci psa nemusí být známi. Klient může přes webové rozhraní zadat požadavek na koupi psa (není třeba uvažovat požadavek na více psů stejného plemene zároveň). U prodaných psů je nutno evidovat, komu byli prodáni a za jakou cenu.
