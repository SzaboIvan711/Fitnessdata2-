🧠 Fitness Data – Machine Learning Regression Project

Fragestellung

Welche Verfahren des maschinellen Lernens eignen sich am besten zur Vorhersage des Kalorienverbrauchs anhand von Aktivitäts- und Körperdaten?

Datensatz

Für dieses Projekt wurde der folgende echte Fitness-Datensatz verwendet:
🔗 https://www.opendatabay.com/data/ai-ml/79f97d41-7e85-476c-84a1-610283f9de4e

Der Datensatz enthält verschiedene Aktivitäts- und Körpermetriken wie Schritte, Herzfrequenz, Gewicht, Trainingsdauer und den gemessenen Kalorienverbrauch.

Datenvorverarbeitung

Die Daten wurden mithilfe eines sklearn-Pipelinesystems vollständig vorverarbeitet:

Behandlung fehlender Werte

Skalierung numerischer Features

One-Hot-Encoding kategorialer Variablen

optionale Erzeugung zusätzlicher Polynom-Features

Train-/Test-Split wurde vor dem Modelltraining durchgeführt.

Verwendete Modelle

Es wurden drei Regressionsmodelle verglichen:

Lineare Regression

Polynomiale Regression (mit Features)

Random Forest Regression

Alle Modelle wurden mithilfe derselben Pipeline trainiert, um eine faire Vergleichbarkeit zu gewährleisten.

Evaluierungsmethoden

Jedes Modell wurde anhand mehrerer Metriken bewertet:

MAE — Mean Absolute Error

RMSE — Root Mean Squared Error

Sowohl:

auf dem Test-Set, als auch

per Cross-Validation (k=10)

um Stabilität und Generalisierungsfähigkeit zu überprüfen.

Hyperparameter-Optimierung

Zur Verbesserung der Modellleistung wurde für jedes Modell eine RandomizedSearchCV-Optimierung durchgeführt.
Danach wurden die Modelle erneut mittels Cross-Validation und auf dem Test-Set bewertet.

Visualisierung

Für alle Modelle wurden erstellt:

Predicted vs. True Plots

Residual Plots (Fehleranalyse)

Vergleichende Grafiken der Modellleistung

Dies erlaubte eine klare Analyse von Overfitting, Unterfitting und systematischen Fehlern.

Ergebnisse

Die Auswertung zeigt deutlich, dass:

⭐ Die Polynomiale Regression (mit erweiterten Features) die beste Performance erzielt hat.

niedrigste MAE- und RMSE-Werte

gleichmäßige Residuenverteilung

robusteste Ergebnisse in der Cross-Validation

Die Lineare Regression zeigte klare Underfitting-Strukturen, während Random Forest gut, aber weniger präzise als das Polynommodell abschnitt.

Fazit

Für diesen Datensatz eignet sich die Polynomiale Regression mit erweiterten Features am besten zur Vorhersage des Kalorienverbrauchs.