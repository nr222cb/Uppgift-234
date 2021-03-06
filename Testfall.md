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
3.Kunden väljer ett datum (27/12/2013) från ett formulärkontroll med datum samt skriver in antal nätter (2) man vill stanna.  
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


TF *[AF1.1 4a Det finns inga tillgängliga rum](https://github.com/nr222cb/Uppgift-234/blob/master/AF%201.1%20Boka%20Rum.md)*
--------------------------------------------------------------------------------------------------------------------

Förkrav
-------

I databasen har alla rum markerats som ej tillgängliga för perioden december 2013


Scenario
--------

1.Kunden surfar in till hotellets webbplats och öppnar fliken Booking.  
2.Systemet ber kunden att ange ett ankomstdatum och hur många nätter man vill stanna genom två formulärfält.  
3.Kunden väljer ett datum (27/12/2013) från ett formulärkontroll med datum samt skriver in antal nätter (2) man vill stanna.  
4.Systemet presenterar en lista med rum på hotellet och ett meddelande att de ej är tillgängliga  
Single room | Not available for dates selected! | 50 EUR per night  
Double room | Not available for dates selected! | 70 EUR per night  
5.Kunden kan gå tillbaka till steg 2 för att börja om och välja ett annat datum  

TF *[AF1.1 9a Fel format eller utelämnad kontaktinformation](https://github.com/nr222cb/Uppgift-234/blob/master/AF%201.1%20Boka%20Rum.md)*
--------------------------------------------------------------------------------------------------------------------

Förkrav
--------

Felhantering implementerad för kundens kontaktinformation både genom client-side teknik (JavaScript) och server-side teknik  


Efterkrav
---------

Korrekt data i databasen om kunden och dess kontaktinformation  

Scenario
--------

1.Kunden surfar in till hotellets webbplats och öppnar fliken Booking.  
2.Systemet ber kunden att ange ett ankomstdatum och hur många nätter man vill stanna genom två formulärfält.  
3.Kunden väljer ett datum (27/12/2013) från ett formulärkontroll med datum samt skriver in antal nätter (2) man vill stanna.  
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
First name - "Lisa" | Last name - "Noname" | Address - "London st 18 Brighton" | Telephone - "donno" | Email - "testartestar" | Arrival time - "14"  
10.Systemet markerar fälten Telephone och Email som fel och tillåter ej kunden att gå vidare.  
11.Kunden korrigerar uppgifter.  
12.Systemet visar en bokningsbekräftelse med ett unikt bokningsnummer på skärmen och valda rum markeras som ej tillgängliga i systemet.  
Systemet skickar ut bokningsbekräftelsen både till kunden och hotellet.  

TF *[AF1.1 6a Temporär reservation av rum](https://github.com/nr222cb/Uppgift-234/blob/master/AF%201.1%20Boka%20Rum.md)*
--------------------------------------------------------------------------------------------------------------------

Förkrav
-------

Implementerat system för temporär reservation av rum (ett särskilt state för det i databasen)  

Efterkrav
----------

Kontrollera att rummets status sätts till temorärt ej tillgägligt i db efter steg 6.  
Kontrollera att den temporära reservation släpps efter steg 10.  

Scenario
---------

1.Kunden surfar in till hotellets webbplats och öppnar fliken Booking.  
2.Systemet ber kunden att ange ett ankomstdatum och hur många nätter man vill stanna genom två formulärfält.  
3.Kunden väljer ett datum (27/12/2013) från ett formulärkontroll med datum samt skriver in antal nätter (2) man vill stanna.  
4.Systemet presenterar en dropdown-lista med minst ett enkelrum och minst ett dubbelrum som finns tillgängliga för den valda perioden.  
Man får också en prisuppgift för varje typ av rum.  
Single room | 1 room | 50 EUR per night  
Double room | 1 room / 2 rooms | 70 EUR per night  
5.Kunden väljer 1 rum av typ enkelrum.  
6.Systemet sammanfattar och presenterar kundens val och skapar en temporär reservation (rummet markeras som temporärt ej tillgängligt i databasen).  
Arriving on 27/12/2013  
How many nights? 2  
Type of Room Single  
Total booking price 100 EUR (Beräknas utifrån Pris per natt * Antal nätter * Antal rum i bokningen)  
7.Kunden väljer att gå vidare genom att trycka på "Proceed with booking"  
8.Systemet presenterar ett antal formulärfält där kunden kan skriva in First name | Last name | Address | Telephone | Email | Arrival time  
9.Kunden låter bli att ange ovanstående uppgifter  
10.Efter 5 minuter av inaktivitet presenterar systemet ett meddelande om att sessionen tajmat ut och kunden kan börja om, den temporära reservationen hävs.