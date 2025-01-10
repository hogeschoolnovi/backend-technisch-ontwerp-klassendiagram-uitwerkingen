### UserStories:
- Als "Medewerker" wil ik alle producten kunnen opvragen, zodat ik de juiste informatie van een product kan inzien en dat mooi kan verkopen aan de klant.
- Als "Medewerker" wil ik een lijst van producten op voorraad kunnen zien, zodat ik weet welke producten ik uit voorraad kan verkopen en welke ik moet bestellen.
- Als "Admin" wil ik de voorraad van producten kunnen inzien en beheren, zodat ik optijd producten kan bestellen. 
- Als "Admin wil ik de naam, prijs, en compatibiliteit van producten kunnen invoeren en bijwerken, zodat de productinformatie altijd up-to-date is.

### Functionele eisen: 

1. De API moet producten kunnen verwijderen uit het systeem, mits deze niet meer verkocht worden of op voorraad zijn.
2. De API moet een lijst van alle beschikbare producten retourneren, gesorteerd op type of naam.
3. De API moet details van een specifiek product kunnen opvragen op basis van een uniek product-ID.
4. De API moet de mogelijkheid bieden om de compatibiliteit van een product met andere producten op te slaan en op te vragen (bijvoorbeeld: een afstandsbediening die bij een specifieke tv past).
5. De API moet een overzicht kunnen geven van de actuele voorraad per producttype, gesorteerd op type of locatie.
6. De API moet het aantal verkochte producten per producttype kunnen bijhouden en teruggeven.
7. De API moet de mogelijkheid bieden om een product als "uitverkocht" te markeren als de voorraad op nul staat.
8. De API moet gebruikersrollen ondersteunen (bijvoorbeeld beheerder en medewerker) en bij elke actie valideren of de gebruiker voldoende rechten heeft.
9. De API moet een endpoint hebben waarmee beheerders nieuwe gebruikers kunnen toevoegen en rollen kunnen toekennen.
10. De API moet gebruikersgegevens (zoals naam, rol, en contactgegevens) kunnen opvragen en bijwerken, uitsluitend toegankelijk voor beheerders.
11. De API moet loggegevens van productwijzigingen kunnen opslaan, inclusief welke gebruiker een wijziging heeft aangebracht en op welk moment.
12. De API moet een endpoint bieden om een lijst van producten te retourneren die binnenkort op voorraad komen, inclusief verwachte leverdatum.
13. De API moet compatibiliteitsadviezen geven door een lijst te retourneren van producten die samen gebruikt kunnen worden (bijvoorbeeld: muurbeugels geschikt voor een bepaalde tv).
14. De API moet de mogelijkheid bieden om een product (tv, muurbeugel, afstandsbediening, CI-module) toe te voegen aan het systeem met gegevens zoals naam, type, prijs en voorraad.
15. De API moet producten kunnen bijwerken, inclusief naam, prijs, type, en voorraadstatus.



### Niet-Functionele eisen
1. De applicatie moet voldoen aan de **OWASP Top 10** beveiligingsrichtlijnen. Voorafgaand aan de implementatie moet een beveiligingsscan worden uitgevoerd waarbij geen kritieke kwetsbaarheden worden gedetecteerd.
2. De applicatie moet reageren op gebruikersacties binnen maximaal **2 seconden** bij het ophalen van voorraad- of productinformatie, gemeten onder een belasting van **100 gelijktijdige gebruikers**.
3. Batchprocessen zoals voorraadupdates of rapportgeneratie mogen niet langer dan **10 seconden** duren om te voltooien.
4. De applicatie moet een beschikbaarheid van minimaal **96%** hebben, berekend over een periode van **1 maand**, exclusief geplande onderhoudsperiodes.
5. Bij een storing moet de applicatie binnen **1 uur** na detectie weer operationeel zijn.
6. De gebruikersinterface moet door een nieuwe medewerker binnen **1 uur** begrepen kunnen worden, vastgesteld via een gebruikerstest met minimaal **10 medewerkers**.
7. Foutenmeldingen moeten begrijpelijk en contextspecifiek zijn, zodat gebruikers direct weten welke actie nodig is.
8. Bij doorontwikkeling van de API moet backwards compatibaliteit gegarandeerd worden tot minimaal 2 major versies.
