# Prompter som hjälper dig komma igång med Claude Code

[← Tillbaka till kursplanen](../KURSPLAN.md)

*Del av kursen [Claude Code på svenska](../README.md) — Börja här.*

Claude Code kan bygga nästan vad som helst. Den kan inte tala om vad
du ska bygga.

Den delen är din, och det är den delen de flesta hoppar över. Här
samlar jag prompter som hjälper dig jobba smartare i Claude Code. Jag
fyller på listan allt eftersom jag hittar fler som är värda att dela.

> [!NOTE]
> Prompterna på den här sidan står på engelska, både de jag skriver
> själv och de jag citerar. Prompter tenderar att fungera bättre på
> originalspråket, och för citerade prompter är det viktigt att orden
> stämmer exakt.

## Jobba smartare

Ordningen här följer hur du faktiskt jobbar: hur du sätter igång, hur
du jobbar medan Claude Code bygger, hur du håller allt hanterbart ju
längre en session pågår, och hur du håller tempot över flera veckor.
Du behöver inte köra alla, bara det som känns relevant just nu.

Ny i Claude Code? Skapa en tom mapp, öppna den i Claude Code, och
klistra in prompten.

**Öppningsprompt för [plan mode](../ORDLISTA.md#plan-mode).** Boris
Cherny, en av grundarna bakom Claude Code, berättade att han alltid
börjar i plan mode. Anledningen
är enkel: det mesta bortkastade arbetet kommer inte av dålig kod, utan
av att Claude byggt fel sak från början. En plan innan koden fångar
det misstaget tidigt.

Kopiera prompten nedan och byt ut det som står inom hakparenteser:

> [!NOTE]
>
> ```
> I want to build [WRITE YOUR REQUEST HERE]. Before writing any code, stay in
> plan mode and help me define the problem in detail. Ask me clarifying
> questions one at a time, surface gaps in my thinking, and don't move
> on until you are 95% confident you understand exactly what I need.
> When you're confident, show me a written plan and wait for my
> approval before touching any code. Ultrathink.
> ```

Citat från [Boris Cherny](https://github.com/bcherny), Claude Code på
Anthropic.

**Ge tydligt sammanhang, begränsningar och mål.** Claude kan bara jobba
med det du faktiskt ger den. Skriver du in bakgrund, begränsningar och
exakt vad du vill uppnå innan du ber om något, minskar risken för
generiska förslag rejält.

> [!NOTE]
>
> ```
> Treat yourself as a brilliant contractor I just hired who has never
> seen my project. Here is the context: [BACKGROUND]. Here are my
> constraints: [CONSTRAINTS]. Here is the exact outcome I expect:
> [OUTCOME]. Build [SPECIFIC THING] — and before you start, tell me what
> an expert in [FIELD] would be thinking about that I haven't mentioned.
> ```

**Välj rätt modell för uppgiften.** Att köra allt på den mest
kraftfulla modellen är sällan nödvändigt. Rätt modell för rätt uppgift
förlänger din sessionsgräns rejält, utan att tappa kvalitet där det
faktiskt räknas.

> [!NOTE]
>
> ```
> Run /model and switch me to 'Opus plan' so planning runs on Opus and
> execution automatically drops to Sonnet. From now on use Sonnet as the
> default for coding, Haiku for sub-agents and simple research, and only
> escalate to Opus for genuinely hard architectural decisions. Confirm
> what you've set.
> ```

**Dela upp i små uppgifter.** Ett stort mål blir snabbt för mycket att
hålla i huvudet på en gång, för dig och för Claude. Bryter du ner det
i tydliga, små steg blir varje enskild uppgift lättare att göra rätt,
och du slipper sessioner som spårar ur.

> [!NOTE]
>
> ```
> Take this idea — [YOUR BIG IDEA] — and break it into the smallest
> possible atomic tasks, in build order. Show me the full task list
> first and wait for my approval. Then we'll tackle exactly one task at
> a time, and you'll commit to git after each one before moving to the
> next.
> ```

**Förstå innan du godkänner.** Vet du inte vad som skiljer ett
gränssnitt från en databas kan du inte heller avgöra om ett förslag
faktiskt passar din situation, bara lita blint på det. Förstår du hur
bitarna hänger ihop kan du också ifrågasätta och felsöka när något
krånglar.

> [!NOTE]
>
> ```
> Whenever you recommend a tech choice, library, or approach I might not
> understand, stop and explain it to me in simple terms before we
> continue — and if I'm still unclear I'll say 'explain it again.' I
> never need to write code myself, but I do want to understand the
> building blocks. So as we go, tell me why you're doing it this way.
> ```

**Bygg in kvalitetskontroll i uppgiftslistan.** Kvalitetskontroll blir
en del av arbetet istället för ett separat steg du kanske hoppar över.
Claude bygger, kontrollerar och fixar innan den går vidare.

> [!NOTE]
>
> ```
> When you build [WHAT WE'RE BUILDING], add verification steps directly
> into your to-do list: after building, take a screenshot and check it
> looks right, then open the browser dev tools / console to confirm
> there are no errors, then fix anything broken. Don't move to the next
> to-do until you're 95% confident the current one actually works.
> ```

**Låt Claude sköta installationen.** Claude erbjuder ofta manuella
steg som standard. Den här prompten gör tydligt att du vill att Claude
gör jobbet åt dig, och håller dina API-nycklar säkra i en `.env`-fil
istället för i chatten.

> [!NOTE]
>
> ```
> I want to install [TOOL NAME]. Here is the documentation: [DOCS OR
> GITHUB URL]. First check what I already have installed, then install
> everything I need and walk me through any credentials step by step.
> Do NOT give me manual instructions — do everything for me. Store any
> API keys in a .env file, never in our chat.
> ```

**Håll koll på din [kontextanvändning](../ORDLISTA.md#kontextfönster).**
Utan en statusrad märker du inte att kontextfönstret fylls förrän
Claude redan tappat skärpa. Sätt upp den en gång, så finns
informationen alltid framför dig. Du behöver
inte komma ihåg att kolla själv.

> [!NOTE]
>
> ```
> Run /statusline and set up a status line that always shows my current
> directory, the model I'm using, a visual progress bar of my context
> window usage, and my token count. Make it persistent so it sits below
> the prompt window in every session from now on.
> ```

**Rensa kontexten i tid.** Ju fullare kontextfönstret blir, desto sämre
presterar Claude, redan runt halvvägs märks det. Lösningen är inte att
undvika långa sessioner, utan att sammanfatta läget innan du startar
om, så du kan fortsätta där du var utan att förlora något.

> [!NOTE]
>
> ```
> We're getting deep into this session. Give me a full but concise
> summary of everything we've done, every decision we locked in, the
> key files, and the exact next steps — written so a brand-new session
> could pick up right where you left off. I'll run /clear and paste this
> back in. From now on, prompt me to do this whenever we cross about 50%
> of the context window.
> ```

**Håll ett jämnt tempo, inte perfekt tempo.** Tid, inte svårighetsgrad,
är det som stoppar flest. Har du bara en kort stund per kväll spelar
det ingen roll hur bra nästa idé känns, hoppar du mellan projekt blir
du aldrig klar med något. Lås ett enda bygge, jobba i korta pass, och
lämna alltid en rad till dig själv om nästa steg. Räkna framsteg per
vecka, inte per kväll.

> [!NOTE]
>
> ```
> I get about 60 minutes a night and I keep starting over on new ideas.
> Help me lock in ONE build to finish. Ask me what's already
> half-done, what's closest to shippable, and what I'd actually be
> proud to post. Pick one for me, then break it into small nightly
> moves I can each do in 45 minutes. End by giving me tonight's single
> move so I can start right now.
> ```

**Nästa:** [Allt du behöver veta om terminalen](08-allt-om-terminalen.md) (frivillig fördjupning), eller direkt vidare till [Steg 1, Importera ditt minne från ChatGPT eller Gemini](../steg1/01-importera-minne.md)

Claude Code utvecklas snabbt. Det som stämmer idag kan vara förändrat
om några månader. Jag uppdaterar allt eftersom jag hinner och hittar
ny information.

---

**Skapat av [Lucy Sonberg](https://www.linkedin.com/in/lucysonberg)** · [GitHub](https://github.com/LucyVers)
Licensierat under [CC BY-NC-ND 4.0](../LICENSE). Dela gärna med kredit, hör av dig för kommersiell användning eller institutionell licensiering.