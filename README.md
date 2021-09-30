# BE-Developer

<details>
  <summary>Java deeper</summary>

## Java deeper

<details>
  <summary>Collections</summary>
  
  
  ### Collections
  Java 8 bola prelomová verzia čo sa týka Java programovacieho jazyka a je stále jednou z najviac využívanou verziou (https://www.jetbrains.com/lp/devecosystem-2020/java/?gclid=CjwKCAjw_Y_8BRBiEiwA5MCBJj758JPI8Zc8kRXmyvdADOdzc6OEchjC2TDEojL3Eul_pG2yjGl9hRoCaJ0QAvD_BwE&gclsrc=aw.ds ). 
  
  O lambdách, method referenciách ale aj iných možnostiach, ktoré priniesla Java 8 si môžeš prečítať viac napríklad tu https://www.tutorialspoint.com/java8/java8_overview.htm (klikni si tam napr. na Streams a nájdeš aj príklady použitia jednotlivých metód).
  
  Skús pri riešení nasledujúcich úloh namiesto klasických cyklov použiť Stream API.
  1.	Vytvor ArrayList, ktorý bude obsahovať elementy 1, 1, 1, 2, 2, 3, 4, 5 a vytvor metódu, ktorá vypíše tieto hodnoty alebo vypíše “List je prázdny“ ak je list prázdny. Skús na to použiť forEach metódu kde sa zoznámiš s lambda expression.<br><br>
  Prepíš lambda funkciu na Method Reference.<br><br>

2.	Vytvor metódu addIfNotExists, ktorá vloží nový element do listu ak taký element ešte neexistuje (tu nepoužívaj stream) // contains, add
3.	Vytvor metódu, kt. vymaže z listu všetky párne čísla  (tu nie je nutné použiť stream, no dá sa) //removeIf
4.	Vytvor metódu, ktorá vráti list párnych čísel z listu z cvičenia 1 // filter
5.	Prepíš cvičenie 4 z časti Java typy, podmienky, cykly. Namiesto poľa použi ArrayList a pre výpočet použi Stream API // map
6.	Vráť sa do cvičenia číslo 13 (suma budgetov) z časti Java triedy, objekty a prepíš výpočet celkovej sumy pomocou Stream API // mapToInt, sum
7.	V cvičení číslo 13 (suma budgetov) z časti Java triedy, objekty dopíš novú metódu, ktorá vráti true, ak list osôb (John, Steve, Martin) obsahuje osobu s menom, v ktorom sa nachádza písmeno "a" //anyMatch

Doplňujúce otázky na zamyslenie a pre lepšie porozumenie:

Aký je rozdiel medzi obyčajným poľom (napr. String []) a ArrayListom?

Prečo má niekedy zmysel pri inicializácii ArrayListu písať počiatočnú kapacitu? new ArrayList<>(10)?

8.	Vytvor nový HashSet z listu z cvičenia 1 a vypíš hodnoty. Skús do tohto setu vložiť číslo 1. Vidíš rozdiel medzi Listom a Setom?
9.	Vytvor nový objekt typu HashMap kde kľúč bude typu String a hodnota bude typu Integer. Vlož do mapy hodnoty:<br>
a.	"Red", 1<br>
b.	"Green", 2<br>
c.	"Black", 3<br>
d.	"White", 4

Vypíš všetky kľúče a všetky hodnoty.

10.	Vytvor metódu s dvoma parametrami (kľúč, hodnota), ktorá vloží nový element do mapy len vtedy, ak element s daným kľúčom ešte neexistuje // putIfAbsent


  </details>
  
  <details>
  <summary>Inheritance</summary>
  <br>
  
  **Užitočné linky:**
  <br>Abstract class: https://www.javatpoint.com/abstract-class-in-java 
  <br>Interface: https://www.javatpoint.com/interface-in-java 
  <br>Prečo používať interface: https://stackoverflow.com/questions/240152/why-would-i-want-to-use-interfaces 
  <br>Rozdiely medzi Abstract class a Interface: https://www.javatpoint.com/difference-between-abstract-class-and-interface 
  <br>...alebo iné
  
  1.  Vytvor triedy Programmer a Teacher každú s atribútmi salary (float) a bonus (int). Pridaj konštruktor s týmito dvomi parametrami. Ďalej pre každú z tried pridaj metódu getInfo(), ktorá vypíše _"Programmer’s salary is " + salary + " and bonus is " + bonus._ pre triedu Programmer a _"Teacher’s salary is " + salary + " and bonus is " + bonus._ pre triedu Teacher. V main metóde vytvor inštancie oboch tried(hodnoty atribútov si zvoľ ľubovoľne) a vypíš volanie metódy getInfo() do konzoly.
  
  Čo keby si teraz chcel pridať nové zamestnanie, napr. Driver, s rovnakými atribútmi a getInfo() metódou?
  
  2.  Skús použiť dedičnosť tak, aby si čo možno najviac zredukoval duplicitu kódu a uľahčil pridanie zamestnania Driver alebo akéhokoľvek ďalšieho zamestnania. Pre typy zamestnaní skús použiť Enum.<br>
  Očakávaný výpis v konzole:<br>
_Programmer's salary is 1700.0 and bonus is 200._<br>
_Teacher's salary is 900.0 and bonus is 300._

3.  Pridaj teraz nové zamestnanie Driver. Vytvor inštanciu triedy Driver a vypíš do konzoly informácie o tomto zamestnancovi.
Uprav main metódu (ak to tak ešte nemáš) tak, že v nej budeš mať list zamestancov a pre výpis použi lambdu.

4.  Teraz si predstav, že pre programátora nechceme vypisovať informácie o plate a bonuse zvlášť ale všetko spolu, no pre všetky ďalšie zamestnania chceme výpis ponechať nezmenený. Uprav metódu getInfo() len pre triedu Programmer tak, aby vypisovala _"Programmer's salary is " + (súčet hodnôt salary a bonus)._ <br>
Očakávaný výpis v konzole:<br>
_Programmer's salary is 1900.0_<br>
_Teacher's salary is 900.0 and bonus is 100._<br>
_Driver's salary is 1000.0 and bonus is 300._

Vytvor nový package s názvom model a presuň tam všetky triedy okrem triedy Main.

5.  V package-i kde sa nachádza trieda Main vytvor teraz interface s názvom EmployeeService, ktorý bude obsahovať 2 metódy – 1 pre výpočet celkovej sumy hodnôt atribútov salary pre zoznam zamestnancov a 1 pre výpočet celkovej sumy bonusov. Vytvor EmployeeServiceImpl, ktorá bude implementovať EmployeeService interface. Vytvor inštanciu tejto service triedy v main metóde a vypíš do konzoly výsledky metód.

  </details>
  
</details>

---

<details>
  <summary>Spring Boot</summary>
  
  ## Spring Boot
  
  <details>
    <summary>Getting started</summary>
  
  ### Getting started
  
  Nasledujúce cvičenia v sekcii Spring Boot ti pomôžu získať aký taký obraz o Spring Boot-e.
  
  Tu si môžeš prečítať niečo o Spring Boot-e, napríklad na https://www.tutorialspoint.com/spring_boot/spring_boot_introduction.htm .
  Niekedy sa ti bude hodiť aj Spring Boot documentácia: https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/
  
  Choď na https://start.spring.io/ .
  
  Spring Initializr je nástroj, ktorý ti pomôže vytvoriť tvoju Spring Boot aplikáciu jednoducho a rýchlo. Nastav si všetko tak ako je to znázornené na obrázku.
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/initializr.png>
  
  V sekcii Project sa volí tzv. build automation tool. Je to nástroj, ktorý ti pomôže „postaviť tvoj projekt na nohy“. Vďaka nemu tiež budeš môcť spravovať všetky dependencies (závislosti; knižnice, ktoré budeš chcieť použiť), ktoré bude tvoja aplikácia potrebovať k svojmu fungovaniu. My budeme používať Maven (môžeš si ho stiahnuť). Ak chceš vedieť o Maven-e viac kľudne si vygoogli, na internete nájdeš všetko.
  
Klikni na GENERATE a stiahnutý zip súbor si niekam rozbaľ. Teraz môžeš otvoriť svoju vygenerovanú aplikáciu v Intellij. Mal by si vidieť niečo takéto:

<img src=https://github.com/AppsLab-2/materials/blob/master/springBootApp.png>

Skús si tam kľudne dopísať výpis napríklad “Hello Spring Boot”. Keď teraz spustíš svoju aplikáciu, v Intellij konzole by si mal vidieť výpis (logy) ako spustenie appky prebiehalo aj spolu s tvojim výpisom. Tak a tvoja prvá Spring Boot appka je hotová.
</details>

  <details>
  <summary>Dependency Injection</summary>
  
  ### Dependency Injection
  
  Dependency injection je základný aspekt Spring frameworku. Spring vlastne spravuje objekty v tvojej appke a počas behu aplikácie ich posúva kde treba. V nasledujúcej časti si to skúsime vysvetliť, no určite sa tomu povenuj aj ja sám, na internete nájdeš všetko čo potrebuješ. Môžeš pozrieť napríklad sem https://www.baeldung.com/spring-dependency-injection .
  
Na začiatok pozri tiež: https://www.baeldung.com/spring-bean a https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html#beans-introduction . Čo je teda Bean?

Kľudne si pozri aj nejaké video na youtube. Prípadne si urob aj sám nejaký tutorial na nete aby si to pochopil.

Prekopíruj si celý model package aj spolu s tvojou service-ou z cvičení o dedičnosti do svojej Spring Boot appky. Vytvor novú triedu DependencyInjectionDemo, ktorá bude mať jeden atribút typu EmployeeService a bude mať jednu metódu getSum(), ktorá bude vracať súčet výsledkov oboch metód z EmployeeService. V konštruktore vypíš do konzoly volanie metódy getSum. V main metóde len vytvor inštanciu triedy. Keď spustíš  appku mal by si vidieť výpis. Takto nejako by to mohlo vyzerať v tvojej main metóde:

<img src=https://github.com/AppsLab-2/materials/blob/master/mainMethod.png>

Zatiaľ je to úplne bežný program aký sme písali aj doteraz a nevyužívame nič navyše.

**Teraz povieme Spring-u aby vytvoril inštancie on. On si ich uloží do IoC kontajnera a ten ich bude injectovať podľa potreby.**

Vymaž vytváranie inštancie triedy DependencyInjectionDemo  v metóde main nechaj len ten jeden riadok, ktorý štartuje Spring Boot appku. Spusti teraz svoju aplikáciu. Samozrejme nevidíš žiadny výpis lebo sa konštruktor nikde nezavolal.

Pridaj teraz anotácie @Component nad triedu DependencyInjectionDemo  a anotáciu @Service nad triedu EmployeeServiceImpl. Skús spustiť aplikáciu, mal by si vidieť výpis. Prečo? Pogoogli si ak potrebuješ. Len aby sme si ukázali ako to funguje, pridaj do EmployeeServiceImpl atribút number a nastav ho rovno na číslo 0. Pridaj tiež novú metódu _writeNumber()_, ktorá zvýši hodnotu atribútu number a vypíše ju do konzoly. V konštruktore DependencyInjectionDemo pridaj výpis metódy _writeNumber()_. Teraz skús pridať nejakú druhú triedu, ktorá tiež bude mať atribút typu EmployeeService. V konštruktore tejto triedy tiež zavolaj _writeNumber()_. Spusti aplikáciu. Všimni si, že ti vypísalo číslo 1 a 2, pretože v oboch prípadoch bola použitá (nainjectovaná) tá istá EmployeeService.
  </details>
  
  <details>
  <summary>Spring Web</summary>
  
  ### Spring Web
  
  Keďže ideme robiť web development budeme potrebujeme pridať do našej aplikácie Spring Web. Pridaj si teda do pom.xml (ak nevieš čo to je za súbor tak si vygoogli 😊 ) dependency na spring-boot-starter-web. Keď ti maven resolvne dependecy a pustíš svoju appku uvidíš, že sa toho spúšťa už o niečo viac. Napríklad vidíš, že Spring Boot spustil tiež embedded Tomcat (web server) s portom 8080. Kým ti ešte beží aplikácia otvor si browser a choď na http://localhost:8080/ . Dostaneš whitelabel error page s nejakou správou (prečítaj si ju), že takútu adresu tvoja aplikácia nepozná. No tento error ti vrátila tvoja appka. Keď teraz zastavíš svoju bežiacu appku a znovu sa pozrieš na http://localhost:8080/ zisíš, že už taká url nebeží.
  
Pridaj teraz do svojho projektu novú triedu s názvom EmployeeController. Urob z nej RestController a vytvor v nej svoj prvý endpoint, ktorý bude vracať text Hello Spring Boot. 

Ak si to urobil spráne a znovu pôjdeš na http://localhost:8080/ mal by si vidieť svoj výpis.

Pre pochopenie endpointov:

Uprav kód tak aby sa Hello Spring Boot vypísalo pri navigáii na http://localhost:8080/hello . Funguje aj http://localhost:8080/ ? 

Pridaj ďalšie 2 endpointy ktoré vrátia výsledky volaní metód z EmployeeService.

Pridaj ďalší endpoint, ktorý vráti výsledok z 1. Java cvičenia (Snail goes up the Stairs). Parametre (výška schodu, ...) prídu v requeste.

Pomôcka:

endpoint = prístupový bod, cez ktorý sa bude dať s tvojou aplikáciou komunikovať

Všetky potrebné informácie nájdeš na https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#getting-started-first-application-code v časti Writing the Code. 

  Client (u nás Angular app)  Server (u nás Spring Boot app) komunikácia prebieha pomocou HTTP. Viac info nájdeš napríklad na https://www.w3schools.com/tags/ref_httpmethods.asp. 
  </details>
  
  <details>
  <summary>Working with the database</summary>
  
  ### Working with the database
  
  <details>
  <summary>Starting with the DB</summary>
  
  ### Starting with the DB
  
  Na začiatok trochu teórie. Napríklad tu https://www.oracle.com/database/what-is-database/ nájdeš nejaké základné informácie. Ale kľudne si prečítaj aj z iných zdrojov.
  
  Pri vývojí aplikácie potrebujeme dáta s ktorými  pracujeme nejakým spôsobom uchovovávať aby keď sa aplikácia zavrie, dáta ostanú zachované a pri ďalšom spustení sa oäť z databázy načítajú. Práve na to slúži databáza.
  
  **databáza** - kolekcia **dát**, ktorá je nejakým spôsobom organizovaná
  
  **DBMS** - database management system
           - niečo čo pomáha pracovať s databázou
  
  Poznáme rôzne typy databáz. Na stránke, ktorú som uviedol v úvode si môžeš prečítať aké. My budeme pracovať s relačnou databázou.
  
  **relačná databáza** - databáza je zložená z tabuliek, ktoré medzi sebou majú určité vzťahy (relations)
  
  Každá tabuľka pozostáva zo stĺpcov a riadkov, kde stĺpce predstavujú akoby atribúty a riadky obsahujú jednotlivé hodnoty týchto atribútov.
  
  Napríklad:
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/osoba_table.PNG></img>
  
  Máme tabuľku Osoba, ktorá má 3 stĺpce: id, meno a email. <br>Každá tabuľka musí mať tzv. **primárny kľúč (PK)**. Primárny kľúč je niečo čo jednoznačne identifikuje každý záznam v tabuľke. Môže byť tvorený 1 alebo viacerými stĺpcami. Keď kľúč tvorí viac ako jeden stĺpec hovoríme o **kompozitnom primárnom kľúči (KPK)**. V tabuľke Osoba je primárnym kľúčom stĺpec nazvaný **id**. To znamená, že hodnota tohto stĺpca je jedinčená a nikdy v danej tabuľkej nebudú 2 záznamy s rovnakou hodnotou.
  <br>Riadky v tejto tabuľke predstavujú už konkrétne osoby.
  
  Napríklad:
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/osoba_example.png></img>
  
  Tu už teda máme jeden záznam v tabuľke Osoba.
  
  Teraz si predstav, že chceš o Osobe uchovávať aj adresu. Pre adresu si môžme vytvoriť novú tabuľku a medzi tabuľkami Osoba a Adresa vytvoríme vzťah. Vyzeralo by to asi takto.
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/adresa.png></img>
  
  Opäť, tabuľka Adresa má svoj primárny kľúč, stĺpce ulica, mesto a psc a posledným stĺpcom je osoba_id. Stĺpec osoba_id v tomto prípade vystupuje ako tzv. **foreign key (FK)** a je akoby referenciou (odkazom) na osobu, ktorej daná adresa prislúcha. To znamená, že najskôr musí existovať osoba, ktorej následne pridelím adresu.<br>Z obrázku so záznamom našej jednej osoby má táto osoba id číslo 1. Takže keď budem chcieť vytvoriť adresu pre túto osobu tak hodnotu v stĺpici osoba_id nastavím na 1.
  
  Existuje niekoľko vzťahov, ktoré môžu byť medzi tabuľkami. V našom príklad sme použili **vzťah 1:1**. Teda 1 osoba má práve 1 adresu. Nie viac. Keby osoba mohla mať viac adries tak by to bol **vzťah 1:N**. Ďalej ešte poznáme **vzťah M:N**. Kľudne si pohľadaj na internete viac.
  </details>
  
  <details>
  <summary>Adding the database</summary>
  
  ### Adding the database
  
  My budeme používať relačnú databázu od Oracle-u, ktorá sa volá MySQL (kľudne si prečítaj na internete).
  
  Na https://dev.mysql.com/downloads/installer/ si stiahni mysql-installer-web-community..
  
  Pomôcka k inštalácii:<br>
  **Setup type** zvoľ **Custom** a vyber **MySQL server 8.0.22** a **Connector/J 8.0.22**.<br>
  Potom klikni **next** a na ďalšej klikni **execute** a počkaj kým dobehnú potrebné veci.<br>
  Na **Type and Networking** len klikni **next**. Podobne aj pri **Authentication**.<br>
  Pri **Accounts and Roles** si nastav heslo pre tzv. root account. **TOTO HESLO SI ZAPAMÄTAJ. Budeš ho potrebovať.**<br>
  Na **Windows service** môžeš nechať označený check box a klikni **next**.<br>
  Na **Apply configuration** klikne **execute** a opäť počkaj kým dobehnú potrebné veci.<br>
  
  Keď skončíš, otvor si MySQL command line client. Ako heslo použi heslo, ktoré si zadal pri tvorbe root account-u.
  
  Po úspešnom pripojení by si mal vidieť niečo takéto:
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/mysql_connected.sql.PNG></img>
  
  Teraz si vytvoríš svoju databázu a jedného používateľa s právami. V cmd line clientovi zadaj nasledovné príkazy:
  
  _create database **database_name**;_ // vytvorí databázu s názvom aký zadáš
  
  database_name si zvoľ aký chceš ty. Príklad: create database db_example;
  
  Ďalej spusti:
  
  _create user ‘**user_name**’@’localhost’ identified by ‘**password**’;_ // vytvorí používateľa s menom _user_name_ a heslom _password_
  
  Znovu, user_name a password si zvoľ aký chceš. **No pamätaj si čo zadáš.** Príklad: create user 'user_example'@'localhost' identified by 'password_example';
  
  A posledný:
  
  _grant all on database_name.* to ‘user_name’@’localhost’;_ // pridá práva používateľovi s menom _user_name_ na databázu s názvom _database_name_
  
  database_name je meno databázy, ktorú si si vytvoril pri prvom príkaze a user_name je meno, ktoré si použil pri druhom príkaze. Príklad: grant all on db_example.* to 'user_example'@'localhost';

  #### DB tool

  Teraz si stiahni a nainštaluj nejaký DB nástroj, napr. https://dbeaver.io/download/.
  
  Keď si ho otvoríš vytvor si novú connection. Klikni na:
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/new_conn.png></img>
  
  Zvoľ MySQL:
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/mysql_chosen.png></img>
  
  a vyplň user name a heslo. Použi údaje toho user-a, ktorého si si predtým vytvoril.
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/connection.png></img>
  
  Ak sa ti podarilo pripojiť mal by si vidieť niečo takéto:
  
  <img src=https://github.com/AppsLab-2/materials/blob/master/conn_success.png></img>
  
  Máš tam teda svoju databázu, do ktorej keď sa pozrieš tak zistíš, že ešte neobsahuje žiadne tabuľky.
  
  </details>
  <details>
  <summary>Spring Data JPA</summary>

  ### Spring Data JPA
  
  Spring Data JPA je ďalšia časť framework-u Spring, ktorá pomáha zjednodušiť prácu s databázou. Robí to pomocou JPA - Java Persistence API a tzv. ORM - Object Relational Mapping. Prečítaj si na internete viac, prípadne si pozri nejaké video.
  
  **ORM nám pomôže mapovať naše Java triedy do tabuliek v našej MySQL databáze.**
  
  #### Adding the dependencies
  
  Najskôr pridaj do svojho pom.xml, do časti _dependencies_, nové závislosti. Konkrétne pre _spring-boot-starter-data-jpa_ a mysql-connector-java. Keďže používame maven tak potrebné závislosti nájdeš na https://mvnrepository.com/ . Keď ich vyhľadáš, kľudne klikni na prvú verziu a skopíruj danú dependency do svojho pom.xml. Z tej dependency môžeš potom kľudne tú časť s verziou (<version>...</version>) vymazať, maven bude vedieť akú verziu použiť podľa verzie, ktorú máme v parent tag-u v pom.xml.
  
  #### Spring Boot application.properties
  
  Spring Boot má mnohé veci nastavené defaultne. Tým nám vlastne zjednodušuje našu prácu. Ak by si chcel vedieť viac o tom aké _properties_ Spring Boot pozná tak tu https://docs.spring.io/spring-boot/docs/current/reference/html/appendix-application-properties.html nájdeš viac.
  
  Čo ale v prípade, keď potrebuješ tieto nastavenia upraviť podľa svojej potreby?
  
  Na to slúži súbor _application.properties_ . Tu si pridáme nasledovné:
  
  **spring.jpa.hibernate.ddl-auto=update** // hibernate je ORM (Object Realational Mapping) tool; prečítaj si na internete čo robí táto property<br>
  **spring.datasource.url=jdbc:mysql://localhost:3306/database_name** // namiesto database_name daj meno db, ktoré si si zvolil keď si vytváral svoju db<br>
  **spring.datasource.username=user_name** // sem daj meno používateľa, ktoré si si zvolil keď si si vytváral usera pre svoju db<br>
  **spring.datasource.password=password** // sem daj heslo používateľa, ktoré si si zvolil keď si si vytváral usera pre svoju db<br>
  
  Týmto vlastne povieme Spring Boot-u ako sa má pripojiť k našej databáze. Heslo by samozrejme nemalo byť takto jednoducho prístupné, no na teraz to nebudeme riešiť.
  
  Ak si urobil všetko správne mal by si vedieť úspešne spustiť svoju appku.
  
  #### Cvičenia
  
  **Cvičenie:** Vytvor teraz triedu Company s atribútom name a namapuj ju ako tabuľku do svojej databázy. Toto by ti mohlo pomôcť: https://www.youtube.com/watch?v=QVpQodGBb8U.
  Keď potom spustíš svoju aplikáciu a pozrieš sa do svojej databázy v DBeaver (alebo v inom nástroji, ak si si zvolil iný) mal by si tam vidieť svoju tabuľku.

  **Cvičenie:** Vytvor teraz CompanyRepository interface, kt. ti pomôže pracovať s tabuľkou company. Tu je pomôcka: https://www.youtube.com/watch?v=z3HnFBzn7DI.
  
  **Cvičenie:** Vytvor interface CompanyService s metódou _saveCompany(Company company)_. K nej vytvor implementačnú service-u CompanyServiceImpl s jedným atribútom typu CompanyRepository. V tele metódy _saveCompany_ zavolaj metódu _save_ na CompanyRepository. Teraz vytvor CompanyController ako @RestController s jedným atribútom typu CompanyService. Ďalej tam urob jeden _get_ endpoint s path hodnotou "company". V tele vytvor objekt typu Company a zavolaj _saveCompany_. Keď spustíš svoju appku a naviguješ na 
http://localhost:8080/company. V databáze v tabuľke company by si mal vidieť prvý záznam.

**Cvičenie:** Keď znovu pôjdeš na http://localhost:8080/company uvidíš, že už sa ti ďalší záznam nevloží pretože _id_, ktoré si nastavil tomu prvému je primary key. To znamená, že už nemôžeš vložiť iný objekt s rovnakou hodnotou atribútu _id_. Povedzme, že nechceme manuálne pridávať hodnoty pre _id_. Pridaj anotáciu _@GeneratedValue(strategy= GenerationType.AUTO)_ pod anotáciu _@Id_ v triede Company. Vymaž teraz nastavenie atribútu _id_ z endpointu kde vytváraš objekt typu Company. Spusti appku. Teraz keď budeš volať http://localhost:8080/company uvidíš, že sa ti pridáva stále nový záznam do tabuľky company. Všimni si aké hodnoty nadobúda _id_. Chápeš čo robí anotácia, ktorú sme pridali? Tiež si všimni, že v databáze ti pribudla nová tabuľka - hibernate_sequence. Túto tabuľku vytvoril Hibernate sám a drží si tam hodnotu, ktorú použije najbližšie ako hodnotu pre stĺpec id.

**Code structure cvičenie:** Množstvo tried v našom projekte začína pomaly narastať. Pre prehľadnosť a čitateľnosť kódu je dobré vytvoriť si určitú štruktúru orgranizácie súborov v projekte. Jedným z možných spôsobov je združovať triedy povedzme po typoch, napr. všetky controllery budú v package-i controllers, repozitáre v repositories, pre entity v model atď. Iný spôsob môže byť združovanie podľa toho čo s čím súvisí. Urobiť si napríklad package company, v ktorom bude všetko čo súvisí s Company, teda repozitár, service-a aj controller. Skús si teda svoje triedy roztriediť jedným z týchto štýlov. <br>
Tieto obrázky by ti mohli pomôcť:<br> 
Prvý spôsob: https://stackoverflow.com/a/53317601/8900927. <br>
Druhý spôsob: https://stackoverflow.com/a/55590796/8900927

**Cvičenie:** Pridaj teraz triedu Address, ktorá bude mať 5 atribútov: id, street, zipCode, city a state. Namapuj túto triedu do svojej databázy. Povedzme, že každá pridávaná spoločnosť musí mať zadefinovanú aj adresu kde sídli. Vytvor teda vzťah 1:1 medzi Company a Address tak aby sa to prejavilo aj v databáze. Nastav tiež aby Company musela vždy mať nastavenú adresu, inak Company nebude možné vložiť do databázy.

**Cvičenie:** Typický príklad funkcionality vo web aplikácii je, že informácie o niečom sa vyplnia na FE cez nejaký formulár a keď používateľ klikne na tlačítko tak sa všetky informácie zoberú a pošľú na BE, kde sa to uloží do databázy a pri ďalšom spustené appky sa tieto dáta už môžu čítať z databázy. Keď to prenesiem na náš príklad, predstav si, že FE nám pošle dáta o nejakej spoločnosti, ktorú chce používateľ pridať.<br><br>Urob teraz POST endpoint, ktorý bude v request body príjmať objekt, ktorý bude obsahovať všetkých 5 atribútov (companyName + všetky address fieldy). Keď mu niekto pošle dáta tak tieto dáta vezme a uloží do databázy ako nový riadok v tabuľke company a address.<br><br>Stiahni si napríklad Postman-a https://www.postman.com/downloads/. Postman ti umožní vykonávať post requesty. Nastav si teda, že chceš vykonať POST, ďalej URL na tvoj BE endpoint. Zvoľ záložku Body, vyber RAW a v poslednom dropdowne vyber JSON. <br>
Podobne ako je to tu:<br><img src="https://github.com/AppsLab-2/materials/blob/master/postman.png"></img><br>
Do RAW potom napíš JSON objekt s dátami, ktoré budú poslané do na tvoj BE. Keď potom klikneš na SEND (tvoja appka musí byť spustená) tvoj BE odchytí dáta, ktoré mu posielaš (predstav si, že to posiela FE) a uloží ich do databázy. Ak všetko prebehlo správne mal by si v databáze vidieť nové záznamy.
<br>Ak nevieš ako písať JSON objekt alebo aj niečo iné skús si to vyhľadať na internete, nemalo by to byť nič zložité. :)

