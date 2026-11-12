# Eda-Chiller-Fault-Detection-Diagnostics-Dataset

## Dataset Overview (From Kaggle)

Centrifugal chillers are critical components in modern HVAC systems, consuming significant electrical energy in large commercial and industrial buildings. Early and accurate Fault Detection and Diagnosis (FDD) is essential for maintaining energy efficiency, preventing unexpected shutdowns, and reducing maintenance costs.

This dataset (https://www.kaggle.com/datasets/phananh715/chiller-fault-detection-diagnostics-dataset) provides preprocessed telemetry sensor data optimized for developing, benchmarking, and evaluating machine learning and deep learning models for time-series classification and chiller fault diagnosis.

## Data Source (From Kaggle)

The dataset is derived from the benchmark ASHRAE Research Project 1043 (RP-1043), which contains experimental measurements collected under controlled conditions from a 90-ton water-cooled centrifugal chiller operating across various operating loads and fault severity levels.

## Data Collection & Physical Fault Injection (From Kaggle)

Unlike purely synthetic datasets generated via mathematical noise, this dataset originates from empirical experiments conducted on an actual industrial-grade **90-ton water-cooled centrifugal chiller testbed** under ASHRAE Research Project 1043.

The data generation adheres to rigorous physical measurement protocols:

- **Real Operational Testbed:** Run under dynamic, real-world cooling loads and condenser water conditions to capture genuine operational transients and system inertia.
- **Controlled Physical Fault Injection:** Faults were deliberately and physically introduced into the operating system rather than simulated via heuristic rules. For example:
  - _Refrigerant leaks and overcharges_ were realized by physically removing or adding controlled mass increments of refrigerant.
  - _Condenser fouling_ was simulated by physically restricting tube channels to emulate scale/deposit resistance.
  - _Non-condensables_ were induced by bleeding measured amounts of nitrogen/air into the circuit.
  - _Flow reductions and oil imbalances_ were directly actuated via throttling valves and precision oil injection/extraction.
- **Graded Fault Severity:** Each physical fault was evaluated across four progressive severity levels (SL1 to SL4) alongside varying thermal load ratios, capturing both subtle micro-deviations at early stages and acute system degradation.

## Fault Classes & Labels (From Kaggle)

The dataset covers normal operation along with several distinct typical chiller fault types, labeled by file name:

- **normal**: Normal baseline operation under standard operating conditions.
- **cf** _(Condenser Fouling)_: Accumulation of deposits or scaling on the condenser water tube surfaces, impairing heat transfer.
- **eo** _(Excess Oil)_: Overcharge of lubrication oil into the refrigerant circuit, degrading cooling performance.
- **fwc** _(Reduced Condenser Water Flow)_: Decreased water flow through the condenser due to valve or pump anomalies.
- **fwe** _(Reduced Evaporator Water Flow)_: Restricted chilled water flow across the evaporator.
- **nc** _(Non-condensable Gas)_: Presence of non-condensable gases (such as air) trapped inside the refrigerant circuit.
- **rl** _(Refrigerant Leak / Undercharge)_: Deficit in system refrigerant charge, reducing cooling capacity.
- **ro** _(Refrigerant Overcharge)_: Excess refrigerant charge, leading to elevated condenser pressure and compressor stress.

# EDA Outputs (see analysis.ipynb)

## Dataframe

![IMG](dataframe.png)

## Descriptive Statistics

![IMG](descriptive.png)

## 📊Sample Count by Class

![IMG](sample_count_by_class.png)

## 📊Sensor Distribution Matrix Across All 8 Classes

![IMG](key_features_boxplots.png)