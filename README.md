# KINETIK-LAB – Das schlecht ausgespülte Becherglas

## Entwicklungsstand

**Version:** v0.1.0  
**Status:** Entwicklungsprototyp – noch nicht für den regulären Unterrichtseinsatz freigegeben.

Diese Version dient der gemeinsamen didaktischen und technischen Erprobung. Inhalte, Messparameter, Arbeitsaufträge, Importfunktionen und Auswertungen können sich bis zur Unterrichtsversion noch ändern.

## Ziel

Das KINETIK-LAB ist eine browserbasierte Lernumgebung zur Verbindung von

- präexperimenteller Planung,
- virtuellem Erproben und bewusst möglichem Scheitern,
- realer photometrischer Messung,
- Import realer Messdaten,
- Vergleich von Experiment und Simulation,
- mathematischer Auswertung und Modellbildung.

Als fachliches Beispiel dient die Entfärbung von Kristallviolett durch Hydroxidionen.

Die App soll das reale Experiment **nicht ersetzen**. Die Simulation unterstützt vor allem die Planung vor dem Experiment und die systematische Auswertung danach.

## Didaktische Phasen

1. Beobachten
2. Forschungsfrage und Messplan entwickeln
3. Virtuell erproben
   - geeignete Messwellenlänge
   - Messintervall und Messdauer
4. Reales Experiment
5. Realdaten auswerten, mit Simulation vergleichen und ein kinetisches Modell ableiten

Die einzelnen Phasen werden schrittweise freigegeben.

## Wichtiger Hinweis zu v0.1.0

Die derzeit verwendeten kinetischen Parameter sind **vorläufige Entwicklungswerte**. Sie werden noch mit realen Schulmessungen abgeglichen. Die App darf daher in dieser Version nicht als quantitativ validiertes Referenzmodell verstanden werden.

## Dateien

```text
index.html
README.md
.nojekyll
```

Die Anwendung ist als **Single-HTML-App** ausgeführt und benötigt keine Installation oder Serverlogik.

## Lokal testen

`index.html` im Browser öffnen.

## GitHub Pages

Für ein einfaches Repository genügt es, die drei Dateien direkt im Hauptverzeichnis abzulegen.

Danach unter:

**Settings → Pages → Build and deployment**

einstellen:

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/ (root)`

## .nojekyll

Die leere Datei `.nojekyll` weist GitHub Pages an, die Dateien unverändert als statische Website bereitzustellen und keine Jekyll-Verarbeitung anzuwenden.

Für diese Single-HTML-App ist sie nicht zwingend erforderlich, aber sinnvoll und unproblematisch.

## Versionsstrategie

- `v0.1.x` – frühe Entwicklungs- und Abstimmungsversionen
- `v0.2.x` – didaktisch und technisch konsolidierte Testversionen
- später `v1.0.0` – stabile Unterrichtsversion

Für jede Entwicklungsstufe soll ein separat benanntes ZIP-Archiv bereitgestellt werden.

## Geplante nächste Schritte

- Feinschliff der fünf didaktischen Phasen
- SchülerInnenanleitung und phasenbezogene Arbeitsunterlagen
- Anpassung des Imports realer Messdaten
- Schnittstelle zum MESSWERT_LAB
- Abgleich des kinetischen Modells mit realen Schulmessungen
- LehrerInnenhinweise und Sicherheitsinformationen

---

Projektkontext: **CHEMIE mit KI**
