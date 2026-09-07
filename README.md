# Formula 1 Tire Degradation & Pit Stop Strategy

Computational analysis of Formula 1 race performance, tire degradation, and pit stop strategy using real-world race data.

## Overview

This project investigates how tire degradation and pit stop strategies affect lap-time performance in Formula 1.

The analysis combines real race data with a simplified computational model to study lap-time evolution throughout a race and evaluate a hypothetical reduction in tire degradation.

The project focuses on the **2023 Bahrain Grand Prix** and **2023 Italian Grand Prix (Monza)**.

## Research Question

How does tire degradation affect Formula 1 lap-time performance, and how could a reduction in the degradation coefficient influence race performance and pit stop strategy?

## Methodology

The project was developed in Python using the **FastF1** library to collect and analyze Formula 1 timing data.

The analysis was divided into three main stages:

### 1. Lap-Time Analysis

Race lap times were analyzed to investigate how performance changed throughout each stint.

The analysis considers:

* Lap-by-lap performance
* Changes in race pace
* Tire stints
* Differences between stages of the race

### 2. Pit Stop Analysis

Pit stop data was analyzed to investigate the relationship between pit stops, tire changes, and changes in lap-time performance.

### 3. Tire Degradation Simulation

A simplified linear degradation model was used:

**T(n) = T₀ + k · n**

where:

* **T(n)** = simulated lap time
* **T₀** = lap time with a new tire
* **k** = tire degradation coefficient
* **n** = number of laps completed on the tire set

A hypothetical scenario was then simulated by reducing the degradation coefficient by **10%**:

**k' = 0.9k**

This scenario does not represent an actual change to Formula 1 tire compounds. Instead, it was used as a computational experiment to evaluate how lower degradation could affect lap times.

## Results

### Bahrain Grand Prix — 2023

The simulation showed that the reduced-degradation scenario began producing a difference of approximately **0.1 seconds per lap around lap 12**.

The maximum simulated difference was approximately **0.39 seconds**, occurring around **lap 34**.

This indicates that even a relatively small reduction in the degradation coefficient can accumulate into a noticeable lap-time advantage over a long stint.

### Italian Grand Prix — 2023

For Monza, the first difference of approximately **0.1 seconds** appeared around **lap 13**.

The maximum simulated difference was approximately **0.43 seconds**, occurring around **lap 51**.

The results illustrate how the effect of degradation accumulates over the number of laps completed on the same tire set.

## Technologies

* **Python**
* **FastF1**
* **Pandas**
* **NumPy**
* **Matplotlib**

## Project Structure

F1-Tire-Degradation/
│
├── data/
├── analysis/
├── simulation/
├── figures/
├── README.md
└── requirements.txt
```

## Limitations

The tire degradation model used in this project is intentionally simplified.

Real Formula 1 tire degradation is affected by several factors, including:

* Tire compound
* Track characteristics
* Track temperature
* Tire temperature
* Fuel load
* Driving style
* Traffic
* Weather conditions
* Tire management

Therefore, the simulation should be interpreted as a **computational model and hypothetical optimization scenario**, rather than an exact physical representation of tire behavior.

## Future Work

Possible extensions of this project include:

* Implementing nonlinear tire degradation models
* Comparing different tire compounds
* Incorporating fuel-load effects
* Simulating alternative pit stop strategies
* Comparing multiple drivers and races
* Implementing numerical optimization to determine optimal pit stop windows

## Data Source

Race timing data was obtained through the **FastF1** Python library.

## Author

**Maria Laura Neidorf**

Brazilian high school student interested in aerospace engineering, Formula 1, computational methods, numerical analysis, and STEM research.
