Testfall
========

TF *[AF1.1 Boka Rum Huvudscenario](https://github.com/nr222cb/Uppgift-234/blob/master/AF%201.1%20Boka%20Rum.md)*
--------------------------------------------------------------------------------------------------------------------

I detta testfall är målet att undersöka om kunden kan boka ett rum på hotellet

Förkrav
-------

Det finns en testmiljö med webbplats och bakomliggande databas, i databasen kar man lagt till minst ett rum av typ enkelrum  
och minst ett rum av typ dubbelrum

Efterkrav
---------

Kontrollera att det har genererats en bokning med ett unikt id, att rummet som kunden väljer att boka markeras som ej tillgängligt  
i bokningssystemet samt att det skickas ut en bokningsbekräftelse med epost både till kunden och hotellet.

Scenario
--------

1.Kunden surfar in till hotellets webbplats och öppnar fliken Booking.  
2.Systemet ber kunden att ange ett ankomstdatum och hur många nätter man vill stanna genom två formulärfält.  
3.Kunden väljer ett datum från ett formulärkontroll med datum samt skriver in antal nätter (2) man vill stanna.  
4.Systemet presenterar en dropdown-lista med minst ett enkelrum och minst ett dubbelrum som finns tillgängliga för den valda perioden.  
Man får också en prisuppgift för varje typ av rum.  
Single room | 1 room | 50 EUR per night  
Double room | 1 room / 2 rooms | 70 EUR per night  
5.Kunden väljer 1 rum av typ enkelrum.  
6.Systemet sammanfattar och presenterar kundens val.  
Arriving on 27/12/2013  
How many nights? 2  
Type of Room Single  
Total booking price 100 EUR (Beräknas utifrån Pris per natt * Antal nätter * Antal rum i bokningen)  
7.Kunden väljer att gå vidare genom att trycka på "Proceed with booking"  
8.Systemet presenterar ett antal formulärfält där kunden kan skriva in First name | Last name | Address | Telephone | Email | Arrival time  
9.Kunden anger ovanstående uppgifter  
10.Systemet visar en bokningsbekräftelse med ett unikt bokningsnummer på skärmen och valda rum markeras som ej tillgängliga i systemet.  
Systemet skickar ut bokningsbekräftelsen både till kunden och hotellet.

3a.Kunden väljer att skriva in datum istället för att välja med datepicker.  
Gå till steg 4  


TF *[AF1.1 Boka 4a](https://github.com/nr222cb/Uppgift-234/blob/master/AF%201.1%20Boka%20Rum.md)*
--------------------------------------------------------------------------------------------------------------------