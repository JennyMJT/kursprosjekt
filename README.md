# AI Markedsføringsassistent (AI Marketing Campaign Manager)

Final project for the Building AI course

## Summary

Dette prosjektet er et AI-drevet verktøy som automatiserer og strukturerer markedsavdelingens arbeidshverdag. Løsningen gir en komplett oversikt over årets markedsaktiviteter, bryter kampanjer ned i konkrete oppgaver, delegerer disse til teammedlemmer, følger opp progresjon, og dytter til slutt ferdig innhold ut som utkast til sosiale medier og nettsider.

## Background
![image of an online cat](https://tinyurl.com/elementsofaicat)
![image of a cat](/cat_image.jpg)


Markedsføring i dag krever koordinering på tvers av mange kanaler, systemer og mennesker. Ofte forsvinner mye verdifull tid i manuelt administrativt arbeid. Dette prosjektet løser flere utfordringer:

* **Mangel på helhetlig oversikt:** Det er vanskelig å se sammenhengen mellom årets store kampanjer og de daglige oppgavene.
* **Tidkrevende delegering og oppfølging:** Å manuelt tildele oppgaver og mase om statusrapporter fra teamet tar tid fra kreativt arbeid.
* **Flaskehalser ved publisering:** Når innhold er ferdig, kreves det fortsatt manuelt arbeid for å logge inn i ulike plattformer (SoMe, CMS) for å opprette utkast.

Motivasjonen bak prosjektet er å la AI ta seg av prosjektledelsen og det rutinemessige, slik at markedsføringsteamet kan fokusere på kreativitet og strategi.

## How is it used?

Løsningen er tenkt brukt daglig av markedsavdelingen, fra markedssjef til innholdsprodusenter. 

**Prosess:**
1. **Planlegging:** Markedssjefen mater systemet med årets mål, budsjetter og merkedager. AI-en foreslår en markedsplan for året.
2. **Delegering:** AI-en bryter markedsplanen ned til spesifikke oppgaver (f.eks. "Skriv blogginnlegg om produkt X", "Lag grafikk for Instagram") og tildeler disse til riktig person i teamet basert på rolle og kapasitet.
3. **Oppfølging:** Systemet har et dashboard som viser progresjon. AI-en kan sende vennlige påminnelser i kanaler som Slack/Teams hvis en frist nærmer seg.
4. **Automatisert utkast:** Når en tekst eller et bilde er markert som ferdig i systemet, bruker AI-en API-integrasjoner til å automatisk opprette et upublisert utkast direkte på nettsiden (f.eks. WordPress) og i sosiale medie-kanaler (Meta, LinkedIn). Alt er klart for en siste menneskelig godkjenning ("Human-in-the-loop").

## Data sources and AI methods

Dataene prosjektet bygger på vil være en kombinasjon av intern bedriftsdata og eksterne API-er:

* **Inndata:** Bedriftens historiske markedsplaner, merkevare-retningslinjer (Tone of Voice), og team-informasjon.
* **AI-metoder:** * *Natural Language Processing (NLP):* Bruk av store språkmodeller (LLMs som GPT-4) for å forstå oppgavebeskrivelser, trekke ut essens, og eventuelt hjelpe til med tekstgenerering/tilpasning for ulike plattformer.
  * *Regelbasert planlegging/Maskinlæring:* For å optimalisere tidspunkt for oppgaver og publisering.
* **Integrasjoner (API):** Løsningen er avhengig av toveis-kommunikasjon med eksisterende verktøy. For eksempel:
  * [Slack API / Microsoft Teams API](https://api.slack.com/) for varslinger.
  * [WordPress REST API](https://developer.wordpress.org/rest-api/) for publisering av nettsideutkast.
  * [LinkedIn Marketing API](https://learn.microsoft.com/en-us/linkedin/marketing/) for sosiale medier.

## Challenges

Dette prosjektet løser *ikke* den overordnede kreative strategien. AI-en kan organisere og optimalisere, men bedriften trenger fortsatt mennesker til å bestemme retningen og produsere det faktiske kvalitetsinnholdet.

**Begrensninger og etiske hensyn:**
* **Hallusinasjoner:** Språkmodeller kan misforstå instrukser og delegere oppgaver feil, eller skrive feil i utkastene.
* **Menneskelig kontroll:** Det er kritisk at systemet kun lager *utkast* og ikke publiserer noe automatisk. Vi må unngå at AI-en publiserer upassende innhold på vegne av merkevaren.
* **Personvern (GDPR):** Systemet vil behandle data om ansattes ytelse (hvem som fullfører oppgaver når). Dette krever at man er bevisst på hvordan denne dataen brukes, slik at det ikke blir et overvåkningsverktøy.

## What next?

Neste naturlige steg for prosjektet vil være å integrere **analytikk (feedback loop)**. Ved å hente inn data fra Google Analytics og SoMe-innsikt etter at noe er publisert, kan AI-en lære hvilke typer kampanjer som fungerte best, og automatisk justere forslagene til markedsplanen for neste kvartal. 

For å ta prosjektet videre trengs det spisskompetanse innen:
* API-arkitektur og integrasjoner (Backend-utvikling).
* Prompt engineering (finjustering av AI-modellen til å forstå markedsføringskontekst).
* UX/UI-design for å lage et intuitivt dashboard for teamet.

## Acknowledgments

* Takk til [Building AI](https://buildingai.elementsofai.com/) (Reaktor & University of Helsinki) for inspirasjon og rammeverk til prosjektet.
* Utkast- og språkfunksjoner er konseptualisert ved bruk av teknologier tilsvarende OpenAI sine språkmodeller.
