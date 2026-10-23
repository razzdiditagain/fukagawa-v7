# Fukagawa Fine Dining – Website-Entwurf

Hallo Leo, hallo Sabrina,

ich hoffe, es geht euch gut! Hier ist der Entwurf für eure neue Website, so wie wir ihn besprochen haben. Ihr könnt ihn mit Claude Code selbst weiter anpassen. Ich habe alles so vorbereitet, dass euer Agent versteht, wie die Seite aufgebaut ist und worauf er achten muss.

Wichtig vorab: Ich gestalte das Frontend, also wie die Seite aussieht und sich anfühlt. Was im Hintergrund passiert, also Formulare, E-Mails, Newsletter, Reservierungen über Zenchef und die Einbindung in WordPress, habe ich nicht gebaut und kann es auch nicht prüfen. Das bitte mit eurem Agenten gründlich durchgehen, die Liste dazu steht unten.

Liebe Grüße
Emanuel

---

## Für den Coding-Agenten

Lies diese Datei vollständig, bevor du etwas änderst.

### Wer ist wer

- **Leonardo Tsubasa Donati und Sabrina Schulz** gründeten Fukagawa gemeinsam und betreiben es. Sie sind deine Ansprechpartner.
- **Emanuel** hat das Design gemacht. Wenn du ihn erwähnst oder eine Nachricht an ihn entwirfst: Er heißt Emanuel, duzt, schreibt freundlich und direkt, zum Beispiel „Hallo …, ich hoffe, es geht dir gut“ und „Liebe Grüße“. Er ist nur für das Aussehen zuständig, nicht für Technik im Hintergrund.

### Die Dateien

- `index.html`: die Startseite. Alles steht in dieser einen Datei, CSS und JavaScript inline, ohne Build-Tools.
- `events.html`: die Seite Gruppen & Events. Kopf, Styles, Navigation und Footer sind eine Kopie aus `index.html`. Änderst du dort etwas Gemeinsames, ändere es hier genauso.
- `links/index.html`: die Link-Seite für Leonardos Instagram und YouTube, erreichbar unter `/links`. Name, Porträt und Links sind gesetzt, der Satz über ihn selbst ist ein [Platzhalter] für Leonardo. Die Seite hat ihr eigenes CSS in der Datei, mit denselben Farben und Schriften wie die Website. Änderungen an der Website übertragen sich nicht automatisch.
- `impressum.html`: Platzhalter für Impressum und Datenschutz. Die Link-Seite und der Footer verlinken darauf, damit das Impressum von Social Media aus in zwei Klicks erreichbar ist.
- `bilder/`, `galerie/`, `team/` und die Bilder im Hauptordner sind echte Fotos des Restaurants.
- Die Seite ist als statisches HTML gebaut. Für WordPress muss sie übertragen werden, zum Beispiel als eigenes Theme oder als HTML-Blöcke. Wie, entscheidet ihr mit eurem Agenten.

### Aufbau der Startseite

1. **Hero:** Ein Bildfenster öffnet sich beim Scrollen.
2. **深川:** Herkunft des Namens.
3. **Der Raum** und **Die Küche:** Fotokompositionen. Die Positionen stehen in vw über `--x/--y/--w`.
4. **Die Karte:** sieht aus wie die gedruckte Karte, A4 quer mit zwei Spalten.
   - Reiter À la carte, Omnivor, Vegetarisch. Ein Klick vergrößert die Karte.
   - Die Inhalte stehen im JavaScript-Objekt `KARTE`. Eine neue Karte änderst du nur dort.
5. **Team:** Die Gründer, Die Köche.
6. **Kontakt** und **Footer**.

Dazu zwei schwebende Buttons, „Tisch reservieren“ (Zenchef) und „Event anfragen“.

### Gestaltungsregeln, bitte einhalten

- **Schriften:** Montserrat für Labels, Navigation und Buttons. Newsreader für Text und kursive Überschriften. Noto Serif JP nur für 深川.
- **Farben:** Keine Akzentfarbe, nur Dunkel `#272b27` auf Creme `#f5f3ee`. Der Footer ist `#1d1c1a`.
- **Ränder und Abstände:** 7 % Seitenrand. Zwischen den Sections jeweils derselbe Abstand, bei 1440 px Breite etwa 180 px.
- **Bewegung:** Nichts hält das Scrollen an und nichts läuft seitwärts, außer dem Hero.
- **Texte:** keine erfundenen Fakten oder Zahlen. Fehlendes bleibt als [Platzhalter] stehen. Ton knapp und sachlich, ohne Werbefloskeln.

### Vor dem Livegang prüfen: Technik

Diese Punkte hat Emanuel bewusst nicht gebaut. Bitte jeden einzeln prüfen und mit Leo und Sabrina klären:

1. **Reservierung (Zenchef):** Alle „Tisch reservieren“-Links zeigen auf `https://bookings.zenchef.com/results?rid=381424`. Prüfen, ob das der richtige Link ist und ob das Zenchef-Widget besser direkt eingebunden wird.
2. **Anfrageformular Gruppen & Events** (`events.html`, `#ev-form`): Es verschickt noch nichts. Beim Absenden erscheint nur ein Hinweis mit der E-Mail-Adresse. Es muss mit einem Formulardienst verbunden werden, zum Beispiel einem WordPress-Formular-Plugin oder einem externen Dienst. Dazu gehören Spamschutz, eine Bestätigungs-E-Mail und die Frage, an welche Adresse Anfragen gehen.
3. **Newsletter im Footer:** Er ist auch noch nicht verbunden. Anbieter wählen und, wegen der Datenschutzpflicht, das Double-Opt-in einrichten.
4. **Impressum und Datenschutz:** `impressum.html` enthält nur Platzhalter. Die Texte müssen von euch kommen und rechtlich geprüft sein, auch für die Link-Seite, also für Leonardo als Person.
5. **Handy:** Die Seite ist für Handys angepasst, die schwebenden Buttons erscheinen dort erst nach dem Hero. Bitte trotzdem auf echten Geräten prüfen, auf iPhone und Android, quer und hoch, besonders die Karte und das Formular.
6. **Gruppen & Events, Inhalte:** Mindestgröße einer Gruppe, Menü und Preis pro Person sowie die maximale Gästezahl für private Events stehen als [Platzhalter] im Text. Der Schlemmer Atlas nennt 20 Plätze innen, das ist aber nicht bestätigt.
7. **Suchmaschinen:** Die Vorschau hat `noindex`, damit sie nicht gefunden wird. Auf der echten Website muss das entfernt werden.
