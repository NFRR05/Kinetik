# Progetto Landing Page: KINETIK Padel & Tennis Club

Documento di specifica definitivo per brand identity, architettura delle 11 sezioni, palette cromatica, typography system e layout visuale con linee guida geometriche del campo da padel.

---

## 1. Brand Identity & Logo Concept

- **Nome Brand**: **KINETIK** (Padel & Tennis Club)
- **Concept Logo**: Monogramma dinamico con lettera "K" geometrica integrata a freccia d'impatto (`>`) e pattern a 4 fori in colore Volt (`#D4FF00`) che richiamano lo *sweet spot* e la foratura aerodinamica della pala da padel.
- **Implementazione**: Vettoriale SVG ad alta definizione inserito inline in Navbar e Favicon.

---

## 2. Tipografia & Font Locali

I font sono archiviati ed elaborati localmente nella cartella `fonts/`:
- **Headings & Grandi Numeri**: **Clash Display** (`Regular`, `Medium`, `Semibold`, `Bold`) -> `fonts/ClashDisplay/`
- **Body Text, Tabelle, Badge & UI**: **Vercetti Regular** (`.woff2`, `.woff`, `.otf`, `.ttf`) -> `fonts/Vercetti/`

---

## 3. Palette Colori & Design Tokens

```css
:root {
  /* Toni Primari di Sfondo (Electric Court Theme) */
  --bg-court-deep: #0e2a47;        /* Blu campo profondo / base scura */
  --bg-court-vibrant: #1b6ca8;     /* Blu cobalto campo centrale */
  --bg-court-electric: #2e88d6;    /* Blu elettrico highlights */
  --bg-sky-light: #7cb9e8;         /* Azzurro ghiaccio sfumature */

  /* Tipografia */
  --text-primary: #ffffff;         /* Bianco puro per titoli e CTA */
  --text-secondary: rgba(255, 255, 255, 0.75); /* Testo di supporto */
  --text-muted: rgba(255, 255, 255, 0.45);     /* Note legali / breadcrumbs */

  /* Accenti & Interattività */
  --accent-ball-volt: #d4ff00;     /* Giallo/Verde fluo pallina (CTA primaria / badges) */
  --accent-volt-hover: #ffffff;    /* Hover stato: transizione bianca a espansione da top-left */
  
  /* Componenti Glassmorphism */
  --card-glass-bg: rgba(14, 42, 71, 0.65);
  --card-glass-border: rgba(255, 255, 255, 0.18);
  --card-glass-blur: 16px;

  /* Linee Guida Campo da Padel (Background Overlay) */
  --court-line-color: rgba(255, 255, 255, 0.08); /* Linea sottile 2px */
  --court-line-accent: rgba(212, 255, 0, 0.15);  /* Linea servizio / punti chiave */
}

/* ==========================================================================
   REGOLA DI BRANDING GLOBALE: BOTTONI & HOVER INTERACTIVE STATE
   ==========================================================================
   1. Stato Default: Sfondo Verde Volt (#D4FF00), Testo Dark Navy (#091A30), border-radius: 8px.
   2. Stato Hover (Regola Ufficiale di Brand):
      - Espansione circolare/radiale bianca (#FFFFFF) con origine nell'angolo in alto a sinistra (top-left / 0% 0%).
      - Transizione fluida in clip-path: circle(150% at 0% 0%) con curva cubic-bezier.
      - Testo sovrastante: Dark Navy (#091A30) per garantire contrasto e perfetta leggibilità sia su Volt che su Bianco.
   ========================================================================== */

```

---

## 4. Visual Background Guide: Linee Campo da Padel (2px Overlay)

La landing page include una struttura di sfondo geometrica continua a linee sottili (2px) ispirata alle dimensioni regolamentari di un **Campo da Padel (10m x 20m)**:
- **Perimetro Esterno & Gabbia/Vetri**: Linee perimetrali continue a bordo pagina che incorniciano le sezioni.
- **Rete Centrale (Net Line)**: Linea orizzontale mediana con pattern a micro-tratteggio che separa i macro-blocchi.
- **Linee di Servizio (6.95m)** e **Linea Centrale di Battuta (T)**: Fanno da guide di allineamento per le card, i container e le sezioni di pricing/campi.
- **Resa Visiva**: L'overlay rimane discreto in trasparenza (`opacity: 0.08 - 0.15`) durante lo scroll, dando un effetto blueprint tecnico-architettonico senza disturbare la leggibilità del contenuto.

---

## 5. Architettura delle Informazioni e Contenuti (Senza Vincoli di Layout)

Di seguito la specifica dei contenuti, dati richiesti e azioni per ciascuna sezione, affiancata dai termini di ricerca per piattaforme di design (Dribbble, Framer, Awwwards, Mobbin).

---

### Sezione 1: Header / Navigation
* **Contenuto**: Logo KINETIK, menù di navigazione (Campi, Academy, Tariffe, Community, Servizi, Contatti), stato club (aperto/chiuso, orari attuali).
* **Azioni / Dati**: CTA primaria di prenotazione, selettore lingua/info rapide.
* **Query di Ricerca (Dribbble / Framer)**:
  * `modern sticky navigation bar`
  * `sports club header glassmorphism`
  * `minimal navigation menu with cta`

---