**Cvičenie:** Urob teraz aby sme v databáze mali ďalšiu tabuľku s názvom employee, v ktorej sa budú ukladať všetci zamestnanci. Teda aby sme NEmali tabuľku pre jednotlivé pozície zvlášť ale iba jednu spoločnú. Podobne ako v predošlom cvičení, urob POST endpoint, ktorý v request body príjme zoznam niekoľkých zamestnancov a uloží ich do databázy.

**Cvičenie:** Každá spoločnosť môže mať niekoľko zamestnancov a povedzme, že každý zamestnanec môže byť v danom čase zamestnaný v práve jednej spoločnosti. To znamená, že trieda Company bude mať ďalší atribút - List alebo Set - zamenstancov a medzi Company a Employee vznikne vzťah 1:N = 1 spoločnosť : N zamenstancov. Nadefinuj teda tento vzťah v kóde. Napríklad toto by ti mohlo pomôcť: https://www.baeldung.com/hibernate-one-to-many . <br>Keď to máš, skús to upraviť tak (ak to tak ešte nemáš), aby sme pri ukladaní nového zamestanca do našej databázy pridávali len ID danej spoločnosti. To znamená, že keď budem vytvárať nového zamestnanca napr. new Driver(salary, bonus, companyId) tak mu v parametri companyId zadám len ID spoločnosti, v ktorej pracuje a nie celý objekt Company. S týmto by ti mohlo pomôcť toto: https://stackoverflow.com/a/50378345/8900927 . Vyskúšaj poslať POST request pre uloženie nového zamestnanca spolu s ID spoločnosti, ku ktorej ho chceš priradiť. Čo ak zadáš ID spoločnosti, ktoré neexistuje? <br>Príklad funkcionality pre lepšiu predstavu: Opäť si predstav, že máme nejakú web appku, ktorá dokáže zobrazovať zoznam spoločností a k nim ich zamestnancov. Taktiež ponúka možnosť pridať nového zamestnanca k nejakej z týchto spoločností. Na FE je teda nejaký formulár pre pridanie nového zamestnanca kde sa vyplní všetko potrebné - meno a tak ďalej. V tomto formulári bude tiež nejaký dropbox, ktorý bude obsahovať názvy všetkých dostupných spoločností, z ktorých sa jedna vyberie. Následne sa všetky dáta pošľú na BE a tam sa spracujú. Nemusíme zbytočne posielať celý objekt Company na BE, stačí nám jeho ID.

