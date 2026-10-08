<meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#faf9f5;color:#141413}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style>
<title>Nicolas Wylock</title>
<style>
/* Concept: an application file. Identity card beside the hero, sections on alternating grounds,
   channels in tabs with four constant headings (professionalism, best practices, techniques, program rules). */
:root {
  --bg: #F5F8FA;
  --surface: #FFFFFF;
  --alt: #EAF0F4;
  --ink: #0F1E2E;
  --muted: #4F5E6D;
  --line: #D6DFE6;
  --accent: #0B6B63;
  --on-accent: #FFFFFF;
  --accent-soft: #DCEFEB;
  --shadow: 0 1px 2px rgba(15, 30, 46, .06), 0 18px 40px -22px rgba(15, 30, 46, .28);

  --band: #0C2B2A;
  --band-ink: #EAF4F2;
  --band-muted: #A5C2BD;
  --band-line: #2A4A47;
  --band-accent: #7FDACB;

  --font-display: "Iowan Old Style", "Palatino Linotype", Palatino, "Book Antiqua", Georgia, serif;
  --font-body: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  --font-mono: ui-monospace, "SF Mono", Menlo, Consolas, "Liberation Mono", monospace;

  --r-lg: 20px;
  --r: 12px;
  --r-sm: 6px;
  --gutter: clamp(16px, 4vw, 40px);
  --max: 1120px;
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #0B151E;
    --surface: #111E29;
    --alt: #0E1923;
    --ink: #E7EEF4;
    --muted: #9DB0C0;
    --line: #24384A;
    --accent: #4CC3B3;
    --on-accent: #06201C;
    --accent-soft: #12332F;
    --shadow: 0 1px 2px rgba(0, 0, 0, .4), 0 18px 40px -22px rgba(0, 0, 0, .7);
    color-scheme: dark;
  }
}
:root[data-theme="dark"] {
  --bg: #0B151E;
  --surface: #111E29;
  --alt: #0E1923;
  --ink: #E7EEF4;
  --muted: #9DB0C0;
  --line: #24384A;
  --accent: #4CC3B3;
  --on-accent: #06201C;
  --accent-soft: #12332F;
  --shadow: 0 1px 2px rgba(0, 0, 0, .4), 0 18px 40px -22px rgba(0, 0, 0, .7);
  color-scheme: dark;
}

*, *::before, *::after { box-sizing: border-box; }
html { scroll-behavior: auto; }
@media (prefers-reduced-motion: no-preference) { html { scroll-behavior: smooth; } }
body {
  margin: 0;
  background: var(--bg);
  color: var(--ink);
  font-family: var(--font-body);
  font-size: 1rem;
  line-height: 1.65;
  -webkit-font-smoothing: antialiased;
}
h1, h2, h3, h4, p, ul, dl, dd, figure, blockquote { margin: 0; }
ul { padding: 0; list-style: none; }
a { color: inherit; }
:focus-visible { outline: 2px solid var(--accent); outline-offset: 3px; border-radius: 4px; }
section[id] { scroll-margin-top: 4.5rem; }
.sr { position: absolute; width: 1px; height: 1px; overflow: hidden; clip: rect(0 0 0 0); white-space: nowrap; }
.wrap { max-width: 1300px; margin-inline: auto; padding-inline: var(--gutter); }
.sec { padding-block: clamp(3.5rem, 8vw, 6.5rem); }
.sec--surface { background: var(--surface); border-block: 1px solid var(--line); }
.sec--alt { background: var(--alt); }
.grid > * { min-width: 0; }

/* Typography */
.label {
  font-family: var(--font-mono);
  font-size: .72rem;
  letter-spacing: .09em;
  text-transform: uppercase;
  color: var(--accent);
  font-weight: 600;
}
h1, h2, h3 { font-family: var(--font-display); font-weight: 600; letter-spacing: -.015em; text-wrap: balance; }
h1 { font-size: clamp(2.2rem, 5.2vw, 3.7rem); line-height: 1.07; letter-spacing: -.025em; }
h1 em { color: var(--accent); font-style: italic; }
h2 { font-size: clamp(1.75rem, 3.5vw, 2.55rem); line-height: 1.12; }
h3 { font-size: 1.3rem; line-height: 1.25; }
h4 { font-family: var(--font-body); font-size: .95rem; font-weight: 650; line-height: 1.3; }
.lead { font-size: 1.125rem; color: var(--muted); max-width: 58ch; }
.sec-head { max-width: 1300px; margin-bottom: clamp(2rem, 4vw, 3rem); display: grid; gap: .9rem; }
.sec-head p { color: var(--muted); max-width: 1300px; }
.ic { width: 1.25rem; height: 1.25rem; flex: none; fill: none; stroke: currentColor; stroke-width: 1.6; stroke-linecap: round; stroke-linejoin: round; }

/* Buttons */
.btn {
  display: inline-flex; align-items: center; justify-content: center; gap: .5rem;
  padding: .8rem 1.35rem; border-radius: 999px; border: 1px solid var(--accent);
  background: var(--accent); color: var(--on-accent);
  font: inherit; font-weight: 600; font-size: .95rem; text-decoration: none; cursor: pointer;
  transition: transform .15s ease, box-shadow .15s ease, background .15s ease;
}
.btn:hover { transform: translateY(-1px); box-shadow: var(--shadow); }
.btn--ghost { background: transparent; color: var(--ink); border-color: var(--line); }
.btn--ghost:hover { border-color: var(--accent); }
.btn--sm { padding: .5rem 1rem; font-size: .88rem; }

/* Navigation */
.nav { position: sticky; top: env(safe-area-inset-top, 0px); z-index: 20; background: var(--bg); border-bottom: 1px solid var(--line); }
.nav-in { display: flex; align-items: center; justify-content: space-between; gap: 1rem; min-height: 3.8rem; }
.brand { display: inline-flex; align-items: center; gap: .65rem; text-decoration: none; font-family: var(--font-display); font-weight: 600; font-size: 1.1rem; }
.mono-badge {
  display: grid; place-items: center; width: 2.1rem; height: 2.1rem; border-radius: 50%;
  border: 1.5px solid var(--accent); color: var(--accent);
  font-family: var(--font-mono); font-size: .72rem; font-weight: 700; letter-spacing: .02em;
}
.nav nav { display: none; gap: 1.4rem; }
.nav nav a { text-decoration: none; font-size: .9rem; color: var(--muted); padding-block: .3rem; border-bottom: 2px solid transparent; }
.nav nav a:hover { color: var(--ink); }
.nav nav a[aria-current="true"] { color: var(--ink); border-bottom-color: var(--accent); }
@media (min-width: 860px) { .nav nav { display: flex; } }

