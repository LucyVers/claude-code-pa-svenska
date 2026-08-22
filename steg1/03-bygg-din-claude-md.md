# Bygg din globala CLAUDE.md i Claude Code

[← Tillbaka till kursplanen](../KURSPLAN.md)

*Del av kursen [Claude Code på svenska](../README.md) — Steg 1: Minne. Skrivbordsappen.*

CLAUDE.md är filen Claude alltid läser först i en session, innan den
gör något annat. Tänk på den som ett facit om dig: vem du är, vad du
håller på med, och hur du vill att Claude ska agera när den inte
redan vet svaret. Har du redan importerat ditt minne i förra
lektionen är det här nästa steg, att göra det minnet till något Claude
faktiskt läser varje gång du öppnar den.

Inte installerat Claude Code än? [Gör det
först](../borja-har/05-installera-claude-code.md), sen kommer du
tillbaka hit.

## Så bygger du den, i två steg

### Steg 1: be Claude sammanfatta dig

Öppna Claude desktop-appen, starta en ny chatt, och klistra in:

> [!NOTE]
>
> ```
> Summarise everything you know about me, my business, my goals, and
> how I like to work into a clean, short context block. Sections:
> About me, Current projects, How I like to work, Definition of done.
> Keep it tight and factual, plain text, no emojis, no fluff.
> ```

Du får tillbaka ett rent block med fakta om dig. Kopiera det.

### Steg 2: lämna över det till Claude Code

Öppna Claude Code-panelen i samma fönster och klistra in (byt ut
hakparentesen mot blocket du just kopierade):

> [!NOTE]
>
> ```
> Here's a summary of me and my work: [PASTE YOUR BLOCK HERE]. Save
> this as my global memory (CLAUDE.md) so you read it at the start of
> every session. Then show me what you saved.
> ```

Tryck enter, och du är färdig för idag. Ingen fil att leta upp, inget
att komma ihåg att göra imorgon, öppna bara Claude Code nästa gång så
är minnet redan där.

## Två regler för ett minne som faktiskt hjälper

**Kort text.** En handfull konkreta rader ger bättre resultat än ett
helt dokument. Ju mer Claude måste läsa för att hitta det viktiga,
desto sämre presterar den.

**Inga emojis.** Det Claude ser i sitt eget minne färgar av sig på
allt annat den skriver åt dig, kodkommentarer, commit-meddelanden,
texter. Håll filen helt neutral så smittar inte stilen vidare.

## Så kan strukturen se ut

```
# Om mig
Namn: [ditt namn]
Roll: [vad du gör]
Kommunikation: rakt på sak, kort, inga omskrivningar

# Aktuella projekt
- [projekt ett]
- [projekt två]

# Hur jag vill jobba
- Öva mer än läsa
- Leverera den minsta användbara versionen först

# Definition av klart
- En fungerande länk någon annan kan använda
- En riktig person har sett att det funkar
```

Din kan bli tio rader eller tjugo, båda funkar lika bra.

Claude Code utvecklas snabbt. Det som stämmer idag kan vara förändrat
om några månader. Jag uppdaterar allt eftersom jag hinner och hittar
ny information.

---

**Skapat av [Lucy Sonberg](https://www.linkedin.com/in/lucysonberg)** · [GitHub](https://github.com/LucyVers)
Licensierat under [CC BY-NC-ND 4.0](../LICENSE). Dela gärna med kredit, hör av dig för kommersiell användning eller institutionell licensiering.