**Cvičenie:** Teraz si predstav, že každý zamestnanec sa môže zúčastniť rôznych školení. Zároveň platí, že jedného školenia sa môže zúčastniť niekoľko zamestnancov naraz. To znamená, že medzi nimi existuje tzv. M:N vťah. Vytvor triedu Course, ktorá bude predstavovať školenie. Táto trieda bude obsahovať atribúty title (názov školenia), startTime (dátum a čas začiatku školenia) a endTime (dátum a čas ukončenia školenia). Namapuj stĺpce to do tabuľky v databáze a tiež samotný M:N vzťah medzi Employee a Course. Toto by ti mohlo pomôcť: https://www.baeldung.com/jpa-many-to-many . Keď spustíš svoju appku v databáze by si mal vidieť svoje nové tabuľky. Pridaj si nový endpoint (alebo uprav niektorý z už existujúcich) a vyskúšaj či ti to funguje.

  </details>
  </details>
  <details>

  <summary>Spring Security</summary>

  ### Spring Security

  Autor: Erik Zemčík

  <details>
  <summary>Úvod</summary>

  ### Úvod

Pri vytváraní projektu budeme potrebovať zabezpečiť našu aplikáciu. Nechceme, aby niekto mohol vykonávať činnosti, ku ktorým by nemal mať prístup. Na toto nám slúži Spring Security, framework, ktorý jednoducho pridáva autentifikáciu a riadenie prístupu k jednotlivým prvkom našej aplikácie. Pridaj teda do pom.xml dependency spring-boot-starter-security a môžme začať.

