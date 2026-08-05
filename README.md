|Csapattagok| 

Jónás Viktor (projektvezető) - adatbázis

Pál Petúr - frontend

Pap Attila - backend

FoxyShop
==================================================
Az eredeti ötlet egy olyan webshop, ami ösztönözi a társadalmat a környezettudatosságra és tudatos összefogásra kapcsolatkiépítésen keresztül.

A projekt célja:
---------------
A FoxyShop egy átfogó webes platform, amely egy róka-tematikájú online kereskedelmi felületet biztosít, emellett pedig egy edukatív környezetet teremt a fiatalabb generációk számára. A projekt célja, hogy a rókák szimbolikáján keresztül ösztönözze a felhasználókat a környezettudatosságra, valamint fejlessze a közösségi kommunikációs képességeket.

Miért egyedi a FoxyShop?
-----------------------
A hagyományos webáruházaktól eltérően a FoxyShop nem csupán egy tranzakciós felület. A közösségi fórum integrációjával edukatív funkciót is betölt: a vásárlás folyamata mellett a közösség aktív tagjait környezettudatos szemléletre ösztönzi. A projekt elsődleges célja nem csupán az értékesítés, hanem a fiatalok bevonása egy olyan digitális környezetbe, ahol a tudatos vásárlás és a minőségi kommunikáció kéz a kézben járnak.



Mire nyújt megoldást?

A projekt 2 társadalmi problémára nyújt megoldást:

    Környezettudatosság hiánya: A gyorsan változó pénzügyi és piaci környezetben kevés hangsúly kerül a környezettudatos gondolkodásmód fejlesztésére.

    Kommunikációs nehézségek: A mai fiatalok gyakran nehezebben folytatnak minőségi, mélyreható párbeszédeket; ezt a problémát egy beépített fórummal kezeljük.

(Megfelelés a KKK elvárásának – Valódi probléma: A szoftver valós, mindennapi társadalmi kihívásokra – a környezettudatosság hiányára és a generációs kommunikációs nehézségekre – kínál kézzelfogható digitális megoldást.)
Műszaki és Technológia megvalósítás:



A szoftver RESTful architektúrára épül, biztosítva a szétválasztott szerver- és kliensoldali működést.

    Skálázhatóság: Mivel a rendszer RESTful architektúrára épül, a szerveroldal stateless, ami lehetővé teszi, hogy a terhelést több szerver között osszuk meg. A nagy felhasználói szám kezelése érdekében a jövőben adatbázis-optimalizációt, indexelést, valamint a gyakran kért adatok gyorsítótárazását tervezzük alkalmazni, így elkerülve a szerver túlterhelését.

    Használt Technológiák: Visual Studio, C#, Angular, HTML, CSS, TypeScript

    Verziókezelés: Github, Github Desktop



(Megfelelés a KKK elvárásának – RESTful architektúra: A C# alapú backend szerver és az Angular alapú frontend kliens teljesen szétváltan működik. A kommunikáció HTTP kéréseken keresztül, JSON formátumban történik, és a szerver stateless módon szolgálja ki a klienseket.)
Fő funkciók:

    Webshop: Fox-tematikájú termékek (ruhák, kiegészítők...) értékesítése, árusítása.

    Fórum: Közösségi tér, ahol a felhasználók a rókákról vagy hétköznapi témákról beszélgethetnek.

(Megfelelés a KKK elvárásának – Asztali és mobil használat: Az Angular keretrendszer reszponzív kialakításának köszönhetően a kliensoldali felület zökkenőmentesen és azonos élménnyel használható asztali számítógépeken, valamint mobil eszközök böngészőjében is.)
Adatkezelés és biztonság:



A rendszer biztonságos felhasználói hitelesítést alkalmaz:

    Regisztráció: Felhasználónév, jelszó (minimum 8 karakter, nagy- és kisbetűk, számok és szimbólumok használata).

    Belépés: A hitelesítés ugyanazokat az információkat kéri be, amit a regisztráció során a felhasználó megadott, de emellett e-mail cím alapú alternatívával is kiegészített.

    Validáció: A bemeneti adatok ellenőrzése mind kliens-, mind szerveroldalon megvalósításra került az adatbiztonság érdekében.

    Biztonsági kockázatok: Bár a rendszer validációval védett, a webáruház ki van téve olyan gyakori támadásoknak, mint az SQL injection, valamint a Cross-Site Scripting (mely során a fórumon keresztül kártékony scripteket futtatnának), illetve a Brute Force támadások, amelyek a jelszavak kitalálására irányulnak. Emiatt a jelszavak titkosított tárolása és a bemeneti adatok szigorú szűrése kiemelt feladatunk volt a fejlesztés során.



|A KKK elvárásainak megfelelően|
-------------------------------
•	Valódi probléma: Életszerű, létező problémára kell megoldást nyújtania. 

•	Adatkezelés: Adattárolási és adatkezelési funkciókat kell megvalósítania.

•	RESTful architektúra: Tartalmaznia kell szerver (backend) és kliens (frontend) oldali komponenseket egyaránt. A két oldalnak elkülönülten kell űködnie, http kérésre JSON formátumú válasz jön. Kérés közben a szerver nem tárol adatokat a kliensről.

•	Asztali és mobil használat: A kliensoldali résznek alkalmasnak kell lennie mindkét platformra. Mobilnál natív app vagy azzal egyenértékű webes kliens is elfogadott. Asztali eszközre kötelező a webes megvalósítás, de mellé választható natív asztali app is.

•	Tiszta kód: A forráskódnak kötelezően követnie kell a tiszta kód (clean code) alapelveit. (A fejlesztés során alkalmazott modulos komponensépítés, átlátható névhasználat és struktúra biztosítja)

•	Dokumentáció: Kötelező hozzá egy technikai leírást, működési feltételeket és rövid használati útmutatót tartalmazó dokumentáció.

A projektet GitHubon vagy hasonló szolgáltatáson keresztül kell megosztani, és a csomagnak pontosan a következő elemeket kell tartalmaznia:

•	Forráskód: A szoftver teljes, tiszta kódú forráskódja.

•	Telepítőkészlet: Natív asztali alkalmazás fejlesztése esetén a program telepítőfájlja. (Jelen webes/Angular projektnél a webes kliens miatt nem releváns, de a szerver/backend futtatható csomagja biztosított).

•	Adatbázismodell-diagram: Az adatbázis szerkezetét bemutató diagram.

•	Adatbázis export fájl: Az adatbázis dump fájlja (.sql vagy megfelelő formátumban).

•	Szoftveralkalmazás dokumentációja: A fent említett célokat és technikai paramétereket részletező leírás.

•	Tesztelési anyagok: A futtatott tesztekhez írt kód (tesztkód), valamint a kapott teszteredmények dokumentációja.

|További Témaötleteink|
----------------------
Apróhirdetés portál - Helyi szolgáltatások adásvételére specializálódott és olyan mindennapi teendőkre fókuszál, mint pl a fűnyírás, a korrepetálás vagy a kutyasétáltatás. Bárki könnyedén feladhatja a saját hirdetését, ha segítséget keres vagy kínál. Gyorsan és egyszerűen lehet böngészni a környéken elérkező megbízások és szabad segítők között

Iskolatúra – egy alkalmazás, amely osztálykirándulások, túrák megtervezésére szakosodna. Igyekszik megkönnyíteni az osztályfőnökök munkáját megkönnyíteni megfelelő célpontok, utazási módszerek és felkészültség ellenőrzésén keresztül. 

