# KINETIK-LAB – Das schlecht ausgespülte Becherglas

## Entwicklungsstand

**Version:** v0.1.2  
**Status:** Entwicklungsprototyp – noch nicht für den regulären Unterrichtseinsatz freigegeben.

Die App entwickelt eine Forschungssequenz zur photometrischen Kinetik von Kristallviolett und Hydroxid. Das reale Experiment bleibt der zentrale Bezugspunkt; die virtuelle Umgebung unterstützt Planung, Erprobung, Datenvergleich und Modellbildung.

## Neu in v0.1.2

- Der LehrerInnenmodus wird unauffällig im Footer über ein kleines Codefeld freigeschaltet; die Zugangshürde ist ausdrücklich keine Sicherheitsfunktion.
- Der Freigabecode für Phase 2 blendet gleichzeitig die Zusatzinformation zu den Natronlaugeresten ein.
- Nach der Phase-2-Freigabe bleibt die Gruppe zunächst in Phase 1 und kann Beobachtung/Hypothesen ergänzen; der Wechsel zu Phase 2 erfolgt bewusst anschließend.
- Ab Phase 2 besitzt **„Ergebnisse zur Besprechung“** eine Funktion **„In Zwischenablage kopieren“**. Damit lassen sich eigene Formulierungen und Messbedingungen schnell in ein parallel geführtes Protokoll übernehmen.
- Neue kompakte **Stoffinfo Kristallviolett** als Popup in Phase 2: farbige CV⁺-Form, Angriff von OH⁻ am zentralen C-Atom, Bildung der farblosen Carbinol-/Pseudobasenform und Unterbrechung des konjugierten Systems. Die Stoffinfo verrät keine Reaktionsordnung.
- Die sichtbare Messgröße bleibt standardmäßig **Absorbanz A**. Eine spätere Umschaltung auf **Extinktion E** ist intern über eine zentrale Notationsschicht vorbereitet, aber noch nicht in der Benutzeroberfläche freigeschaltet.
- Sitzungen aus v0.1.1 werden beim ersten Start soweit möglich übernommen.

## Phasenfreigabe

Die Freigabecodes sind **didaktische Barrieren, keine Sicherheitsfunktion**. Phase 1 wird gemeinsam begonnen. Nach der gemeinsamen Besprechung kann der Code für Phase 2 allen Gruppen bekanntgegeben werden. Mit dessen Eingabe wird auch die Zusatzinformation zur Natronlauge sichtbar. Die Gruppen ergänzen daraufhin ihre eigene Dokumentation und wechseln erst danach bewusst in Phase 2.

Ab Phase 2 können Gruppen im eigenen Tempo arbeiten. Nach einem kurzen Gespräch mit Lehrperson oder Laborpersonal erhalten sie den jeweils nächsten Code.

## Ergebnisse und Protokoll

Die App speichert die eigenen Texte und Messbedingungen lokal. Die Besprechungsansichten ab Phase 2 können als formatierten Klartext in die Zwischenablage kopiert werden. Zusätzlich bleibt der kumulative Markdown-Arbeitsstand erhalten.

## Dateien

```text
index.html
README.md
.nojekyll
docs/
└── schuelerinnen/
    ├── 00_Kurzanleitung_KINETIK_LAB.md
    └── 01_Beobachtung_Hypothesen.md
```

## GitHub Pages

Die Dateien können direkt in das Repository-Root hochgeladen werden. `.nojekyll` verhindert eine unnötige Jekyll-Verarbeitung der statischen Dateien.

## Noch offen

- Feinschliff der einzelnen Phasen
- sichtbare Option **Absorbanz A / Extinktion E** erst in einer späten Konsolidierungsphase
- weitere SchülerInnen-Arbeitsblätter
- LehrerInnenanleitung
- Abgleich der vorläufigen kinetischen Modellparameter mit einem eigenen Realversuch
- spätere DOCX-Downloads der stabilen Arbeits- und Anleitungsmaterialien

> Die derzeit verwendeten kinetischen Geschwindigkeitsparameter sind Entwicklungswerte und noch nicht als quantitative Referenz für einen konkreten Schulversuch validiert.
