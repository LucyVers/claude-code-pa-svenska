# Allt du behöver veta om terminalen i Claude Code

[← Tillbaka till kursplanen](../KURSPLAN.md)

*Del av kursen [Claude Code på svenska](../README.md) — Börja här. Frivillig fördjupning.*

Läs det här bara om du är nyfiken. Skrivbordsappen klarar allt annat i
kursen på egen hand, och du kan gå igenom hela kursen utan att någonsin
öppna en terminal. Den här sidan finns för dagen du vill förstå vad
som faktiskt döljer sig bakom den svarta rutan, inte för att du måste.

Sidan växer allt eftersom fler terminaltips är värda att dela.

## En vänlig första titt

Glöm bilden av hackare som trummar in kryptiska kommandon i mörkret.
En terminal är mycket mer vardaglig än så.

### Vad terminalen faktiskt är

Du skriver en rad, trycker enter, och datorn utför den. I grunden är
det samma sak som att klicka en knapp i skrivbordsappen, bara utan
knappen. Ingen kod, bara vanliga ord i rätt ordning, ungefär som att
söka efter något.

### Så öppnar du en

Tre alternativ, välj det som är närmast till hands:

**Mac.** Tryck Cmd och mellanslag, skriv "Terminal", tryck enter.

**Windows.** Klicka Start, skriv "Terminal" (eller "PowerShell"),
tryck enter.

**Inuti VS Code.** Öppna Terminal-menyn högst upp, klicka "New
Terminal". En panel öppnas längst ner, praktiskt eftersom koden och
terminalen ligger sida vid sida.

Stäng den genom att skriva `exit` och trycka enter, eller stäng bara
fönstret. Inget går sönder, att stänga en terminal raderar aldrig ditt
arbete.

### Att läsa skärmen

Det här är delen ingen förklarar, så gå långsamt igenom den.

**Prompten.** Raden med den blinkande markören väntar på dig. Den
slutar ofta med `$`, `%` eller `>`, helt normalt. Du skriver efter
den.

**"Ingenting hände."** Du kör ett kommando och inget meddelande dyker
upp. De flesta får panik här, men det betyder nästan alltid att allt
gick som det skulle. Terminalen hör bara av sig när den faktiskt har
något att säga dig, annars jobbar den tyst vidare.

**Något jobbar.** Sitter markören still och du kan inte skriva, jobbar
något fortfarande. Låt det bli klart. När prompten kommer tillbaka är
det färdigt.

**Ett riktigt fel.** Riktiga fel är oftast rött, eller en rad som
börjar med "error" eller "command not found". De ser läskigare ut än
de är. Kopiera texten, klistra in den i Claude, så får du en lösning.

I praktiken behöver du bara skilja på tre lägen på skärmen, väntar på
dig, jobbar fortfarande, eller berättar något. Kan du det, kan du
terminalen.

### De två sätten att röra dig

Du använder de här för att peka terminalen mot rätt mapp innan du
startar Claude Code:

**`cd mappnamn`** flyttar dig in i en mapp ("cd" står för change
directory). `cd mitt-projekt` tar dig in i ditt projekt.

**`ls`** listar vad som finns i mappen du står i, så du ser var du är.

Mer än så behöver du sällan, resten kan du överlåta åt Claude.

## Kommandona du faktiskt skriver själv

Även i terminalen skriver du nästan ingenting tekniskt med egna
fingrar. Du beskriver vad du vill ha på vanligt språk, och Claude
sköter resten. Listan över det du själv behöver skriva är kort nog
att få plats här i sin helhet.

**För att komma igång:**

`cd mitt-projekt` tar dig till projektmappen (från förra avsnittet).
`claude` startar Claude Code direkt i terminalen, samma samtal som i
appen.

**Ett fåtal snedstreck-kommandon lönar sig att kunna:**

`/clear` rensar det pågående samtalet. Använd det när du byter till en
helt ny uppgift och inte vill att gammal kontext hänger med.

`/model` byter vilken Claude-modell du kör. Bra att känna till när en
specifik uppgift behöver mer (eller mindre) kraft.

`/resume` öppnar en tidigare konversation precis där du lämnade den.
Stäng datorn, kom tillbaka imorgon, skriv `/resume`, och projektet
fortsätter mitt i tanken.

`!` kör ett enstaka datorkommando utan att du lämnar Claude. Sällan
nödvändigt, men bra att veta att det finns.

Fler kommandon än så behöver du sällan lära dig utantill, resten är
sådant du beskriver i ord snarare än skriver för hand.

### Det du ser Claude köra

Du skriver aldrig de här själv, men det hjälper att känna igen dem när
de rullar förbi på skärmen, så det inte känns som en gåta:

`ls` listar filer, `cd` byter mapp. `git status` visar vad som
ändrats, `git commit` sparar en checkpoint (se [Git](../ORDLISTA.md#git)
i ordlistan). `npm install` lägger till ett verktyg projektet behöver
(se [npm](../ORDLISTA.md#npm)).

Ingen av dem kräver något av dig, de är bara till för att skärmen ska
kännas begriplig istället för kryptisk medan Claude jobbar.

### När terminalen faktiskt är värd att öppna

Appen räcker nästan alltid. Tre situationer där terminalen ändå är
smidigare:

**Plocka upp en gammal session.** `claude` följt av `/resume`, ett
rent sätt tillbaka in i gårdagens arbete.

**Långa jobb eller sådant som körs i bakgrunden.** Terminalen håller
på utan att låsa ditt fönster.

**När appen krånglar.** Att starta `claude` i en terminal är en
pålitlig plan B.

Inget av det här är obligatoriskt. Vill du hellre stanna i appen är
det ett fullgott val, kvaliteten på det du bygger beror inte på vilken
du väljer.

**Nästa:** [Steg 1, Varför Claude Code behöver komma ihåg dig](../steg1/01-varfor-minnet-kommer-forst.md)

Claude Code utvecklas snabbt. Det som stämmer idag kan vara förändrat
om några månader. Jag uppdaterar allt eftersom jag hinner och hittar
ny information.

---

**Skapat av [Lucy Sonberg](https://www.linkedin.com/in/lucysonberg)** · [GitHub](https://github.com/LucyVers)
Licensierat under [CC BY-NC-ND 4.0](../LICENSE). Dela gärna med kredit, hör av dig för kommersiell användning eller institutionell licensiering.
