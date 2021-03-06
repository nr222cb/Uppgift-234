AF 1.1 Boka Rum
===============

En kund vill boka ett eller flera rum på hotellet och utgår från ett visst datum och antal dagar man vill stanna på hotellet.  
Systemet presenterar tillgängliga rum för den givna perioden.  
Efter att kunden valt typ av rum och antal rum samt bekräftat sitt val genereras det en bokning med ett unikt id och en bokningsbekräftelse presenteras  
på skärmen samt skickas iväg med epost till kunden och hotellets personal.

Primär Aktör
-----------

Kund

Sekundär Aktör
--------------

Personal: Får epost med bokningsdetaljer efter genomförd bokning

Offstage Aktör
---------------

Webbmaster: ger riktlinjer för utseende och integration i befintligt system.

Förkrav
-------

Efterkrav
---------

Epost med bokningsinformation skickas ut till kund och personal.  
Rum markeras som ej tillgängliga för bokning i systemet.

Huvudscenario
--------------

1. Startar när Kunden vill boka ett rum.

2. Systemet ber kunden att ange ett ankomstdatum och hur många nätter man vill stanna.

3. Kunden anger ett ankomstdatum och många nätter man vill stanna

4. Systemet presenterar i nästa steg typ och antal av tillgägliga rum. Man får också en prisuppgift för varje typ av rum.

5. Kunden väljer ut önskat rumstyp och antal rum.

6. Systemet sammanfattar och presenterar kundens val i nästa steg.

7. Kunden bekräftar sitt val.

8. Systemet ber om kontaktinformation till kunden.

9. Kunden anger sina kontaktuppgifter.

10. Systemet visar en bokningsbekräftelse med ett unikt bokningsnummer på skärmen och valda rum markeras som ej tillgängliga i systemet.

11. Systemet skickar ut bokningsbekräftelsen både till kunden och hotellet.

Alternativa Scenarios
---------------------

4a Det finns inga tillgängliga rum för angivet datum

1. Systemet meddelar kunden att inga rum finns tillgängliga för det angivna datumet

2. Kunden kan välja ett nytt datum

Gå till steg 1

6a Systemet sammanfattar kundens val och kunden upptäcker ett fel eller ångrar sig

1. Systemet sammanfattar och presenterar kundens val

2. Kunden upptäcker att något är fel och vill börja om från start

Gå till steg 1

9a Fel format eller utelämnad kontaktinformation

1. Ifall kunden utelämnar en detalj eller skriver in den i fel format får man ett felmeddelande från systemet

2. Kunden ges möjlighet att korrigera sina fel

Gå till steg 9

6a Temporär reservation av rum

1. Efter att kunden valt ett rum för bokning markeras rummet som reserverat av systemet

2. Om inte kunden genomför bokningen och kommer till steg 10 inom 5 minuter  
stäpps den temporära reservationen och kund meddelas att sessionen har tajmat ut (time-out)

Användningsfallet avslutas


Datadefinitioner och Affärsregler
---------------------------------

Pris per natt

Pris för rumstyp per natt presenteras under steg 3


Pris för bokningen

Pris för hela bokningen presenteras under steg 5 och utgörs av pris för rumstyp per natt * antal nätter * antal bokade rum