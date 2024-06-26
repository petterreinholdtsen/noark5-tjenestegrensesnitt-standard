Orientering og introduksjon
===========================

Historikk og status
-------------------

Noark
-----

Noark – Norsk arkivstandard – ble utarbeidet som kravspesifikasjon for
elektroniske journalsystemer i statsforvaltningen, og etablerte seg
raskt som en de facto standard, forvaltet av Riksarkivet. Kommunal
sektor utarbeidet en tilsvarende kravspesifikasjon – Koark.
Spesifikasjonene i Koark ble innlemmet i Noark-4, og da arkivforskriften
trådte i kraft ble det obligatorisk for offentlig forvaltning å benytte
et Noark-basert system for elektronisk journalføring.

Gjeldende standard – Noark 5 skal benyttes for all elektronisk
arkivdanning – også fagsystemer med saksbehandling.

Noark tjenestegrensesnitt
-------------------------

Noark 5-tjenestegrensesnittet (API) er en spesifikasjon av en dataprotokoll for
maskinell kommunikasjon med Noark-løsninger. Formålet er å standardisere og
forenkle kommunikasjonen mellom de ulike systemene i forvaltningen.

Et utvidet standardisert grensesnitt vil legge til rette for gode,
sammenhengende tjenester på tvers av virksomhetsgrensene i offentlig sektor.
De ulike leverandørene behøver ikke utvide tjenestene, eller benytte egne grensesnitt.

Prosjekt for Noark 5 tjenestegrensesnitt
----------------------------------------

Prosjekt for Noark 5 Tjenestegrensesnitt ble satt i gang av Riksarkivet
og Kommunenes Sentralforbund høsten 2013, og et forslag til spesifikasjon
overlevert fra Samdok-prosjektet i september 2016 som en betaversjon.

Sommeren 2017 innledet Arkivverket og Arkitektum AS (som utviklet betaversjonen)
et samarbeid med Fredrikstad kommune, Evry og HK Data om å kjøre en pilot (Proof
of Concept) for å verifisere betaversjonen.

I forbindelse med ferdigstilling av Noark 5.5.0 ble det også besluttet at
tjenestegrensesnittet skulle videreutvikles og forbedres. Prosjektet hadde oppstart
høsten 2018 og ny versjon skulle foreligge sommeren 2019. Det ble besluttet at
spesifikasjonen og alle åpne saker skulle publiseres på GitHub. Prosessen med og
diskusjonen rundt det å videreutvikle tjenestegrensesnittet ble dermed åpent
tilgjengelig for alle interesserte.

Vi takket samtidig ja til invitasjon til samarbeid med NUUG ved Petter Reinholdtsen
og OsloMet ved Thomas Sødring. De har testet Nikita mot tjenestegrensesnittets
betaversjon samt versjon 1.0 og 1.1. Denne testingen har resultert i mange nyttige
innspill og gode eksempler.

.. _prosjektets-hovedmal:

Prosjektets hovedmål
--------------------

Mandatet for prosjektet i Samdok var:

-  å etablere en plattformuavhengig informasjonsmodell i UML for
   arkivstrukturen i Noark 5
-  å definere CRUD tjenester (Create, Read, Update, Delete) for
   objektene i informasjonsmodellen

Mål og begrunnelse var videre:

-  sammen med arkivleverandørindustrien å utvikle og levere et
   tjenestegrensesnitt for Noark 5 som implementeres som et krav i
   Noark-standarden, forvaltes av Riksarkivet og benyttes av
   fagløsninger uavhengig av leverandør. Prosjektet skal også levere
   et forslag til opplegg for test og godkjenning. Prosjektet skal
   videre bidra til å skape en arena der leverandørindustrien og
   bestillerne kan møtes og diskutere behov og utfordringer.

-  Et standardisert Noark 5 tjenestegrensesnitt skal bidra til gode,
   sammenhengende digitale tjenester på tvers av virksomhetsgrensene i
   offentlig sektor, støtte opp under offentlige virksomheters ønske om
   leverandøruavhengighet, samt fremme digitalisering og gi bedre
   tjenester.

I forbindelse med ferdigstilling av Noark 5.5.0 ble det besluttet at
tjenestegrenesnittet skulle videreutvikles, og få inn endringer som var
etterspurt etter betalanseringen.

Prosjektets organisering
------------------------

Prosjekteier: Arkivverket

Prosjektgruppen har bestått av:

-  Arkivverket ved Øyvind Kruse, Hans Fredrik Berg, Mona Danielsen og
   Anne Sofie Knutsen.
-  Leverandør til prosjektet har vært Arkitektum AS
-  Piloter:

   -  Fredrikstad kommune i samarbeid med Evry og HK Data
   -  NUUG ved Petter Reinholdtsen (Nikita)
   -  OsloMet ved Thomas Sødring (Nikita)

Noark leverandører er blitt informert og involvert i prosjektet, og har via
GitHub hatt mulighet til følge med og bidra underveis i videreutviklingen
av tjenestegrensesnittet.

