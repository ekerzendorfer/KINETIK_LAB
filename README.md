# KINETIK-LAB – Das schlecht ausgespülte Becherglas

## Entwicklungsstand

**Version:** v0.1.7  
**Status:** Entwicklungsprototyp – noch nicht für den regulären Unterrichtseinsatz freigegeben.

Die App entwickelt eine Forschungssequenz zur photometrischen Kinetik von Kristallviolett und Hydroxid. Das reale Experiment bleibt der zentrale Bezugspunkt; die virtuelle Umgebung unterstützt Planung, Erprobung, Datenvergleich und Modellbildung.

## Neu in v0.1.7

- Der kinetische Referenzfall ist erstmals an einer eigenen realen Schulmessung kalibriert: Vernier Colorimeter, 565 nm, c₀(CV⁺) = 1,20·10⁻⁵ mol/L, c₀(OH⁻) = 0,0300 mol/L.
- Referenzparameter des virtuellen Modells: k_app ≈ 0,00534 s⁻¹ und A∞ ≈ 0,01136.
- Der reale 20-min-Referenzlauf kann in Phase 4 direkt geladen werden; die bereinigte CSV liegt zusätzlich unter `docs/referenzdaten/`.
- Die ca. 15 s Misch-/Überführungszeit wird dokumentiert, aber nicht in das virtuelle Reaktionsmodell eingebaut und standardmäßig nicht auf die Zeitachse aufgeschlagen.
- Phase 5B weist ausdrücklich darauf hin, dass Real-/Modellabweichungen nicht verborgen werden.
- Die OH⁻-Variation bleibt vorerst eine Modellvorhersage; nur der Referenzpunkt bei 0,030 M ist real kalibriert.


## Didaktische Funktion von Phase 2

Die Lernenden sollen Photometrie nicht aus dem Nichts „erfinden“ müssen. Zuerst formulieren sie eine eigene Messidee. Bei Bedarf steht ein kurzer fachlicher Exkurs zur Verfügung. Die optimale Messwellenlänge und der eigentliche photometrische Messplan werden erst in Phase 3 untersucht.

Die kleine Zeitmaßstab-Simulation dient noch nicht der Bestimmung einer Reaktionsordnung. Sie soll lediglich eine begründete erste Vorstellung ermöglichen, in welcher Größenordnung Messintervall und Messdauer liegen könnten.

## Phasenfreigabe

Die Freigabecodes sind **didaktische Barrieren, keine Sicherheitsfunktion**. Phase 1 wird gemeinsam begonnen. Nach der gemeinsamen Besprechung kann der Code für Phase 2 allen Gruppen bekanntgegeben werden. Ab Phase 2 können Gruppen im eigenen Tempo arbeiten und erhalten nach kurzer Rückmeldung den jeweils nächsten Code.

## Ergebnisse und Protokoll

Die App speichert eigene Texte und Messbedingungen lokal. Die Besprechungsansichten ab Phase 2 lassen sich als Klartext in die Zwischenablage kopieren. Zusätzlich bleibt der kumulative Markdown-Arbeitsstand erhalten.

## Dateien

```text
index.html
README.md
.nojekyll
docs/
└── schuelerinnen/
    ├── 00_Kurzanleitung_KINETIK_LAB.md
    ├── 01_Beobachtung_Hypothesen.md
    ├── 02_Forschungsfrage_Messplan.md
    ├── 03_Virtuelle_Erprobung.md
    └── 05_Auswertung_Erkenntnis.md
└── referenzdaten/
    └── KV_Referenz_565nm_KINETIK_LAB.csv
```

## GitHub Pages

Die Dateien können direkt in das Repository-Root hochgeladen werden. `.nojekyll` verhindert eine unnötige Jekyll-Verarbeitung der statischen Dateien.

## Noch offen

- Wiederholungsmessungen der niedrigen und hohen CV-Konzentration mit längerer Messdauer
- reale Validierung der OH⁻-Reihe bei 0,005 / 0,010 / 0,020 / 0,030 mol/L
- optionaler Vergleich 565 nm mit einer Messung näher am spektralen Maximum
- spätere Angleichung des Kinetik-Kerns im SpektralLab an denselben real kalibrierten Referenzfall
- sichtbare Option **Absorbanz A / Extinktion E** erst in einer späten Konsolidierungsphase
- LehrerInnenanleitung und spätere DOCX-Downloads der stabilen Materialien

> v0.1.7 ist **real kalibriert, aber nicht „realitätskosmetisiert“**: Der Referenzfall basiert auf einer realen Messung, während verbleibende Abweichungen und noch nicht validierte Modellbereiche ausdrücklich sichtbar bleiben.
