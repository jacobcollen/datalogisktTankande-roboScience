# Datalogiskt Tankande Robot Scientists


## Figma-skiss: https://www.figma.com/file/DbVIZuNRi9iBpe1XaMQ4hu/Untitled?type=whiteboard&node-id=0%3A1&t=cqYuLMvNdmLiOynK-1

#Sammanfattning

## Decomposition

## Pattern recognition

## Decomposition

Fem huvudområden har definierats:
-Branding
-Meny
-Orderhantering
-Användarhantering
-Produkthantering 
Dessa har delats upp i underområden utifrån appens tänkta funktion, framför allt ur företagets perspektiv.
Sent i processen har det insetts att gruppen kan ha gått händelserna i förväg och blandat in abstraction i uppdelningen,
och resultatet blir en mycket slimmad decomposition som kunde ha innehållit fler detaljer.

## Pattern recognition
Databashantering
Även om appen har en tämligen enkel konstruktion kräver en del funktioner lagring av data, t.ex. produktdata, lagerinformation, användarinformation, och orderhistorik.

Gränssnittsmönster
Appen har en lekfull design med ett genomgående tema som utgår från grafiken på förstasidan. Denna grafik går igen på övriga sidor, antingen som bakgrund eller som sidhuvud och sidfot. Formspråket är enkelt och tydligt vilket möjliggör lätt och snabb hantering och beställning för användaren.
Menyn har få alternativ och användaren gör sitt val genom att klicka på “+” för att lägga till varan i varukorgen

Navigationsmönster
Appen har en hamburgarmeny längst upp till vänster på de sidor där det är nödvändigt. Därifrån kan användaren lätt nå de funktioner som är nödvändiga för beställning. Det finns också en ikon för varukorg uppe i högra hörnet, där antal varor syns och som kan användas för att komma till varukorgen

Beställningsflöden
Flödet är enkelt utformat. Användaren lägger först till sina varor och väljer sedan att gå till varukorg/checkout. Vid checkout går det att beställa både som inloggad och ej inloggad. Det är lätt att lägga till och ta bort varor, och att betala och slutföra beställningen. Flödet följer samma mönster både för registrerade, inloggade kunder och för icke inloggade kunder. Arbetsorder skapas vid beställning och används i olika delar av flödet, men syns inte för kunden. Orderhistorik finns på flera ställen och kan nås både av systemet och av kunden.

En frekvensanalys har gjorts. Analysen visade att databas förekom oftast, med fem tillfällen.
De övriga två; arbetsorder och orderhistorik, förekom två gånger vardera. Övriga punkter förekom endast en gång.
Utifrån det har slutsatsen dragits att antalet databaser är tillräckligt men det är många punkter som används som skulle kunna användas mer. Detta har tillämpats så gott det går.

## Abstraction
En del av abstraktionen är utförd redan i första steget eftersom gruppen gått händelserna i förväg. Därmed blir resultatet en något grund analys. 

Stora delar av de bakomliggande delarna är abstraherade för kunden. Den färdiga produkten är enkelt designad för användaren, och endast viktiga funktioner finns representerade, såsom meny, orderhistorik och inloggning/användarinfo.

Användaren går igenom beställningsprocessen snabbt och smidigt utan några omvägar och får sin beställning och leverans utförda på ett enkelt sätt.

Produkterna har ID, namn, och pris. Saldo finns i databasen men är abstraherat för kunden eftersom det endast är för internt bruk.

Varukorgsföremål har ID, namn, pris och antal.


## Algorithm design
Diskussion om att login ska förekomma direkt när appen öppnats har förekommit. Ingen förändring blev gjord eftersom appen verkar vara konstruerad så att login-möjligheten ligger sent i flödet. 
Designen speglar kundens agerande och interaktion med appen under beställningsprocessen. 
Alla delar av processen anses vara representerade i skissen.
