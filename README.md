# CAMS Regionale Luftqualitätsvorhersage – Analyse der Ozonkonzentration über Deutschland

Dieses Repository enthält ein Jupyter Notebook zur Analyse von Luftqualitätsvorhersagen des Copernicus Atmosphere Monitoring Service (CAMS) für Deutschland.

CAMS stellt modellbasierte Informationen zur Luftqualität bereit, die auf Atmosphärenmodellen und Beobachtungsdaten basieren und für Umweltanalysen, Forschung und Anwendungen in Behörden genutzt werden können.

## Ziel

Ziel dieses Notebooks ist es, einen praxisnahen Einstieg in die Nutzung von CAMS-Daten zu geben und grundlegende Methoden zur Analyse von Luftqualitätsvorhersagen zu vermitteln.

## Zielgruppe

Das Notebook richtet sich an:

- Studierende und Forschende im Bereich Umwelt, Geographie, Meteorologie oder Datenanalyse 
- alle weiteren Interessierten, die mit Luftqualitätsdaten arbeiten möchten

## Einordnung

Dieses Notebook basiert auf dem ECMWF-Trainingskurs zur regionalen Luftqualitätsvorhersage  
([ECMWF CAMS Training Notebook](https://github.com/ecmwf-training/cams-training/blob/main/cams-regional-forecast.ipynb)).

## Was wird im Notebook gemacht?

Am Beispiel der bodennahen Ozonkonzentration (O₃) werden folgende Schritte durchgeführt:

- **Datenzugriff:**  
  CAMS-Vorhersagedaten werden über die ADS API heruntergeladen  

- **Datenverarbeitung:**  
  Die Daten werden mit Python (xarray) eingelesen und vorbereitet  

- **Zeitliche Aggregation:**  
  Aus stündlichen Vorhersagen werden tägliche Mittelwerte und Maximalwerte berechnet  

- **Räumliche Analyse:**  
  Die Ozonkonzentration wird als Karten für Deutschland dargestellt  

- **Zeitliche Analyse:**  
  Für einen Beispielstandort (Berlin) wird eine Zeitreihe der Ozonkonzentration erstellt  

## Daten

Verwendet wird der Datensatz:

CAMS European Air Quality Forecast  
https://ads.atmosphere.copernicus.eu/datasets/cams-europe-air-quality-forecasts

Die dargestellten Werte basieren auf modellierten Vorhersagen und stellen keine direkten Messungen dar.

## Nutzung

Das Notebook kann direkt in der Cloud ausgeführt werden, wobei Google Colab zu empfehlen ist:

[![Open in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/oskarwittenberg-dev/CAMS-Ozon-Deutschland/HEAD)
[![Open in Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/oskarwittenberg-dev/CAMS-Ozon-Deutschland/blob/main/NotebookCAMSLuftqualität.ipynb)

Für den Datenzugriff wird ein persönlicher API-Schlüssel für den Atmosphere Data Store (ADS) benötigt.

## Beispielergebnisse

### Ozonvorhersage – Deutschland

Die Karten zeigen die räumliche Verteilung der modellierten Ozonkonzentration.  
Dargestellt werden tägliche Mittelwerte und Maximalwerte, wodurch regionale Unterschiede und Belastungsspitzen sichtbar werden.

![Ozonkarte](figures/o3_maps.png)

### Zeitreihe – Berlin

Die Zeitreihe zeigt die Entwicklung der vorhergesagten Ozonkonzentration über den 96-Stunden-Vorhersagezeitraum.  
Damit lassen sich zeitliche Schwankungen und mögliche Belastungsspitzen analysieren.

![Zeitreihe](figures/o3_timeseries_berlin.png)

## Erweiterungsmöglichkeiten

Die gezeigte Methodik kann auf weitere Luftschadstoffe übertragen werden, z. B.:

- NO₂ (Stickstoffdioxid)  
- PM10 (Feinstaub)  
- PM2.5  
- SO₂  

## Hinweis

Dieses Notebook dient als Einführung und Demonstration grundlegender Methoden zur Analyse von CAMS-Daten.
