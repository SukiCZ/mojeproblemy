---
layout: page
title: Pracuji
---

Již více jak dva roky pracuji jako **programátor** ve společnosti která prodává autodíly. Autodíly mi sice nic neříkají - jsou to krabičky v kterých jsou díly a mají své číslo. Ale to hlavní je, že jsem **programátor**. Mé vysněné povolání. Mačkat tlačítka a koukat do logů kterým málo kdo rozumí. Je to výzva implemenotvat nové funkcionality, opravovat existující a optimalizovat je. Poslední dobou je to čím dál tím stejnější - sedět v kanclu.

Hned po nástupu jsem dostal na starost projekt zvaný **DRES** - *Developer Request Evidence System*. Je to systém na evidování vývojových požadavků psaný v Javě, pod sebou má [FireBird DB](https://firebirdsql.org/). Hned ze začátku jsem si všiml, že projekt generuje (2N+1) dotazů do databáze při listování vývojových požadavků. To jsem během chvilky změnil a po nasazení si mě všichni začali chválit. Netrvalo dlouho a byla mi nabídnuta smlouva na dobu neurčitou.

**Na neurčito** zkuste si to slovo zašeptat. Budu zde *neurčitě* pracovat dokud *někdo* neurčí, že zde pracovat nebudu. Kromě finančního ohodnocení se moc nezměnilo.

Dostal jsem na starost další projekt **EDI** - *Electronic Data Interchange*. Systém na shromažďování fiskálních dokumentů. Navíc obsahuje rozhraní pro komunikaci s pár dodavateli. Je psaný v Javě, používá framework zvaný [Hibernate](http://hibernate.org/) a pod sebou má [MSSQL DB](https://www.microsoft.com/en-us/sql-server/sql-server-2017). Zde jsem řešil implementaci nových rozhraní pro dodavatele, kteří nám dostupnost zboží posílali např. jednou denně mailem, jiní přes FTP nebo na to využívali webové služby **SOAP** - *Simple Object Access Protocol*. V mezi čase jsem dělal drobné úpravy naší HelpDesk aplikace, která je psaná v C# a do databáze jsem se nikdy nedostal. I tak mi to šlo.

Po pár letech v práci mi ukázali další projekt **MCAT** - *Mobile Catalogue*. Je v něm zaimplementovaná i JSON REST API pro desktopy a této části se říká **MAXI** - asi moc velká. Projekt bývával outsourcovaný a tým který ho řešil na to ztratil nervy. Neposlední co v nervách měli bylo mé zaškolení do projektu. Projekt je psaný v [Python](https://www.python.org/) (2.7), využívá Framework [Django](https://www.djangoproject.com/) (1.6.10), pod sebou má 3 [maria db](https://mariadb.org/), jednu jen pro čtení produktových inforamcí, jednu regionální pro udržování sessions, aktuálních košíků, ... a jednu pro logování. Jednu Sphinx databázi pro vyhledávání. Přihlašování uživatele, aktuální ceník, fiskální dokumenty či odesílání košíku se řeší pomocí SOAP WS. Loguje se i pomocí `sentry` a také do textových souborů na které bych jedině doporučil `grep`, `tail -f`, `awk` a další. Tento projekt jsem rok a půl vychovával se vší úctou. Zde jsem řešil vše od analýzy požadavků, jejich zapracování, psaní unittestů až po psaní dokupentace v APIARY.

Trápilo mě, že jsem na vývoji backendu - našeho hlavního e-shopu - sám a právě proto mi byli nalezeni dva kolegové - junioři - pracující v externí společnosti. Poté co první kolega porušil naší vývojovou workflow a vytvořil branch z develop větve (do develop větve padá veškerý rozpracovaný bordel), tak jsme po těchto juniorech vyžadovali otevírat Pull Requesty (požadavky na přijetí změny kódu) kterým jsem dělal review. Ze začátku to šlo fakt fajn protože pokud tyto junioři nevěděli co mají dělat, tak se mě ptali a já je navigoval správným směrem což mi pomohlo k rychlejšímu schvalování PR. Nadřízený těchto juniorů z toho začal dostávat dojem, že na ticketu by měl pracovat jeden vývojář nikoliv vývojář a schvalovatel dohromady a od té doby jsou PR hell. Několikrát se mi stalo, že jsem je zavřel bez komentáře jelikož neřešili co jsme požadovali aby řešeno bylo.

<iframe width="100%" height="315" src="https://www.youtube-nocookie.com/embed/x60V0eayiAY?rel=0&amp;showinfo=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

```
BANG!
Playin' a different game
Kill 'em all
```
