# KINETIK-LAB – Das schlecht ausgespülte Becherglas

## Entwicklungsstand

**Version:** v0.1.8  
**Status:** Entwicklungsprototyp – noch nicht für den regulären Unterrichtseinsatz freigegeben.

Die App entwickelt eine Forschungssequenz zur photometrischen Kinetik von Kristallviolett und Hydroxid. Das reale Experiment bleibt der zentrale Bezugspunkt; die virtuelle Umgebung unterstützt Planung, Erprobung, Datenvergleich und Modellbildung.

## Neu in v0.1.8

- Phase 1: Die qualitative Entfärbungsanimation wurde von ca. 7 s auf ca. 20 s verlängert.
- Phase 3A: Beim Start ist kein Messgerät und keine reale Wellenlänge mehr vorausgewählt.
- Der Spektralscan kann bewusst vor der Gerätewahl durchgeführt werden. Erst danach werden die verfügbaren Gerätewellenlängen eingeblendet.
- Beim Vernier-Colorimeter wird 565 nm nicht mehr automatisch gewählt; die Lernenden müssen die geeignete verfügbare Wellenlänge selbst festlegen.
- Phase 3B: 1000 s wurde als zusätzliche Messdauer ergänzt.
- Hinweise zur Messstrategie reagieren nun auch auf 120/180 s Messdauer und auf relativ grobe Intervalle ab 20 s.
- Ein Messplan kann erst nach mindestens einem virtuellen Testlauf übernommen werden.
- Phase 4: CSV-Dateien mit mehreren Spalten können vor dem Import über sichtbare Dropdowns für Zeit- und Absorbanz-/Extinktionsspalte zugeordnet werden.
- Vernier-Spalten mit der Bezeichnung „Absorption“ werden jetzt korrekt als Absorbanz erkannt; Transmission wird nicht mehr versehentlich als Zielgröße verwendet.
- Synthetische Entwicklungsdaten werden deutlicher als solche gekennzeichnet und überschreiben die Beobachtungsnotiz entsprechend.
- Phase 5A: A∞ wird bei eigenen Importen nicht mehr automatisch aus den letzten fünf Messpunkten übernommen.
- Für A∞ stehen drei transparente Wege zur Verfügung: realer Referenzwert bei 565 nm, Schätzung aus einem tatsächlichen Endplateau oder begründete manuelle Eingabe.
- Phase 5C: Werte sehr nahe an A∞ werden aus der linearen Regression ausgeschlossen, weil Logarithmus und Kehrwert dort Messrauschen stark verstärken. Der verwendete Fitbereich wird sichtbar ausgewiesen; die Rohdaten bleiben vollständig erhalten.
- Phase 5D: Der Weg von der OH⁻-Variation über k_app zur Reaktionsordnung wird in vier Schritten explizit dargestellt.
- Phase 5E: Optionaler Zusatzauftrag für einen Wellenlängenvergleich im SpektralLab.
- Finale Erkenntnis: kleine „Denkhilfe“-Schaltflächen zu Reaktionsordnung CV⁺, Reaktionsordnung OH⁻ und Geschwindigkeitsgesetz.

## Real kalibrierter Referenzfall

- c₀(CV⁺) = 1,20·10⁻⁵ mol/L
- c₀(OH⁻) = 0,0300 mol/L
- Vernier Colorimeter, 565 nm
- k_app ≈ 0,00534 s⁻¹
- A∞ ≈ 0,01136

Die etwa 15 s zwischen Mischen und erster registrierter Messung werden als reale experimentelle Startverzögerung dokumentiert, aber nicht in das virtuelle Reaktionsmodell eingebaut.

## Wichtiger Hinweis zu Phase 5C

Bei einer Langzeitmessung nähert sich A der Größe A∞. Dann werden A − A∞ sehr klein. Die Transformationen ln(A − A∞) und besonders 1/(A − A∞) verstärken deshalb unvermeidlich kleine Messfehler und die begrenzte Auflösung des Messgeräts.

v0.1.8 verwendet deshalb für alle drei Ordnungsprüfungen denselben transparenten Auswertungsbereich: Nur Messpunkte mit A − A∞ ≥ 5 % des anfänglichen Signals oberhalb von A∞ werden für die lineare Regression herangezogen. Spätere Punkte bleiben in den Rohdaten erhalten.

Beim hinterlegten realen Referenzlauf führt dies ungefähr bis 575 s und liefert für ln(A − A∞) eine nahezu lineare Darstellung mit k_app ≈ 0,00531 s⁻¹.

## GitHub Pages

`index.html` kann direkt im Repository-Root verwendet werden. Die beigefügte `.nojekyll` verhindert eine unnötige Jekyll-Verarbeitung.

## Noch offen

- Wiederholungsmessungen der niedrigen und hohen CV-Konzentration mit längerer Messdauer
- reale Validierung der OH⁻-Reihe bei 0,005 / 0,010 / 0,020 / 0,030 mol/L
- optionaler realer Vergleich 565 nm mit einer Messung näher am spektralen Maximum
- Anpassung des Kinetik-Kerns im SpektralLab an denselben real kalibrierten Referenzfall
- LehrerInnenanleitung und spätere DOCX-Downloads der stabilen Materialien

> v0.1.8 bleibt bewusst **real kalibriert, aber nicht „realitätskosmetisiert“**: Reale Messungen verankern den Referenzfall, während Modellgrenzen, Messrauschen und noch nicht validierte Bereiche sichtbar bleiben.