/* Hero */
.hero {
  padding-block: clamp(3rem, 7vw, 5.5rem);
  background: radial-gradient(900px 420px at 88% -10%, var(--accent-soft), transparent 70%), var(--bg);
}
.hero-grid { display: grid; gap: clamp(2rem, 5vw, 3.5rem); grid-template-columns: minmax(0, 1fr); align-items: start; }
@media (min-width: 960px) { .hero-grid { grid-template-columns: minmax(0, 1.2fr) minmax(0, .8fr); } }
.hero-copy { display: grid; gap: 1.5rem; }
.cta-row { display: flex; flex-wrap: wrap; gap: .75rem; }
.idea { display: grid; gap: .5rem; padding-top: 1.5rem; border-top: 1px solid var(--line); max-width: 56ch; }
.idea p { font-family: var(--font-display); font-size: 1.15rem; line-height: 1.5; }

.id-card { background: var(--surface); border: 1px solid var(--line); border-radius: var(--r-lg); box-shadow: var(--shadow); padding: clamp(1.25rem, 3vw, 1.75rem); display: grid; gap: 1.25rem; }
.id-top { display: flex; align-items: center; justify-content: space-between; gap: .75rem; flex-wrap: wrap; }
.pill { display: inline-flex; align-items: center; gap: .45rem; padding: .25rem .7rem; border-radius: 999px; background: var(--accent-soft); color: var(--accent); font-size: .78rem; font-weight: 600; }
.pill::before { content: ""; width: .45rem; height: .45rem; border-radius: 50%; background: var(--accent); }
.id-person { display: flex; align-items: center; gap: 1rem; }
.avatar { display: grid; place-items: center; width: 3.6rem; height: 3.6rem; border-radius: 50%; background: var(--accent); color: var(--on-accent); font-family: var(--font-display); font-size: 1.35rem; font-weight: 600; flex: none; }
.id-person h2 { font-size: 1.4rem; }
.id-person p { color: var(--muted); font-size: .92rem; }
.id-list { display: grid; gap: 0; border-block: 1px solid var(--line); }
.id-list div { display: grid; grid-template-columns: 5.5rem minmax(0, 1fr); gap: .75rem; padding-block: .7rem; }
.id-list div + div { border-top: 1px dashed var(--line); }
.id-list dt { font-family: var(--font-mono); font-size: .7rem; letter-spacing: .08em; text-transform: uppercase; color: var(--muted); padding-top: .2rem; }
.id-list dd { font-size: .93rem; }
.id-card h3 { font-family: var(--font-mono); font-size: .72rem; letter-spacing: .09em; text-transform: uppercase; color: var(--accent); font-weight: 600; }
.checks { display: grid; gap: .55rem; margin-top: .6rem; }
.checks li { position: relative; padding-left: 1.6rem; font-size: .92rem; }
.checks li::before { content: ""; position: absolute; left: .3rem; top: .32em; width: .38rem; height: .72rem; border: solid var(--accent); border-width: 0 2px 2px 0; transform: rotate(45deg); }

/* Principles */
.principles { display: grid; grid-template-columns: minmax(0, 1fr); gap: 1.5rem; }
@media (min-width: 640px) { .principles { grid-template-columns: repeat(2, minmax(0, 1fr)); } }
@media (min-width: 1000px) { .principles { grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 2rem; } }
.principle { display: grid; gap: .6rem; align-content: start; }
.principle .ic { color: var(--accent); width: 1.6rem; height: 1.6rem; }
.principle p { color: var(--muted); font-size: .93rem; }

/* Generic cards */
.card { background: var(--surface); border: 1px solid var(--line); border-radius: var(--r); padding: clamp(1.25rem, 3vw, 1.75rem); display: grid; gap: 1rem; align-content: start; }
.card p { color: var(--muted); font-size: .95rem; }
.tags { display: flex; flex-wrap: wrap; gap: .5rem; }
.tag { border: 1px solid var(--line); background: var(--bg); border-radius: 999px; padding: .3rem .8rem; font-size: .84rem; }
.ticks { display: grid; gap: .55rem; }
.ticks li { position: relative; padding-left: 1.2rem; font-size: .93rem; }
.ticks li::before { content: ""; position: absolute; left: 0; top: .6em; width: .45rem; height: .45rem; border-radius: 1px; background: var(--accent); }

/* Services */
.services { display: grid; gap: 1.25rem; grid-template-columns: minmax(0, 1fr); }
@media (min-width: 640px) { .services { grid-template-columns: repeat(2, minmax(0, 1fr)); } .services .criteria { grid-column: 1 / -1; } }
@media (min-width: 1000px) { .services { grid-template-columns: repeat(3, minmax(0, 1fr)); } .services .criteria { grid-column: auto; } }
.card .kicker { font-family: var(--font-mono); font-size: .7rem; letter-spacing: .09em; text-transform: uppercase; color: var(--muted); }
.criteria { background: var(--accent-soft); border-color: transparent; }
.criteria .ticks li { color: var(--ink); }

