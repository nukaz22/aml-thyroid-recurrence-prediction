# Analyse und ML-basierte Prognose von Rezidiven bei differenziertem Schilddrüsenkrebs

Dieses Projekt untersucht das Rückfallrisiko bei Patientinnen und Patienten mit differenziertem Schilddrüsenkrebs auf Basis klinischer Daten. Ziel ist die Entwicklung prädiktiver Modelle mittels klassischer und ensemblebasierter Machine-Learning-Methoden.

## Inhalt

Die Jupyter-Analyse umfasst:

- Datenexploration und Aufbereitung eines UCI-Datensatzes
- Transformation kategorialer Merkmale mittels Binärkodierung, ordinaler Kodierung und One-Hot-Encoding
- Entwicklung und Vergleich mehrerer Klassifikationsmodelle:
  - Logistische Regression
  - Entscheidungsbaum
  - Random Forest (mit GridSearchCV)
  - XGBoost (mit Optimierung und SHAP-Erklärungen)
- Validierung der Modelle mittels Accuracy, Recall, F1-Score und ROC-AUC
- Modellinterpretation mit Feature Importances und SHAP-Werten

## Projektdaten

- **Datensatz**: Differentiated Thyroid Cancer Recurrence – UCI Machine Learning Repository
- **Beobachtungen**: 364
- **Zielvariable**: `Recurred` (0 = kein Rückfall, 1 = Rückfall)
- **Feature-Anzahl (nach Kodierung)**: 31

## Ergebnisse

- **Beste Modelle**: Random Forest und XGBoost
- **XGBoost-Recall (Rezidivklasse)**: 95 %
- **Wichtigste Prädiktoren**:
  - response_structural_incomplete
  - risk
  - age
  - n (Lymphknotenstatus)

Die Modelle erreichen eine sehr hohe Klassifikationsgenauigkeit und zeigen besonders im klinisch relevanten Recall für Rückfälle herausragende Werte. Die finale Version des Random-Forest-Modells wurde zur Wiederverwendung serialisiert.

## Projektstruktur

- `SS25_AML_Projekt_Nurullah_Kazak.ipynb` – Analyse- und Modellierungsnotebook
- `SS25_AML_FinalPaper_Nurullah_Kazak.pdf` – Abschlussbericht (wissenschaftliche Ausarbeitung)
- `best_random_forest_model.pkl` – Serialisiertes Modell (optional)

## Ausführung

1. Repository klonen:
   ```bash
   git clone https://github.com/USERNAME/aml-thyroid-recurrence-prediction.git
   cd aml-thyroid-recurrence-prediction