```xml
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

Skús teraz poslať request cez prehliadač na nejaký endpoint. Ako si môžeš všimnúť, tak si nedostal odpoveď, ktorú si očakával, dostal si prihlasovaciu obrazovku

![Login Form](https://github.com/AppsLab-2/materials/blob/master/security_form_login.png?raw=true)

Ak teraz skúsiš to isté cez Postmana, tak uvidíš, že sa ti znova nevráti odpoveď, ktorú si očakával, ale dostaneš kód 401 - Unauthorized (to znamená, že tvoj request neobsahoval platné údaje pre autentifikáciu).

Aj keď sme nič nekonfigurovali, tak Spring Security hneď od nás žiada údaje na prihlásenie. Spring Security sa stáva aktívny hneď po pridaní do projektu a očakáva s každým requestom potrebné údaje pre prihlásenie. My sme síce používateľa nevytvárali, ale Spring Security automatický jedeného vytvorí, ak nie je inak nakonfigurovaný (toto si ukážeme v ďalších častiach). Tento používateľ má username ‘user’ a heslo, ktoré sa náhodne vygeneruje a vypíše do konzole pri spustení aplikácie.

![Vygenerované heslo](https://github.com/AppsLab-2/materials/blob/master/security_generated_password.png?raw=true)

Skús sa teraz cez prehliadač prihlásiť do tohto usera s týmito informáciami (username = ‘user’, heslo nájdeš v konzoli). Ak si všetko urobil správne, tak by si mal mať odpoveď, ktorú si očakával hneď na začiatku. Ak teraz skúsiš znova urobiť nejaký request (aj na iný endpoint), tak uvidíš, že heslo nemusíš znova zadávať.

No, ako teraz v Postmanovi? Tam sa nás nikto nepýtal na heslo, request hneď zlyhal. V Postmanovi môžeš nastaviť meno a heslo v záložke Authentication, ak si zvolíš typ Basic.

![Basic autentifikácie v Postmanovi](https://github.com/AppsLab-2/materials/blob/master/security_postman_basic.png?raw=true)

Skús poslať request v Postmanovi na ľubovoľný endpoint s menom a heslom.

  </details>
  <details>  
  <summary>Základna konfigurácia</summary>  
 
### Základna konfigurácia
Ak chceme konfigurovať Spring Security, tak to budeme musieť urobiť prostredníctvom novej triedy, ktorá dedí od `WebSecurityConfigurerAdapter` a musí mať anotáciu `@EnableWebSecurity`.
Príklad:
```java
@EnableWebSecurity  
public class SecurityConfig extends WebSecurityConfigurerAdapter {  

}
```
`WebSecurityConfigurerAdapter` obsahuje niekoľko metód, ktoré slúžia na konfiguráciu rôzných aspektov Spring Security. Ak sa chceš pozrieť hlbšie ako funguje, môžeš sa pozrieť [tu](https://docs.spring.io/spring-security/site/docs/current/api/org/springframework/security/config/annotation/web/configuration/WebSecurityConfigurerAdapter.html). Napríklad pre konfiguráciu autentifikácie prepíšeme takto túto metódu:
```java
@Override  
protected void configure(AuthenticationManagerBuilder auth) throws Exception {  
      
}
```
`AuthenticationManagerBuilder` nám dovoľuje rýchlo nastaviť, že odkiaľ má Spring Security brať údaje o používateľoch. Každý uživateľ sa skladá z niekoľkých údajov (ako napríklad meno, heslo, rola, ...). Ako zdroj údajov môžeme použiť viacero vecí, ktoré si neskôr ukážeme, ale na teraz nám stačí preddefinovať používateľov v kóde (tým ich uložíme v pamäti). Toto môžeme docieliť takto:
```java
@Override  
protected void configure(AuthenticationManagerBuilder auth) throws Exception {  
    auth.inMemoryAuthentication()  
            .withUser("apps-lab")  
            .password("hello-world")  
            .roles("USER");  
}
```
Ak by si to teraz skúsil, tak by si zistil, že to nefunguje 😀. Chýba nám totiž ešte jedná vec. Potrebujeme dodať Spring Security takzvaný `PasswordEncoder`. Úlohou rozhrania `PasswordEncoder` je starať sa o bezpečné ukladanie hesiel. Existuje viacero implementácií tohto rozhrania, z ktoých si môžme vybrať, ale nám zatiaľ stačí `NoOpPasswordEncoder`, ktorý z heslom neurobí nič. **POZOR:** `NoOpPasswordEncoder` sa **musí** neskôr vymeniť za nejakú alternatívu, toto si ukážeme neskôr. Pridáme teda do našej konfigurácie nový bean:
```java
@Bean  
public PasswordEncoder passwordEncoder() {  
    return NoOpPasswordEncoder.getInstance();  
}
```
Ak to teraz skúsiš znova a ak si urobil všetko správne, tak by si mal byť schopný prihlásiť sa pomocou špecifikovaných údajov.
  </details>
  </details>
</details>
