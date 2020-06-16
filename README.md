# selectors

Specify szelektor
Előfordul, hogy egy szelektorral nem tudod pontosan kijelölni az elemet. Ekkor pontosabban kell rámutatnod az elemre, pontosabban kell specifikálnod. Egyszerre több szelektort használsz, például:

a.menu-link:hover

vagy durvábban

input.form-control[type=email]:focus

A szelektort egybeírjuk, ha egy elemre vagy elem-csoportra vonatkozik.

Egymásba ágyazott elemek kiválasztása
Van, hogy csak egy bizonyos elemen belül szeretnél dolgozni. Ekkor először a szülőt kell megadnod. Például a login azonosítójú formon belüli összes input elem megadása:

form#login input

> jel csak a közvetlen gyerekeket jelöli, az unokákat már nem ;)

form#login > input

***

Attribute szelektor
Az elemet valamilyen tulajdonsága alapján választja ki. A tulajdonság nevét és értékét egyenlőségjellel elválasztva szögletes zárójelek között adjuk meg. Például:

[type='button']

Ha nem adunk meg értéket, akkor azokat az elemeket jelöli ki, ahol a tulajdonság létezik. Például:

[disabled]

Jele: [ ]
Előnye: külön formázást adhatunk meg egy elemnek eltérő tulajdonságok esetén.
Hátránya: böngésző támogatása nem teljesen egységes.

***

Szövegek helyettesítése CSS szelektorokban
[attribute^=value]
Példa: a[href^="https"]
Kiválasztja az összes olyan elemet, aminek az adott attribútuma a megadott szöveggel kezdődik.

[attribute$=value]
Példa: a[href$=".pdf"]
Kiválasztja az összes olyan elemet, aminek az adott attribútuma a megadott szöveggel végződik.

[attribute*=value]
Példa: a[href*="training360"]
Kiválasztja az összes olyan elemet, aminek az adott attribútuma a megadott szöveget bárhol tartalmazza.

***

Pseudo szelektorok
A pseudo szó hamisat jelent. Azért ez a nevük, mert olyan tulajdonságokra vonatkoznak, amelyeket a böngésző automatikusan rendel az elemekhez. Például ha az elem fölé visszük az egeret, vagy kattintottunk már egy linkre. Az eredeti szelektor után kell kettősponttal írni, például:

a:hover vagy a:visited

Fontosabb pseudo szelektorok
:hover - ha az elem fölé viszik az egeret,
:visited - azok a linkek, amelyekre már kattintottak,
:active - ha a felhasználó használ egy elemet, mondjuk rákattint,
:focus - elsősorban input mezőknél, ha éppen használjuk,
:first-child - a szülő elem első gyereke,
:last-child - a szülő elem utolsó gyereke,
:nth-child(n) - az n-edik gyereke a szülő elemnek,
:empty - olyan elem, aminek nincs gyereke, azaz nem tartalmaz beágyazott elemet,
:checked - a kiválasztott checkbox,
:disabled - letiltott elem.