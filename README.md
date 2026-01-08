# mpr-animating-aos

A repository associated with the manuscript demonstrating Artificial Organisms (AOs) animated by the Mathematical Principles of Reinforcement (MPR).

## Overview

This repository contains Jupyter notebooks that simulate behavioral responses using the Mathematical Principles of Reinforcement framework. The notebooks implement MPR equations to model arousal, coupling, and response rates across different reinforcement schedules.

## Notebooks

The repository includes four main notebooks, each focusing on different reinforcement schedule configurations as demonstrated in the accompanying manuscript:

### 1. `AOs_MPR_single_VR.ipynb`
- **Focus**: Single Variable Ratio (VR) schedules
- **Description**: Demonstrates basic MPR model implementation with VR schedules. Includes a basic demo showing how the model works, with simulations of arousal, coupling, and response rate dynamics.

### 2. `AOs_MPR_single_VI.ipynb`
- **Focus**: Single Variable Interval (VI) schedules
- **Description**: Simulates AOs across a range of single VI schedules. AOs are sequentially exposed to different VI schedule values, tracking how arousal and coupling evolve over time.

### 3. `AOs_MPR_concurrent_VR.ipynb`
- **Focus**: Concurrent Variable Ratio (VR) schedules
- **Description**: Models choice behavior between two concurrent VR schedules. Includes changeover delay (COD) mechanisms and choice probability calculations based on coupling strengths.

### 4. `AOs_MPR_concurrent_VI.ipynb`
- **Focus**: Concurrent Variable Interval (VI) schedules
- **Description**: Simulates choice behavior between two concurrent VI schedules. Tracks arousal and coupling for both alternatives, with COD constraints on switching between options.

## MPR Model Components

The notebooks implement key MPR equations:

1. **Arousal (A)**: Updated recursively based on reinforcement events (r)
   - `A_t = α * (a * r_t) + (1 - α) * A_{t-1}`

2. **Response Constraint**: Total response rate based on arousal and motor constraint (δ)
   - `b_total = (1 / δ) * (A / (1 + A))`

3. **Coupling (C)**: Directional control, updated toward schedule-sensitive asymptote
   - `b_target = C * (1 / δ) * (A / (1 + A))`
   - Schedule-specific coupling asymptotes (C*) for FR, VR, FI, and VI schedules

## Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Requirements

See `requirements.txt` for a complete list of dependencies. Key packages include:
- `numpy` - Numerical computations
- `pandas` - Data manipulation
- `scipy` - Statistical functions and optimization
- `matplotlib` - Plotting
- `seaborn` - Statistical visualization
- `scikit-learn` - Machine learning utilities (for concurrent schedule analyses)
- `tqdm` - Progress bars