Fra 2020-02-03 består redaksjon for spesifikasjonen av Mona Danielsen,
Anne Sofie Knutsen, Thomas Sødring og Petter Reinholdtsen.

Denne spesifikasjonen faller inn under unntakene i den norske
åndsverkslovens § 14[1]_, og er ikke opphavsrettslig vernet.

.. [1] «Lover, forskrifter, rettsavgjørelser og andre vedtak av
       offentlig myndighet er uten vern etter denne loven. Det samme
       gjelder forslag, utredninger, uttalelser og lignende som
       gjelder offentlig myndighetsutøvelse, og er avgitt av
       offentlig myndighet, offentlig oppnevnt råd eller utvalg,
       eller utgitt av det offentlige. Tilsvarende er offisielle
       oversettelser av slike tekster uten vern etter denne loven.»

Endringslogg for dette dokumentet
---------------------------------


Version 1.1 10.6.2023
~~~~~~~~~~~~~~~~~~~~~

Utført av Anne S Knutsen, Mona Danielsen, Petter Reinholdtsen, Thomas
Sødring.

Funksjonelle endringer:

 * Korrigert beskrevet relasjon mellom Registrering og
   Korrespondansepart til å samsvare med N5 [0..\*].
 * Korrigert til konsistent bruk av https i alle relasjonsnøkler.
 * Lagt inn relasjon mellom Dokumentbeskrivelse og Part, avglemt i
   overgang til Noark 5.5.
 * Korrigert feil relasjonsnøkkel til ny-journalpost for mappe.
 * Korrigerte relasjonsnøkler for Korrespondansepart og Part som
   resultat av tidligere overføring til Registrering og Mappe.
 * Korrigert skrivefeil i relasjonsnøkkellisten for Klasse.
 * Korrigert all bruk av date til datetime for samkjøring med
   oppdatering i Noark 5.
 * Korrigerte Matrikkel-typer fra 'string' til 'integer', for å
   være i tråd med Kartverkets SOSI-standard.
 * Fjernet redundant relasjonstype NoteLink fra Dokumentbeskrivelse.
 * La inn attributt gradering til Klasse, avglemt ved overgang til
   Noark 5.5.
 * Endret kode for PartRolle-oppføring Pårørende fra PÅ til PAA
   for å la alle kodeverdier være ASCII.
 * Klargjorde at attributtene format, konvertertFraFormat og
   konvertertTilFormat bruker samme vokabular fra
   Format-kodelisten.
 * Klargjorde hvilken formatkode som skal brukes for ukjente
   formater.
 * Korrigerte PRONOM-koder brukt i eksempler.
 * Fastsatte HTTP-returkode 200 for søk uten resultat.
 * Definerte kodeverdier og justerte kodenavn for den åpne
   kodelisten Hendelsetype.
 * Korrigerte relasjoner for Endringslogg og Hendelseslogg.
 * Endret atributt oppdatertDato og oppdatertAv til endretDato
   endretAv for konsistens med Noark 5 endringslogg.xsd.
 * Korrigerte manglende relasjonsnøkler til
   virksomhetsspesifikkeMetadata-kodelisten.
 * Korrigerte gjenglemte relasjonsnøkler for å opprette
   kodelisteverdier.
 * La til nytt tillegg med beskrivelse hva som menes med blanke tegn.
 * Introduserte notasjon for forkomstkrav ved oppretting og
   uthenting, der dette er forskjellig.
 * Korrigerte manglende relasjosnnøkkel til Koordinatsystem i
   kodelisteoversikten.
 * Korrigerte forekomst for Skjerming.SkjermingMetadata fra [0..\*]
   til [1..\*] for samkjøring med Noark 5 og XSD.
 * Fjernet feilplasserte ny-\*-relasjonsnøkler på instanser som
   ikke kan være foreldre til instans av samme type.
 * Korrigerte flere OData-eksempler.
 * Fastsatte standardiserte protokollversjonsnummer for
   system-endepunktet.
 * Fjernet mappetype-attributt fra Mappe, som ikke har tilsvarende
   felt i Noark 5.
 * Samkjørte attributtnavn inaktiv og utdatert samt endret type
   til dato for samkjøring med metadatabeskrivelser i N5-gitdepot.
 * Utvidet filopplastingsprosess til å tillate opplasting direkte
   fra dokumentbeskrivelse uten forutgående oppretting av
   dokumentobjekt-instans.
 * Oppdaterte UML-diagrammer til å inkludere flere relevante
   relasjoner.
 * Forbedret tekstlige beskrivelser og eksempler samt korrigerte
   skrivefeil i tekst og tabeller.
 * Reformulerte 'åpen kodeliste' til å forklare hva det betyr.
 * Gjorde det klart at journalstatus er en åpen kodeliste.

Detaljert historikk over endringer i spesifikasjonen kan hentes
ut av git-depotet (se kapittel 2).

Versjon 1.0 4.7.2019
~~~~~~~~~~~~~~~~~~~~~~

Utført av Anne S Knutsen og Mona Danielsen

Detaljert historikk over endringer i spesifikasjonen kan hentes ut av
git-depotet (se kapittel 2).
