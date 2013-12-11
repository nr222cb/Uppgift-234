Kravspecifikation Bokningsplattform för ett nystartat hotell/B&B
=================================================================

Referenser
----------

*[Vision](https://github.com/nr222cb/Uppgift-234/blob/master/Vision.txt)*

Här beskrivs bakgrund, användargrupper och baskrav.

Aktörer
-------

Primära Aktörer
---------------

1 Kund

Vill på ett enkelt sätt boka rum på hotellet. Vill snabbt 

få kontakt med hotellet om det finns några frågor eller oklarheter.

2 Personal

Vill ta emot bokningar från kunder med alla nödvändiga bokningsdetaljer och tydlig information om kunden.

3 Ägare/Manager

Vill få ut viss statistik om bokningar - Hur många bokningar har kommit in genom den egna plattformen? 
Hur ser beläggningsgraden ut för en given period?

Stödjande Aktörer
------------------

Offstage Aktörer
------------------

Webbmaster

Vill att bokningssystemet skall ha ett liknande gränssnitt som den befintliga webbplatsen för att 

kunderna skall känna sig trygga.

Funktionella Krav
------------------

F1 Information om kunden

Kunden skall behöva ange kontaktinformation till sig själv först i slutskedet av bokningsprocessen, 
först söka fram ett rum som passar, sedan ange kontaktinformation

Användningsfall
-----------------

1 Kund

AF1.1 Boka Rum

AF1.2 Kolla tillgänglighet för ett visst typ av Rum

2 Personal

AF 2.1 Ta emot en Bokning

3 Ägare/Manager

AF 3.1 Ta ut en rapport om inkommna Bokningar genom den egna plattformen för en given period


Ickefunktionella Krav
-----------------------

Projektkrav
------------

Begränsningar
--------------

B1 Integration med befintlig webbplats

Bokningsfunktionen skall integreras med befintlig webbplats

Kvalitetskrav
---------------

Användbarhet

> Anv 1 Grafisk Utformning

> Bokningssystemet skall grafiskt utformas som den befintliga webbplatsen i fråga om färg och form. En 

> kund skall inte se eller känna någon skillnad jämfört med övrig webbplats när den gör en bokning.

Tillgänglighet

> Tillg 1

> Inga begränsningar får finnas vare sig med hänsyn till hårdvara, mjukvara eller bandbredd för att kunna genomföra en bokning

Stödbarhet

Prestanda

Säkerhet

> Säk 1 Användning av HTTPS

> Bokningssidorna skall vara skyddade genom användning av HTTPS