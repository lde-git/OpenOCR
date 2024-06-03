# OCR-Vergleich: Microsoft Phi-3-vision-128k-instruct (Open Source) vs. Gemini Advanced (Closed Source)

## Projektbeschreibung

Dieses Projekt untersucht die OCR-Fähigkeiten (Optical Character Recognition) von zwei KI-Modellen: Gemini Advanced (closed Source) und Microsoft Phi-3-vision-128k-instruct (Open Spurce). Ziel ist es, die Stärken und Schwächen beider Modelle in verschiedenen OCR-Szenarien zu bewerten.

## 1. Mögliche Aufgaben

Die OCR-Fähigkeiten der Modelle anhand verschiedener Kriterien testen:

* **Genauigkeit:** Wie gut können die Modelle Text aus Bildern unterschiedlicher Qualität und Komplexität extrahieren?
* **Robustheit und Fehlertoleranz:** Wie gut funktionieren die Modelle bei verschiedenen Schriftarten, Handschriften, Layouts, Unschärfe und Rauschen?
* **Geschwindigkeit:** Wie schnell können die Modelle Text aus Bildern extrahieren?
* **Output:** Wie gut wird der Text in bspw. JSON/XML ausgegeben? 

**Beispiel:**

Den Modellen wird ein Bild eines historischen Dokuments mit verblasstem Text und einem handschriftlichen Kommentar vorlegen. Anschließend wird der extrahierten Texte auf Genauigkeit und Vollständigkeit verglichen.

## 2. Datenbasis

* **Medium:** Gescannte Dokumente, Fotos von Texten, Screenshots
* **Sprache:** Deutsch/Englisch (ggf. auch andere Sprachen zum Vergleich)
* **Quelle:**  Archivmaterialien, historische Dokumente, aktuelle Zeitungsartikel

## 3. OpenLLM

* Microsoft Phi-3-vision-128k-instruct
* (Optional: Weitere Modelle zum Vergleich, z.B. Tesseract OCR)
* Vergleich per: Gemini Advanced

## 4. Experimentdesign

1. **Datenauswahl:** Zusammenstellung eines kleinen (vielfältigen) Datensatzes mit Textenausschnitten unterschiedlicher Schwierigkeitsgrade.
2. **Vorverarbeitung:**  Eventuell notwendige Bildoptimierung (z.B. Kontrastanpassung, Rauschreduzierung).
3. **OCR-Durchführung:** Jedes Bild wird beiden Modellen vorgelegt.
4. **Ergebnisbewertung:**
    * Manueller Vergleich der extrahierten Texte mit den Originalen.
    * evtl. Berechnung von Genauigkeitsmetriken (z.B. Zeichenfehlerrate, Wortfehlerrate).
    * Messung der Bearbeitungszeit pro Bild.
5. **Analyse:** Identifizierung von Stärken und Schwächen der Modelle in Bezug auf die verschiedenen Kriterien.

## Projektstruktur

* **data:** Ordner für die verwendeten Bilddaten (ggf. privat, Link oder separater Zugang)
* **prompts:** Ordner für die Prompts an die LLMs und deren Entwicklung
* **results:** Ordner für die Ergebnisse der OCR-Durchführung (extrahierte Texte)
* **code:** Ordner für den Code zur Datenverarbeitung, OCR-Durchführung und Auswertung

##
