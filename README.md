# Carbon to Silicon · Fassadenkonfigurator

**Architekturprojekt von Rugeyye Nur Aksu · Hochschule Mainz · WS 2026/27 · Prof. Thomas Mrokon**

**[Konfigurator im Browser öffnen](https://rugeyyenuraksu.github.io/carbon-to-silicon/)**

## Konzept und eigener Beitrag

Wie kann ein schmales Gebäude trotz geschlossener Seitenwände unterschiedliche räumliche Qualitäten erzeugen? Mein regelbasierter Fassadenkonfigurator untersucht die Beziehung zwischen Gebäude, Straße und Innenhof. Fenster, Erker, Loggia und Balkon bilden das Kit of Parts. Nutzung, räumliche Absicht und Fassadensystem beeinflussen die verfügbaren Kombinationen. Der vorgegebene Blockrand und die seitlichen Brandwände bleiben erhalten.

Der eigene Beitrag ist die Kombination aus nutzungsabhängigen Fassadenregeln, einer dialogbasierten Entwurfsberatung und dem Straßeninteraktionsindex. Die Beratung interpretiert Freitext lokal über Stichwörter und schlägt Optionen vor. Sie verändert weder Modell noch Bewertung automatisch: Die Entwurfsentscheidung bleibt bei der Nutzerin bzw. beim Nutzer. Es gibt keine KI-Aufrufe oder API-Schlüssel zur Laufzeit.

## Bedienung

1. Grundstücksbreite, Tiefe und Traufhöhe wählen. 12–18 m erzeugen 4–6 Geschosse.
2. Wohnen, Büro oder Mischnutzung wählen und räumliche Wünsche beschreiben.
3. Vorschläge lesen und selbst geeignete Einstellungen übernehmen.
4. Fassadensystem, Gliederung, Öffnungsanteil, Erker, Loggien und Balkone vergleichen. Nicht unterstützte Module werden gesperrt.
5. Straßenansicht, Hofansicht oder 3D-Übersicht verwenden. Mit der Maus drehen und zoomen.
6. Das Gebäude über die Schaltflächen als OBJ oder glTF exportieren.

Die Anwendung läuft vollständig im Browser. Alternativ kann `index.html` direkt in Chrome geöffnet werden. Three.js 0.160.0 und seine Add-ons werden von einem fest versionierten CDN geladen; Internet ist dafür erforderlich. Keine Installation, kein Backend und kein Build-Schritt.

## Eigenes Bewertungskriterium

Der Straßeninteraktionsindex bewertet sechs konzeptionelle Aspekte:

| Anteil | Maximalpunkte |
|---|---:|
| Transparenz und Sichtbezug | 20 |
| Schwelle und Eingang | 20 |
| Räumliche Tiefe | 20 |
| Rhythmus und Gliederung | 15 |
| Nutzungsausdruck | 15 |
| Hof–Straße-Balance | 10 |

Die Bewertung verwendet erzeugte Module und geometrische Fensterflächen. Der Tiefenanteil folgt der schematischen Modultiefe. Gewichte und Eignungswerte sind architektonische Setzungen. Ein hoher Wert bedeutet nicht automatisch einen besseren Entwurf: Straßenkontakt kann etwa mit Privatheit und sommerlichem Wärmeschutz konkurrieren. Der Index ist kein normativer Tageslicht- oder Komfortnachweis.

## Geprüfter Finalstand · 01.11.2026

- Chrome: 78 Nutzungs-/Systemvarianten und 24 Geometrie-Stresstests.
- 27 Tests der gesperrten Moduloptionen.
- Fünf Höhen: ausschließlich 4–6 Geschosse.
- Fünf Texteingaben: Vorschläge lassen Parameter, Modell, Kamera und Punktzahl unverändert.
- Kameratasten und A/B/C-Strategien geprüft; im Hauptlauf keine JavaScript-Fehler.
- OBJ und glTF heruntergeladen, mit Trimesh gelesen und mit separaten Three.js-Loadern erneut geöffnet; Modellgrenzen stimmen überein.
- Khronos glTF Validator: keine Fehler oder Warnungen; informative Hinweise auf ungenutzte UV-Daten.

Im Finalstand wurden 11-mm-Überstände an der globalen Höhengrenze, konstante Erker-/Loggia-Tiefenwerte im Index und auswählbare, aber nicht erzeugte Module korrigiert. Konzept und sechs Indexgewichte wurden beibehalten. Diese Tests gelten für den beschriebenen Prüfumfang, nicht für sämtliche denkbaren Kombinationen.

## Grenzen

Dies ist ein schematisches Fassadenwerkzeug, keine vollständige Gebäudeplanung. Innenräume, Grundrisse und Treppen werden nicht generiert. BGF, BRI, GRZ, GFZ und A/V beziehen sich auf eine vereinfachte Grundstücks-Referenzhülle, nicht auf die tatsächlich eingerückte Modellmasse. CO₂ und Kosten verwenden didaktische Platzhalter. Keine DIN-, Statik-, Brandschutz- oder Bauphysiknachweise.

Nicht bestätigt: Firefox, mobile Geräte, native CAD-Imports und ein vollständiger semantischer Bauteilkollisionstest. OBJ enthält keine MTL-Materialdatei. PDF/DXF sind in dieser bewusst reduzierten Fassung nicht implementiert.

## Herkunft und Abgabe

Auf Grundlage des offiziellen [Carbon-to-Silicon-Templates von Prof. Thomas Mrokon](https://github.com/thomasmrokon/carbon-to-silicon). Die Template-Lizenz, technischen Anforderungen und Reflexionsvorlage bleiben erhalten. `index.html` ist der zuletzt lokal geprüfte Finalstand. Die persönliche Reflexion und das tatsächlich verwendete KI-Modell sind zusätzlich in den Abgabeunterlagen anzugeben.
