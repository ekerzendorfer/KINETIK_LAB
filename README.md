# KINETIK-LAB – Das schlecht ausgespülte Becherglas

## Version v0.1.9

Zwischenversion auf Basis von v0.1.8.

### Neu

- Phase 5C enthält jetzt eine **vorläufige Vermutung zur Reaktionsordnung**.
- Nach Auswahl von 0., 1. oder 2. Ordnung kann die Vermutung geprüft werden.
- Bei richtiger Auswahl wird der Zusammenhang zwischen der linearen Darstellung
  `ln(A − A∞) gegen t` und einer Reaktion 1. Ordnung erklärt.
- Bei falscher Auswahl wird auf die jeweils passende Linearisierung für
  0. bzw. 2. Ordnung verwiesen, ohne eine Strafwertung vorzunehmen.
- Die Vermutung wird im lokalen Arbeitsstand und im Export mitgespeichert.
- Phase 5E wurde bereinigt: Der bislang vorgeschlagene Wellenlängenvergleich im
  SpektralLab wurde entfernt, weil das dortige KV-Kinetikmodul aktuell keine
  freie Wellenlängenvariation anbietet. Der Vergleich erfolgt direkt innerhalb
  des KINETIK-LABs.

## Real kalibrierter Referenzfall

- c₀(CV⁺) = 1,20·10⁻⁵ mol/L
- c₀(OH⁻) = 0,0300 mol/L
- reale Messung: Vernier Colorimeter, 565 nm
- k_app ≈ 0,00534 s⁻¹
- A∞ ≈ 0,01136

Die reale Startverzögerung beim Mischen und Überführen wird dokumentiert,
aber nicht in das virtuelle Reaktionsmodell eingebaut.