/* Channels */
.tabs { display: grid; gap: 1.5rem; grid-template-columns: minmax(0, 1fr); }
@media (min-width: 900px) { .tabs { grid-template-columns: 15rem minmax(0, 1fr); gap: 2rem; align-items: start; } }
[role="tablist"] { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: .5rem; }
@media (min-width: 900px) { [role="tablist"] { grid-template-columns: minmax(0, 1fr); gap: .35rem; position: sticky; top: calc(env(safe-area-inset-top, 0px) + 5rem); } }
[role="tab"] {
  display: grid; gap: .1rem; text-align: left; padding: .65rem .8rem; border-radius: var(--r-sm);
  border: 1px solid var(--line); background: var(--surface); color: var(--ink);
  font: inherit; font-weight: 600; font-size: .9rem; cursor: pointer; transition: background .15s ease, border-color .15s ease;
}
[role="tab"] .sub { display: none; font-family: var(--font-mono); font-size: .68rem; letter-spacing: .06em; text-transform: uppercase; font-weight: 500; color: var(--muted); }
@media (min-width: 900px) { [role="tab"] .sub { display: block; } [role="tab"] { padding: .8rem 1rem; } }
[role="tab"]:hover { border-color: var(--accent); }
[role="tab"][aria-selected="true"] { background: var(--accent); border-color: var(--accent); color: var(--on-accent); }
[role="tab"][aria-selected="true"] .sub { color: var(--on-accent); opacity: .85; }
.panel { background: var(--surface); border: 1px solid var(--line); border-radius: var(--r-lg); padding: clamp(1.25rem, 3vw, 2rem); display: grid; gap: 1.5rem; }
.panel:not([hidden]) { animation: panel-in .25s ease; }
@keyframes panel-in { from { opacity: .4; transform: translateY(4px); } to { opacity: 1; transform: none; } }
.panel-head { display: grid; gap: .5rem; }
.panel-head p { color: var(--muted); max-width: 56ch; }
.facets { display: grid; gap: 1rem; grid-template-columns: minmax(0, 1fr); }
@media (min-width: 700px) { .facets { grid-template-columns: repeat(2, minmax(0, 1fr)); } }
.facet { background: var(--bg); border: 1px solid var(--line); border-radius: var(--r); padding: 1.1rem 1.2rem 1.25rem; display: grid; gap: .8rem; align-content: start; min-width: 0; }
.facet h4 { display: flex; align-items: center; gap: .55rem; color: var(--accent); }
.facet--rules { background: var(--accent-soft); border-color: transparent; }
code { font-family: var(--font-mono); font-size: .85em; background: var(--alt); padding: .08em .35em; border-radius: 4px; }

/* Formats */
.formats { display: grid; gap: 1rem; grid-template-columns: minmax(0, 1fr); }
@media (min-width: 620px) { .formats { grid-template-columns: repeat(2, minmax(0, 1fr)); } }
@media (min-width: 1000px) { .formats { grid-template-columns: repeat(4, minmax(0, 1fr)); } }
.format { background: var(--bg); border: 1px solid var(--line); border-radius: var(--r); padding: 1.25rem; display: grid; gap: .65rem; align-content: start; }
.format .ic { width: 1.6rem; height: 1.6rem; color: var(--accent); }
.format p { color: var(--muted); font-size: .92rem; }
.format .kicker { font-family: var(--font-mono); font-size: .68rem; letter-spacing: .09em; text-transform: uppercase; color: var(--muted); margin-top: auto; padding-top: .3rem; }
.format--note { background: var(--accent-soft); border-color: transparent; }
.format--note h3 { font-size: 1.1rem; }
.matrix-block { margin-top: clamp(2rem, 5vw, 3.5rem); display: grid; gap: 1rem; }
.matrix-block h3 { font-size: 1.35rem; }
.scroll { overflow-x: auto; border: 1px solid var(--line); border-radius: var(--r); background: var(--surface); }
.matrix { width: 100%; min-width: 640px; border-collapse: collapse; font-size: .9rem; }
.matrix th, .matrix td { padding: .7rem .9rem; text-align: center; }
.matrix thead th { font-family: var(--font-mono); font-size: .68rem; letter-spacing: .07em; text-transform: uppercase; color: var(--muted); font-weight: 600; border-bottom: 1px solid var(--line); }
.matrix tbody th { text-align: left; font-weight: 600; white-space: nowrap; }
.matrix tbody tr + tr > * { border-top: 1px solid var(--line); }
.matrix td::before { content: ""; display: inline-block; vertical-align: middle; }
.matrix td.p::before { width: .7rem; height: .7rem; border-radius: 50%; background: var(--accent); }
.matrix td.s::before { width: .7rem; height: .7rem; border-radius: 50%; border: 2px solid var(--accent); }
.matrix td.n::before { width: .6rem; height: 2px; background: var(--line); }
.legend { display: flex; flex-wrap: wrap; gap: 1.25rem; font-size: .85rem; color: var(--muted); }
.legend span { display: inline-flex; align-items: center; gap: .5rem; }
.legend i { display: inline-block; width: .7rem; height: .7rem; border-radius: 50%; }
.legend .p { background: var(--accent); }
.legend .s { border: 2px solid var(--accent); }

/* Objections */
.objections { display: grid; gap: 1.25rem; grid-template-columns: minmax(0, 1fr); }
@media (min-width: 700px) { .objections { grid-template-columns: repeat(2, minmax(0, 1fr)); } }
@media (min-width: 1040px) { .objections { grid-template-columns: repeat(3, minmax(0, 1fr)); } }
.objection { background: var(--surface); border: 1px solid var(--line); border-radius: var(--r-sm); padding: 1.4rem; display: grid; gap: .9rem; align-content: start; }
.objection q { quotes: none; font-family: var(--font-display); font-style: italic; font-size: 1.15rem; line-height: 1.35; display: block; }
.objection .answer { border-top: 1px solid var(--line); padding-top: .9rem; display: grid; gap: .4rem; }
.objection .answer p { color: var(--muted); font-size: .93rem; }
.objection .label { color: var(--muted); }

/* FAQ */
.faq-grid { display: grid; gap: 2rem; grid-template-columns: minmax(0, 1fr); }
@media (min-width: 900px) { .faq-grid { grid-template-columns: minmax(0, .8fr) minmax(0, 1.2fr); gap: 3.5rem; } }
.faq-grid .sec-head { margin-bottom: 0; }
.faq { border-top: 1px solid var(--line); }
.faq details { border-bottom: 1px solid var(--line); }
.faq summary { list-style: none; cursor: pointer; display: flex; justify-content: space-between; align-items: center; gap: 1rem; padding: 1.15rem 0; font-weight: 600; }
.faq summary::-webkit-details-marker { display: none; }
.faq summary::after { content: "+"; font-family: var(--font-mono); font-size: 1.2rem; color: var(--accent); flex: none; }
.faq details[open] summary::after { content: "\2212"; }
.faq details p { color: var(--muted); padding-bottom: 1.25rem; max-width: 60ch; }

