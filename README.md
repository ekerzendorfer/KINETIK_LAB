# KINETIK-LAB – Das schlecht ausgespülte Becherglas

## Entwicklungsstand

**Version:** v0.1.5  
**Status:** Entwicklungsprototyp – noch nicht für den regulären Unterrichtseinsatz freigegeben.

Die App entwickelt eine Forschungssequenz zur photometrischen Kinetik von Kristallviolett und Hydroxid. Das reale Experiment bleibt der zentrale Bezugspunkt; die virtuelle Umgebung unterstützt Planung, Erprobung, Datenvergleich und Modellbildung.

## Neu in v0.1.5

- Phase 2 wurde räumlich verdichtet: Skizze und Ein-Becherglas-Simulation sind nun annähernd gleich hoch; die längere Erläuterung zur Zeitsimulation steht über die gesamte Rahmenbreite darunter.
- Die Endfarbe der Zeitmaßstab-Simulation ist deutlich blasser und bleibt nur noch schwach violett sichtbar.
- Die Beispielwerte in den Eingabefeldern für die erste Schätzung von Messintervall und Messdauer wurden entfernt. Die Gruppen sollen eigene Werte formulieren.
- Phase 3A: Der virtuelle Spektralscan läuft nun über etwa **5 s** und ist dadurch besser beobachtbar.
- Phase 3B übernimmt, soweit vorhanden, die eigene Schätzung aus Phase 2 als Ausgangspunkt. Es gibt keine voreingestellte „gute“ Standardstrategie mehr.
- Nach jedem virtuellen Testlauf erscheint eine **Reflexionshilfe ohne automatische Bewertung**: Zahl der Messpunkte, erfasste Zeitspanne und relative Signaländerung werden angezeigt; Leitfragen helfen beim Vergleich verschiedener Einstellungen.
- Ein didaktischer Hinweis macht explizit, dass ein kurzer Ausschnitt einer gekrümmten Kurve nahezu geradlinig wirken kann. Damit wird eine zu kurze Messdauer erkennbar, ohne die optimale Einstellung vorzugeben.
- Neues SchülerInnenblatt `03_Virtuelle_Erprobung.md` für Phase 3A/3B.

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
    └── 03_Virtuelle_Erprobung.md
```

## GitHub Pages

Die Dateien können direkt in das Repository-Root hochgeladen werden. `.nojekyll` verhindert eine unnötige Jekyll-Verarbeitung der statischen Dateien.

## Noch offen

- weitere Erprobung und Feinschliff von Phase 3B
- sichtbare Option **Absorbanz A / Extinktion E** erst in einer späten Konsolidierungsphase
- weitere SchülerInnen-Arbeitsblätter
- LehrerInnenanleitung
- Abgleich der vorläufigen kinetischen Modellparameter mit einem eigenen Realversuch
- spätere DOCX-Downloads der stabilen Arbeits- und Anleitungsmaterialien

> Die derzeit verwendeten kinetischen Geschwindigkeitsparameter sind Entwicklungswerte und noch nicht als quantitative Referenz für einen konkreten Schulversuch validiert.


## Änderungen in v0.1.5

- Phase 3B: dezente Warnlogik bei zu kurzem erfasstem Kurvenausschnitt bzw. sehr wenigen Messpunkten; keine automatische Vorgabe einer „richtigen“ Messstrategie.
- Phase 4: Datenquelle technisch vorbereitet (`Eigenes reales Experiment`, `Realer Referenzdatensatz`, `Virtueller Datensatz aus dem SpektralLab`).
- Hinweis und Direktlink zum SpektralLab für Schulen ohne geeignetes Photometer.
- Entwicklungs-Testdatensatz bleibt ausschließlich im LehrerInnenmodus und wird eindeutig als synthetisch gekennzeichnet.
- CSV-Export auf den vorbereiteten Standard `KINETIK_LAB_CSV_v1` umgestellt: `Versuch`, `Zeit_s`, `Absorbanz`, Wellenlänge, Konzentrationen, Schichtdicke, Temperatur, Startverzögerung und Datenquelle.
- Die Gerätezeit bleibt im Export unverändert; eine Startverzögerung wird separat dokumentiert.

Phase 4 ist weiterhin ausdrücklich **vorläufig**. Die endgültige Ausgestaltung erfolgt nach Vorliegen realer Messdaten mit Spektralphotometer und Colorimeter.