### Sezione 2: Hero & Value Proposition
* **Contenuto**: Headline ad alto impatto (posizionamento del club), sub-headline descrittiva della struttura (indoor, campi professionali, tecnologia), micro-dati in evidenza (numero campi, disponibilità live, valutazione media).
* **Azioni / Dati**: CTA primaria (Prenota un campo), CTA secondaria (Scopri i corsi o Esplora il club).
* **Query di Ricerca (Dribbble / Framer)**:
  * `sports landing page hero section`
  * `fitness club hero split screen`
  * `bold typography hero web design`
  * `dark sports web hero banner`

---

### Sezione 3: Trust & Key Metrics (Statistiche / Highlights)
* **Contenuto**: 4-5 metriche quantitative chiave del club (es. numero campi panoramici, metri d'altezza indoor, numero maestri certificati, ore di apertura settimanali, posti auto).
* **Azioni / Dati**: Nessuna interazione complessa, solo dati numerici e relative etichette di valore.
* **Query di Ricerca (Dribbble / Framer)**:
  * `stats counter section ui`
  * `feature numbers metrics grid`
  * `trust indicators bento bar`

---

### Sezione 4: Campi & Specifiche Struttura
* **Contenuto**: Schede informative per tipologia campo (Padel Panoramico vs Tennis Resina/Terra), dettagli materiali (manto, vetri, illuminazione lux, altezza soffitto, climatizzazione).
* **Azioni / Dati**: Switcher/filtro tra Padel e Tennis, visualizzatore caratteristiche tecniche, CTA per verificare disponibilità oraria per quel tipo di campo.
* **Query di Ricerca (Dribbble / Framer)**:
  * `interactive product specs section`
  * `facility showcase tabs ui`
  * `court booking features comparison`
  * `interactive bento grid features`

---

### Sezione 5: Academy & Coaching
* **Contenuto**: Catalogo programmi formativi suddivisi per target (Junior Academy, Corsi Adulti per livelli, Lezioni Private/Intensive), profili sintetici dei coach o qualifiche federali.
* **Azioni / Dati**: Scheda corso con durata, frequenza e livello; CTA per richiedere prova gratuita o assessment di livello.
* **Query di Ricerca (Dribbble / Framer)**:
  * `course curriculum cards ui`
  * `sports academy coaching packages`
  * `pricing cards tier coaching`
  * `trainer profiles section`

---

### Sezione 6: Community, Matchmaking & Tornei
* **Contenuto**: Sistema per trovare compagni di gioco / quarto giocatore (diviso per ranking/livello), calendario prossimi eventi e tornei amatoriali/sociali.
* **Azioni / Dati**: Link diretto a gruppi WhatsApp di livello, pulsante iscrizione torneo con deadline e posti rimanenti.
* **Query di Ricerca (Dribbble / Framer)**:
  * `community hub section ui`
  * `tournament schedule timeline`
  * `matchmaking sports app web interface`
  * `events calendar list ui`

---

### Sezione 7: Tariffe, Fasce Orarie & Noleggio
* **Contenuto**: Listino prezzi diviso per fascia (Peak / Off-Peak / Weekend), costi noleggio attrezzatura (racchette test, palline), opzioni tesseramento/carnet.
* **Azioni / Dati**: Calcolatore quota singola a persona (split per 4 giocatori), selettore fascia oraria, CTA diretta di prenotazione slot.
* **Query di Ricerca (Dribbble / Framer)**:
  * `pricing table with toggle calculator`
  * `split cost pricing widget ui`
  * `sports court booking rate table`

---

### Sezione 8: Club House & Servizi Accessori
* **Contenuto**: Elenco servizi complementari (Bistrot/Sport Bar per terzo tempo, Pro Shop con servizio incordatura, Spogliatoi con area relax/sauna, Parcheggio).
* **Azioni / Dati**: Orari di apertura specifici dei servizi, menu/servizi del pro shop.
* **Query di Ricerca (Dribbble / Framer)**:
  * `amenities grid lifestyle ui`
  * `hotel club facilities showcase`
  * `bento grid services dark theme`

---

### Sezione 9: Social Proof & Recensioni
* **Contenuto**: Testimonianze reali di giocatori e allievi dell'academy, voto medio aggregato (Google / Playtomic), badge di certificazione o partnership.
* **Azioni / Dati**: Filtro o navigazione tra recensioni padel/tennis, link alla pagina recensioni completa.
* **Query di Ricerca (Dribbble / Framer)**:
  * `testimonials carousel ui modern`
  * `review cards grid social proof`
  * `customer feedback dark mode ui`

---

### Sezione 10: Location, Orari & Contatti
* **Contenuto**: Indirizzo esatto, indicazioni stradali/accesso parcheggio, orari segreteria e campi, recapiti diretti (telefono, email, chat rapida).
* **Azioni / Dati**: Mappa interattiva, link rapido per avviare navigatore GPS (Google Maps / Apple Maps), bottone contatto WhatsApp rapido.
* **Query di Ricerca (Dribbble / Framer)**:
  * `contact section with map dark mode`
  * `location details card ui`
  * `footer contact bento box`

---

### Sezione 11: Footer
* **Contenuto**: Ragione sociale, P.IVA, note legali, link a Privacy & Cookie Policy, orari riassuntivi, scorciatoie di navigazione, link download app collegate.
* **Azioni / Dati**: Iscrizione newsletter/aggiornamenti tornei, link social media.
* **Query di Ricerca (Dribbble / Framer)**:
  * `modern sitemap footer dark`
  * `mega footer web design`
  * `minimal sports website footer`

---

## 6. Assets del Progetto

- Immagini e video: `assets/` (incluso `assets/img-player-no-bg.png` e `assets/hero.jpeg`).
- Font locali: `fonts/ClashDisplay/` e `fonts/Vercetti/`.
