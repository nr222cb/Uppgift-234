Testfall
========

TF *[AF1.1 Boka Rum Huvudscenario](https://github.com/nr222cb/Uppgift-234/blob/master/AF%201.1%20Boka%20Rum.md)*
--------------------------------------------------------------------------------------------------------------------

I detta testfall �r m�let att unders�ka om kunden kan boka ett rum p� hotellet

F�rkrav
-------

Det finns en testmilj� med webbplats och bakomliggande databas, i databasen kar man lagt till minst ett rum av typ enkelrum  
och minst ett rum av typ dubbelrum

Efterkrav
---------

Kontrollera att det har genererats en bokning med ett unikt id, att rummet som kunden v�ljer att boka markeras som ej tillg�ngligt  
i bokningssystemet samt att det skickas ut en bokningsbekr�ftelse med epost b�de till kunden och hotellet.

Scenario
--------

1.Kunden surfar in till hotellets webbplats och �ppnar fliken Booking.  
2.Systemet ber kunden att ange ett ankomstdatum och hur m�nga n�tter man vill stanna genom tv� formul�rf�lt.  
3.Kunden v�ljer ett datum fr�n ett formul�rkontroll med datum samt skriver in antal n�tter (2) man vill stanna.  
4.Systemet presenterar en dropdown-lista med minst ett enkelrum och minst ett dubbelrum som finns tillg�ngliga f�r den valda perioden.  
Man f�r ocks� en prisuppgift f�r varje typ av rum.  
Single room | 1 room | 50 EUR per night  
Double room | 1 room / 2 rooms | 70 EUR per night  
5.Kunden v�ljer 1 rum av typ enkelrum.  
6.Systemet sammanfattar och presenterar kundens val.  
Arriving on 27/12/2013  
How many nights? 2  
Type of Room Single  
Total booking price 100 EUR (Ber�knas utifr�n Pris per natt * Antal n�tter * Antal rum i bokningen)  
7.Kunden v�ljer att g� vidare genom att trycka p� "Proceed with booking"  
8.Systemet presenterar ett antal formul�rf�lt d�r kunden kan skriva in First name | Last name | Address | Telephone | Email | Arrival time  
9.Kunden anger ovanst�ende uppgifter  
10.Systemet visar en bokningsbekr�ftelse med ett unikt bokningsnummer p� sk�rmen och valda rum markeras som ej tillg�ngliga i systemet.  
Systemet skickar ut bokningsbekr�ftelsen b�de till kunden och hotellet.

3a.Kunden v�ljer att skriva in datum ist�llet f�r att v�lja med datepicker.  
G� till steg 4  


TF *[AF1.1 Boka 4a](https://github.com/nr222cb/Uppgift-234/blob/master/AF%201.1%20Boka%20Rum.md)*
--------------------------------------------------------------------------------------------------------------------