/* Contact */
.contact { background: var(--band); color: var(--band-ink); padding-block: clamp(3.5rem, 8vw, 6rem); }
.contact-grid { display: grid; gap: 2.5rem; grid-template-columns: minmax(0, 1fr); align-items: start; }
@media (min-width: 900px) { .contact-grid { grid-template-columns: minmax(0, 1.1fr) minmax(0, .9fr); gap: 4rem; } }
.contact .label { color: var(--band-accent); }
.contact h2 { margin-top: .9rem; }
.contact .lead { color: var(--band-muted); margin-top: 1rem; }
.contact-box { border: 1px solid var(--band-line); border-radius: var(--r); padding: 1.5rem; display: grid; gap: 1rem; }
.contact-box h3 { font-family: var(--font-mono); font-size: .72rem; letter-spacing: .09em; text-transform: uppercase; color: var(--band-accent); font-weight: 600; }
.contact-box .ticks li { color: var(--band-ink); }
.contact-box .ticks li::before { background: var(--band-accent); }
.channels { display: flex; flex-wrap: wrap; gap: .5rem; }
.chip { border: 1px solid var(--band-line); border-radius: 999px; padding: .35rem .95rem; font-size: .88rem; color: var(--band-ink); text-decoration: none; }
a.chip { background: var(--band-accent); border-color: var(--band-accent); color: #06201C; font-weight: 600; }
.mail-row { display: flex; flex-wrap: wrap; align-items: center; gap: .75rem; }
.mail-row[hidden] { display: none; }
.mail-row code { background: transparent; color: var(--band-ink); font-size: .95rem; padding: 0; overflow-wrap: anywhere; }
.btn--band { background: var(--band-accent); border-color: var(--band-accent); color: #06201C; }

/* Footer */
.foot { background: var(--bg); border-top: 1px solid var(--line); padding-block: 2rem; }
.foot-in { display: flex; flex-wrap: wrap; justify-content: space-between; gap: 1rem; font-size: .85rem; color: var(--muted); }
.foot-in p { max-width: 62ch; }

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { animation: none !important; transition: none !important; }
}
</style>

<svg width="0" height="0" style="position:absolute" aria-hidden="true" focusable="false">
  <symbol id="i-pro" viewBox="0 0 24 24"><rect x="3" y="7" width="18" height="13" rx="2"/><path d="M9 7V5a2 2 0 0 1 2-2h2a2 2 0 0 1 2 2v2M3 13h18"/></symbol>
  <symbol id="i-best" viewBox="0 0 24 24"><path d="m12 3 2.6 5.3 5.9.9-4.3 4.1 1 5.8L12 16.3l-5.2 2.8 1-5.8L3.5 9.2l5.9-.9z"/></symbol>
  <symbol id="i-tech" viewBox="0 0 24 24"><path d="M4 6h8M16 6h4M4 12h3M11 12h9M4 18h6M14 18h6"/><circle cx="14" cy="6" r="2"/><circle cx="9" cy="12" r="2"/><circle cx="12" cy="18" r="2"/></symbol>
  <symbol id="i-rules" viewBox="0 0 24 24"><path d="M12 3 5 6v5c0 4.5 3 8 7 10 4-2 7-5.5 7-10V6z"/><path d="m9 12 2.2 2.2L15.5 10"/></symbol>
  <symbol id="i-compare" viewBox="0 0 24 24"><rect x="3" y="4" width="8" height="16" rx="1.5"/><rect x="13" y="4" width="8" height="16" rx="1.5"/><path d="M5.5 9h3M15.5 9h3M5.5 13h3M15.5 13h3"/></symbol>
  <symbol id="i-doc" viewBox="0 0 24 24"><path d="M6 3h8l4 4v14H6z"/><path d="M14 3v4h4M9 12h6M9 16h6"/></symbol>
  <symbol id="i-guide" viewBox="0 0 24 24"><circle cx="12" cy="12" r="9"/><path d="m15.5 8.5-2 5-5 2 2-5z"/></symbol>
  <symbol id="i-blog" viewBox="0 0 24 24"><path d="M4 20l1-4L16 5l3 3L8 19z"/><path d="m14 7 3 3"/></symbol>
  <symbol id="i-ebook" viewBox="0 0 24 24"><path d="M5 4h10a3 3 0 0 1 3 3v13H8a3 3 0 0 1-3-3z"/><path d="M5 17a3 3 0 0 1 3-3h10"/></symbol>
  <symbol id="i-case" viewBox="0 0 24 24"><circle cx="12" cy="12" r="9"/><circle cx="12" cy="12" r="5"/><circle cx="12" cy="12" r="1.2"/></symbol>
  <symbol id="i-video" viewBox="0 0 24 24"><rect x="3" y="5" width="18" height="14" rx="3"/><path d="m10.5 9.5 4 2.5-4 2.5z"/></symbol>
</svg>

<header class="nav">
  <div class="wrap nav-in">
    <a class="brand" href="#top"><span class="mono-badge" aria-hidden="true">NW</span>Nicolas Wylock</a>
    <nav aria-label="Page sections">
      <a href="#services">Services</a>
      <a href="#leviers">Channels</a>
      <a href="#formats">Formats</a>
      <a href="#objections">Objections</a>
      <a href="#faq">FAQ</a>
    </nav>
    <a class="btn btn--sm" href="#contact">Contact me</a>
  </div>
</header>

<main>
<section class="hero" id="top">
  <div class="wrap hero-grid grid">
    <div class="hero-copy">
      <p class="label">Independent B2B affiliate · Belgium</p>
      <h1>B2B affiliate marketing, run with method and <em>by the rules</em>.</h1>
      <p class="lead">I'm Nicolas Wylock. I recommend SaaS, software and recruitment services to business decision-makers across six channels, applying the terms of every affiliate program to the letter.</p>
      <div class="cta-row">
        <a class="btn" href="#contact">Propose a program</a>
        <a class="btn btn--ghost" href="#leviers">See my method</a>
      </div>
      <div class="idea">
        <span class="label">The idea</span>
        <p>A recommendation that is documented, disclosed as affiliate and compliant with the program's rules serves the buyer and the brand alike. That is what makes an affiliate relationship last.</p>
      </div>
    </div>

    <aside class="id-card" aria-label="Affiliate profile">
      <div class="id-top">
        <span class="label">Affiliate profile</span>
        <span class="pill">B2B programs: open to applications</span>
      </div>
      <div class="id-person">
        <div class="avatar" aria-hidden="true">NW</div>
        <div>
          <h2>Nicolas Wylock</h2>
          <p>38 years old · Belgium</p>
        </div>
      </div>
      <dl class="id-list">
        <div><dt>Status</dt><dd>Independent B2B affiliate</dd></div>
        <div><dt>Offers</dt><dd>SaaS, software, recruitment services</dd></div>
        <div><dt>Channels</dt><dd>B2B cold email, SEO, X, LinkedIn, Instagram, Pinterest</dd></div>
        <div><dt>Formats</dt><dd>Comparisons, guides, ebooks, use cases, videos and more</dd></div>
      </dl>
      <div>
        <h3>My commitments</h3>
        <ul class="checks">
          <li>Affiliate disclosure visible before the first link</li>
          <li>One sub-ID per channel and per piece of content</li>
          <li>No bidding on your brand name</li>
          <li>Program terms re-read at every update</li>
        </ul>
      </div>
    </aside>
  </div>
</section>

<section class="sec sec--surface" aria-label="Working principles" style="padding-block: clamp(2.5rem, 5vw, 3.5rem);">
  <div class="wrap principles grid">
    <div class="principle"><svg class="ic" aria-hidden="true"><use href="#i-pro"/></svg><h4>Professionalism</h4><p>Clear identity, proofread content, measured claims.</p></div>
    <div class="principle"><svg class="ic" aria-hidden="true"><use href="#i-best"/></svg><h4>Best practices</h4><p>Buying intent first, one offer per message, regular updates.</p></div>
    <div class="principle"><svg class="ic" aria-hidden="true"><use href="#i-tech"/></svg><h4>Techniques</h4><p>Segmentation, testing, sub-IDs per channel and readable reporting.</p></div>
    <div class="principle"><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg><h4>Program rules</h4><p>Terms re-read, disclosure visible, no brand bidding.</p></div>
  </div>
</section>

<section class="sec sec--alt" id="services">
  <div class="wrap">
    <div class="sec-head">
      <span class="label">Promoted services</span>
      <h2>Offers that can be documented, compared and explained.</h2>
      <p>I focus on products and services a business buyer can evaluate on precise criteria: features, pricing, limits and support.</p>
    </div>
    <div class="services grid">
      <article class="card">
        <span class="kicker">Category 1</span>
        <h3>SaaS and software</h3>
        <p>For SMEs and teams comparing several solutions before they buy.</p>
        <div class="tags">
          <span class="tag">CRM and prospecting</span>
          <span class="tag">Marketing and email</span>
          <span class="tag">Project management</span>
          <span class="tag">Invoicing and accounting</span>
          <span class="tag">HR and payroll</span>
          <span class="tag">Automation</span>
        </div>
      </article>
      <article class="card">
        <span class="kicker">Category 2</span>
        <h3>Recruitment services</h3>
        <p>For companies looking for a partner that fits their need, sector and timeline.</p>
        <div class="tags">
          <span class="tag">Search firms and headhunting</span>
          <span class="tag">Job boards</span>
          <span class="tag">Specialist recruitment</span>
          <span class="tag">Temp staffing and contract work</span>
          <span class="tag">Recruitment outsourcing</span>
        </div>
      </article>
      <article class="card criteria">
        <span class="kicker">Before accepting a program</span>
        <h3>My criteria</h3>
        <ul class="ticks">
          <li>Written terms: commission, cookie duration, payment timing</li>
          <li>An offer I can document and compare honestly</li>
          <li>Explicit promotion rules: allowed channels, brand usage</li>
          <li>Resources and support provided by the brand</li>
          <li>A reputation that can be checked with its customers</li>
        </ul>
      </article>
    </div>
  </div>
</section>

<section class="sec" id="leviers">
  <div class="wrap">
    <div class="sec-head">
      <span class="label">Acquisition channels</span>
      <h2>Six channels, one standard.</h2>
      <p>Every channel follows the same frame: professional work, the channel's best practices, measurable techniques and compliance with the affiliate program's rules.</p>
    </div>

    <div class="tabs">
      <div role="tablist" aria-label="Acquisition channels">
        <button role="tab" id="tab-email" aria-controls="panel-email" aria-selected="true" tabindex="0">Cold email<span class="sub">Direct</span></button>
        <button role="tab" id="tab-seo" aria-controls="panel-seo" aria-selected="false" tabindex="-1">SEO<span class="sub">Organic</span></button>
        <button role="tab" id="tab-x" aria-controls="panel-x" aria-selected="false" tabindex="-1">X<span class="sub">Social</span></button>
        <button role="tab" id="tab-linkedin" aria-controls="panel-linkedin" aria-selected="false" tabindex="-1">LinkedIn<span class="sub">Professional social</span></button>
        <button role="tab" id="tab-instagram" aria-controls="panel-instagram" aria-selected="false" tabindex="-1">Instagram<span class="sub">Visual social</span></button>
        <button role="tab" id="tab-pinterest" aria-controls="panel-pinterest" aria-selected="false" tabindex="-1">Pinterest<span class="sub">Visual search</span></button>
      </div>

      <div>
        <!-- Cold email -->
        <div class="panel" role="tabpanel" id="panel-email" aria-labelledby="tab-email">
          <div class="panel-head">
            <h3>B2B cold email</h3>
            <p>Reach a decision-maker directly with a precise offer, only when the program allows it.</p>
          </div>
          <div class="facets">
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-pro"/></svg>Professionalism</h4><ul class="ticks">
              <li>Clearly identified sender: name, business, way to reply</li>
              <li>Proofread, restrained message, with no false promises or fake "Re:" subject lines</li>
              <li>Affiliate role stated from the first exchange</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-best"/></svg>Best practices</h4><ul class="ticks">
              <li>One offer per message, addressed to a specific job function</li>
              <li>Short, spaced-out sequence, stopped at the first reply or unsubscribe</li>
              <li>Dedicated sending domain, SPF, DKIM and DMARC in place, volume increased gradually</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-tech"/></svg>Techniques</h4><ul class="ticks">
              <li>Segmentation by business problem, company size and sector</li>
              <li>First line personalized from relevant, publicly available information</li>
              <li>A/B tests on subject line and call to action, dedicated tracking link per send</li></ul></div>
            <div class="facet facet--rules"><h4><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg>Program rules</h4><ul class="ticks">
              <li>Sending only if the program explicitly allows it in writing</li>
              <li>GDPR and ePrivacy rules respected, strictly professional targeting</li>
              <li>One-click unsubscribe, up-to-date suppression list, brand-approved materials</li></ul></div>
          </div>
        </div>

        <!-- SEO -->
        <div class="panel" role="tabpanel" id="panel-seo" aria-labelledby="tab-seo" hidden>
          <div class="panel-head">
            <h3>SEO</h3>
            <p>Capture buyers who are already comparing solutions and looking for a precise answer.</p>
          </div>
          <div class="facets">
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-pro"/></svg>Professionalism</h4><ul class="ticks">
              <li>Content written from documentation, hands-on tests and cited sources</li>
              <li>Visible update dates, prices re-checked</li>
              <li>Each solution's limits stated, including the cases where it is not a fit</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-best"/></svg>Best practices</h4><ul class="ticks">
              <li>Search intent first: compare, choose, implement</li>
              <li>Topic-based architecture, internal linking, one page per query</li>
              <li>Regular refresh of the pages that earn clicks</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-tech"/></svg>Techniques</h4><ul class="ticks">
              <li>Commercial-intent queries: alternative to, best tool for, pricing</li>
              <li>Structured data, page speed, mobile-friendly pages</li>
              <li>Page-by-page tracking of rankings and click-through rate</li></ul></div>
            <div class="facet facet--rules"><h4><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg>Program rules</h4><ul class="ticks">
              <li>No bidding on the brand name or its variants, unless agreed in writing</li>
              <li>Links tagged <code>rel="sponsored"</code>, affiliate disclosure before the first link</li>
              <li>No fake reviews or satellite pages, search engine guidelines respected</li></ul></div>
          </div>
        </div>

        <!-- X -->
        <div class="panel" role="tabpanel" id="panel-x" aria-labelledby="tab-x" hidden>
          <div class="panel-head">
            <h3>X (Twitter)</h3>
            <p>Share hands-on feedback and answer the questions of the moment, in a factual tone.</p>
          </div>
          <div class="facets">
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-pro"/></svg>Professionalism</h4><ul class="ticks">
              <li>Account in the business's name, factual tone, no controversy</li>
              <li>Careful replies, no pushiness, no promises of results</li>
              <li>Affiliation mentioned every time a link is shared</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-best"/></svg>Best practices</h4><ul class="ticks">
              <li>Educational threads, hands-on feedback, mini-comparisons</li>
              <li>Consistency over volume, one pinned resource</li>
              <li>Replies to real community questions, never mass messages</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-tech"/></svg>Techniques</h4><ul class="ticks">
              <li>Monitoring of "which tool for…" questions</li>
              <li>Screenshots, diagrams and concrete examples attached to threads</li>
              <li>One tracking link per post to see what is read and clicked</li></ul></div>
            <div class="facet facet--rules"><h4><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg>Program rules</h4><ul class="ticks">
              <li>#ad or "affiliate link" visible on every relevant post</li>
              <li>No automated replies, no bulk mentions</li>
              <li>Brand name and logo used according to the program's guidelines</li></ul></div>
          </div>
        </div>

        <!-- LinkedIn -->
        <div class="panel" role="tabpanel" id="panel-linkedin" aria-labelledby="tab-linkedin" hidden>
          <div class="panel-head">
            <h3>LinkedIn</h3>
            <p>Speak to decision-makers where they follow their industry, with useful, signed content.</p>
          </div>
          <div class="facets">
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-pro"/></svg>Professionalism</h4><ul class="ticks">
              <li>Real profile, clear positioning, no fake endorsements</li>
              <li>Signed, proofread posts, no exaggeration</li>
              <li>Private messages only after an exchange or at the person's request</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-best"/></svg>Best practices</h4><ul class="ticks">
              <li>Use cases and hands-on feedback rather than feature lists</li>
              <li>PDF carousels, articles and a newsletter for longer content</li>
              <li>Useful comments under industry posts</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-tech"/></svg>Techniques</h4><ul class="ticks">
              <li>Content matched to the decision stage: discovery, comparison, choice</li>
              <li>Ebooks and studies targeted by job function and sector</li>
              <li>Click tracking by post format</li></ul></div>
            <div class="facet facet--rules"><h4><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg>Program rules</h4><ul class="ticks">
              <li>Affiliate disclosure in the text of the post</li>
              <li>No automation or data-extraction tools that go against the platform's terms</li>
              <li>No bulk messages containing an affiliate link</li></ul></div>
          </div>
        </div>

        <!-- Instagram -->
        <div class="panel" role="tabpanel" id="panel-instagram" aria-labelledby="tab-instagram" hidden>
          <div class="panel-head">
            <h3>Instagram</h3>
            <p>Show a tool in action, in short formats, with a restrained and consistent look.</p>
          </div>
          <div class="facets">
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-pro"/></svg>Professionalism</h4><ul class="ticks">
              <li>Restrained, consistent visual identity, readable captions</li>
              <li>No promises of earnings, no misleading screenshots</li>
              <li>Partnership flagged in the first line</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-best"/></svg>Best practices</h4><ul class="ticks">
              <li>Educational carousels and short video demos</li>
              <li>Stories to answer frequent questions</li>
              <li>Clear bio that points to a page of comparisons</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-tech"/></svg>Techniques</h4><ul class="ticks">
              <li>"Before / after" workflow demo in under a minute</li>
              <li>Built-in captions, cover readable even without sound</li>
              <li>Dedicated landing page to measure clicks</li></ul></div>
            <div class="facet facet--rules"><h4><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg>Program rules</h4><ul class="ticks">
              <li>Platform's paid partnership label used where it applies</li>
              <li>No brand assets used without the program's permission</li>
              <li>Platform rules on promotional content respected</li></ul></div>
          </div>
        </div>

        <!-- Pinterest -->
        <div class="panel" role="tabpanel" id="panel-pinterest" aria-labelledby="tab-pinterest" hidden>
          <div class="panel-head">
            <h3>Pinterest</h3>
            <p>Make guides and comparisons easy to find through clear, well-indexed visuals.</p>
          </div>
          <div class="facets">
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-pro"/></svg>Professionalism</h4><ul class="ticks">
              <li>Restrained pins, titles that match the page they lead to</li>
              <li>No clickbait that promises more than the content delivers</li>
              <li>Careful descriptions, flagged as affiliate when needed</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-best"/></svg>Best practices</h4><ul class="ticks">
              <li>Infographics, checklists and comparison visuals</li>
              <li>Precise keywords in titles and descriptions</li>
              <li>Themed boards by service category</li></ul></div>
            <div class="facet"><h4><svg class="ic" aria-hidden="true"><use href="#i-tech"/></svg>Techniques</h4><ul class="ticks">
              <li>Vertical format, text readable on mobile, one message per visual</li>
              <li>Pins that lead first to my own guides and comparisons</li>
              <li>Tracking parameters per pin and per board</li></ul></div>
            <div class="facet facet--rules"><h4><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg>Program rules</h4><ul class="ticks">
              <li>Affiliate disclosure in the description of relevant pins</li>
              <li>Pinterest's and the program's rules on links respected</li>
              <li>No misleading content, no hidden redirects</li></ul></div>
          </div>
        </div>
      </div>
    </div>
    <noscript><style>.panel[hidden] { display: grid !important; margin-top: 1.5rem; }</style></noscript>
  </div>
</section>

<section class="sec sec--surface" id="formats">
  <div class="wrap">
    <div class="sec-head">
      <span class="label">Promotion formats</span>
      <h2>Seven formats, one for each stage of the buying decision.</h2>
      <p>A business buyer rarely decides in a single visit. Each format answers a precise moment in their thinking, and every one carries the affiliate disclosure.</p>
    </div>

    <div class="formats grid">
      <article class="format"><svg class="ic" aria-hidden="true"><use href="#i-compare"/></svg><h3>Comparisons</h3><p>Public criteria, side-by-side tables, a recommendation matched to the buyer's profile.</p><span class="kicker">Stage: comparison</span></article>
      <article class="format"><svg class="ic" aria-hidden="true"><use href="#i-doc"/></svg><h3>Full service reviews</h3><p>Features, pricing, limits, integrations and target audience gathered on a single page.</p><span class="kicker">Stage: evaluation</span></article>
      <article class="format"><svg class="ic" aria-hidden="true"><use href="#i-guide"/></svg><h3>Guides</h3><p>Step by step to choose, set up or switch a tool, or to scope a hire.</p><span class="kicker">Stage: discovery</span></article>
      <article class="format"><svg class="ic" aria-hidden="true"><use href="#i-blog"/></svg><h3>Blog articles</h3><p>Answers to precise industry questions, with sources and update dates.</p><span class="kicker">Stage: discovery</span></article>
      <article class="format"><svg class="ic" aria-hidden="true"><use href="#i-ebook"/></svg><h3>Ebooks</h3><p>Long, downloadable resources for teams preparing a purchase.</p><span class="kicker">Stage: consideration</span></article>
      <article class="format"><svg class="ic" aria-hidden="true"><use href="#i-case"/></svg><h3>Use cases</h3><p>A problem, a solution, how it was implemented and the limits observed.</p><span class="kicker">Stage: consideration</span></article>
      <article class="format"><svg class="ic" aria-hidden="true"><use href="#i-video"/></svg><h3>Videos</h3><p>Short demos, a walkthrough of a tool, answers to frequent questions.</p><span class="kicker">Stage: demonstration</span></article>
      <article class="format format--note"><svg class="ic" aria-hidden="true"><use href="#i-rules"/></svg><h3>Affiliation always disclosed</h3><p>The disclosure text appears before the first link, on the blog as in video.</p></article>
    </div>

    <div class="matrix-block">
      <h3>Where each format circulates</h3>
      <div class="scroll">
        <table class="matrix">
          <thead>
            <tr><th scope="col" style="text-align:left">Format</th><th scope="col">Cold email</th><th scope="col">SEO</th><th scope="col">X</th><th scope="col">LinkedIn</th><th scope="col">Instagram</th><th scope="col">Pinterest</th></tr>
          </thead>
          <tbody>
            <tr><th scope="row">Comparisons</th><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td><td class="n"><i class="sr">not used</i></td><td class="p"><i class="sr">primary</i></td></tr>
            <tr><th scope="row">Full service reviews</th><td class="n"><i class="sr">not used</i></td><td class="p"><i class="sr">primary</i></td><td class="n"><i class="sr">not used</i></td><td class="s"><i class="sr">secondary</i></td><td class="n"><i class="sr">not used</i></td><td class="s"><i class="sr">secondary</i></td></tr>
            <tr><th scope="row">Guides</th><td class="p"><i class="sr">primary</i></td><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td></tr>
            <tr><th scope="row">Blog articles</th><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td><td class="n"><i class="sr">not used</i></td><td class="p"><i class="sr">primary</i></td></tr>
            <tr><th scope="row">Ebooks</th><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td><td class="n"><i class="sr">not used</i></td><td class="p"><i class="sr">primary</i></td><td class="n"><i class="sr">not used</i></td><td class="s"><i class="sr">secondary</i></td></tr>
            <tr><th scope="row">Use cases</th><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td><td class="n"><i class="sr">not used</i></td></tr>
            <tr><th scope="row">Videos</th><td class="s"><i class="sr">secondary</i></td><td class="s"><i class="sr">secondary</i></td><td class="s"><i class="sr">secondary</i></td><td class="s"><i class="sr">secondary</i></td><td class="p"><i class="sr">primary</i></td><td class="s"><i class="sr">secondary</i></td></tr>
          </tbody>
        </table>
      </div>
      <div class="legend"><span><i class="p"></i>Primary channel</span><span><i class="s"></i>Secondary channel</span><span>Dash: not used on this channel</span></div>
    </div>
  </div>
</section>

<section class="sec sec--alt" id="objections">
  <div class="wrap">
    <div class="sec-head">
      <span class="label">Objections</span>
      <h2>The questions a brand asks before accepting an affiliate.</h2>
      <p>They are fair. Here is how I answer them, plainly.</p>
    </div>
    <div class="objections grid">
      <article class="objection">
        <q>An independent affiliate is a risk to our brand image.</q>
        <div class="answer"><span class="label">My answer</span><p>You are dealing with an identified person, not a network of anonymous sites. I follow your brand guidelines, submit sensitive materials for approval when the program requires it, and remove any content at your request.</p></div>
      </article>
      <article class="objection">
        <q>We don't want cold email sent with our name on it.</q>
        <div class="answer"><span class="label">My answer</span><p>I don't send any for a brand that doesn't explicitly allow it. When the program accepts it, I use approved messages, a one-click unsubscribe and a suppression list.</p></div>
      </article>
      <article class="objection">
        <q>How will we know where the traffic comes from?</q>
        <div class="answer"><span class="label">My answer</span><p>Every channel and every piece of content has its own sub-ID or tracking parameter. I can share a summary by channel with clicks, sign-ups and attributed sales, within what the program allows.</p></div>
      </article>
      <article class="objection">
        <q>You're going to bid on our brand.</q>
        <div class="answer"><span class="label">My answer</span><p>No. No bidding on your name or its variants, no domain that imitates your brand, no invented promo codes. If an exception suits you, it has to be in writing.</p></div>
      </article>
      <article class="objection">
        <q>A single affiliate won't bring volume.</q>
        <div class="answer"><span class="label">My answer</span><p>I don't promise volume. I target precise queries and decision-makers where buying intent already exists. We can set a trial period with indicators agreed in advance.</p></div>
      </article>
      <article class="objection">
        <q>Affiliate content is biased.</q>
        <div class="answer"><span class="label">My answer</span><p>I say so from the start and compare on public criteria. I also state when a solution is not a fit: a recommendation that admits its limits is more credible and sends you better-informed buyers.</p></div>
      </article>
    </div>
  </div>
</section>

<section class="sec" id="faq">
  <div class="wrap faq-grid grid">
    <div class="sec-head">
      <span class="label">FAQ</span>
      <h2>Frequently asked questions.</h2>
      <p>Can't find your answer? Write to me and I'll reply precisely.</p>
      <div><a class="btn btn--ghost" href="#contact">Ask a question</a></div>
    </div>
    <div class="faq">
      <details><summary>Who is behind this page?</summary><p>Nicolas Wylock, 38, based in Belgium. I work as an independent B2B affiliate, specializing in SaaS, software and recruitment services.</p></details>
      <details><summary>Which programs can I propose to you?</summary><p>Any B2B program in these three categories, with written terms: commission rate, cookie duration, payment timing, allowed channels and brand usage rules.</p></details>
      <details><summary>How does a collaboration start?</summary><p>You send me the program link and its terms. I read them, then tell you which channels I would use and which I rule out. Once accepted, I prepare a first piece of content and a tracking plan.</p></details>
      <details><summary>How are you paid?</summary><p>According to the program: commission per sale, per lead or recurring. The brand pays only what the program provides for. My invoicing details are shared at sign-up.</p></details>
      <details><summary>How do you disclose the affiliation?</summary><p>With a visible statement before the first affiliate link, in the article, post, video or email. On the web, links are also tagged for search engines.</p></details>
      <details><summary>What happens if the program's rules change?</summary><p>I re-read the terms at every announced update. Affected content is corrected or removed, and I let you know.</p></details>
      <details><summary>Do you work on an exclusive basis?</summary><p>My comparisons present several solutions, which is what makes them credible. If category exclusivity interests you, we can discuss it case by case.</p></details>
    </div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="wrap contact-grid grid">
    <div>
      <span class="label">Contact</span>
      <h2>Do you run an affiliate program?</h2>
      <p class="lead">Send me the program link and its terms. I'll reply with the channels I would use and those I would rule out.</p>
    </div>
    <div class="contact-box">
      <h3>What to include to move fast</h3>
      <ul class="ticks">
        <li>The program link and its terms and conditions</li>
        <li>Commission, cookie duration and payment timing</li>
        <li>Allowed and forbidden channels</li>
        <li>Brand resources: logos, approved copy, visuals</li>
      </ul>
      <div class="mail-row" id="mail-row" hidden>
        <code id="mail-addr"></code>
        <button class="btn btn--sm btn--band" id="mail-copy" type="button">Copy</button>
      </div>
      <div class="channels" id="channels" aria-label="Channels"></div>
    </div>
  </div>
</section>
</main>

<footer class="foot">
  <div class="wrap foot-in">
    <p>This page presents my B2B affiliate activity. Content I publish about brands may contain affiliate links, always disclosed as such.</p>
    <p>© 2026 Nicolas Wylock · Belgium</p>
  </div>
</footer>

<script>
(function () {
  // Contact details shown in the contact block: fill in the values to activate the links.
  var CONFIG = { email: "", linkedin: "", x: "", instagram: "", pinterest: "" };

  // Channel tabs
  var tabs = Array.prototype.slice.call(document.querySelectorAll('[role="tab"]'));
  var panels = tabs.map(function (t) { return document.getElementById(t.getAttribute('aria-controls')); });
  function select(i, focus) {
    tabs.forEach(function (t, j) {
      var on = i === j;
      t.setAttribute('aria-selected', on ? 'true' : 'false');
      t.tabIndex = on ? 0 : -1;
      panels[j].hidden = !on;
    });
    if (focus) tabs[i].focus();
  }
  tabs.forEach(function (t, i) {
    t.addEventListener('click', function () { select(i, false); });
    t.addEventListener('keydown', function (e) {
      var n = null;
      if (e.key === 'ArrowRight' || e.key === 'ArrowDown') n = (i + 1) % tabs.length;
      else if (e.key === 'ArrowLeft' || e.key === 'ArrowUp') n = (i - 1 + tabs.length) % tabs.length;
      else if (e.key === 'Home') n = 0;
      else if (e.key === 'End') n = tabs.length - 1;
      if (n !== null) { e.preventDefault(); select(n, true); }
    });
  });

  // Active section in the navigation
  var links = Array.prototype.slice.call(document.querySelectorAll('.nav nav a'));
  var targets = links.map(function (a) { return document.querySelector(a.getAttribute('href')); });
  if ('IntersectionObserver' in window) {
    var io = new IntersectionObserver(function (entries) {
      entries.forEach(function (en) {
        if (!en.isIntersecting) return;
        links.forEach(function (a, k) {
          if (targets[k] === en.target) a.setAttribute('aria-current', 'true');
          else a.removeAttribute('aria-current');
        });
      });
    }, { rootMargin: '-40% 0px -55% 0px' });
    targets.forEach(function (t) { if (t) io.observe(t); });
  }

  // Contact block
  var labels = { linkedin: 'LinkedIn', x: 'X', instagram: 'Instagram', pinterest: 'Pinterest' };
  var box = document.getElementById('channels');
  Object.keys(labels).forEach(function (k) {
    var url = CONFIG[k];
    var el = document.createElement(url ? 'a' : 'span');
    el.className = 'chip';
    el.textContent = labels[k];
    if (url) { el.href = url; el.target = '_blank'; el.rel = 'noopener'; }
    box.appendChild(el);
  });
  if (CONFIG.email) {
    var row = document.getElementById('mail-row');
    var addr = document.getElementById('mail-addr');
    var btn = document.getElementById('mail-copy');
    addr.textContent = CONFIG.email;
    row.hidden = false;
    btn.addEventListener('click', function () {
      var done = function (msg) { btn.textContent = msg; setTimeout(function () { btn.textContent = 'Copy'; }, 1800); };
      try {
        navigator.clipboard.writeText(CONFIG.email).then(function () { done('Copied'); }, function () { fallback(); });
      } catch (e) { fallback(); }
      function fallback() {
        var r = document.createRange();
        r.selectNodeContents(addr);
        var s = window.getSelection();
        s.removeAllRanges();
        s.addRange(r);
        done('Selected');
      }
    });
  }
})();
</script>

</body></html>
