# Multi-Layer Lens Thermo-Mechanical Stress Simulation

This is an interactive web application designed to simulate and analyze the thermo-mechanical stress in various multi-layer lens structures. The primary goal is to identify the optimal design that minimizes the risk of delamination caused by the mismatch in the Coefficient of Thermal Expansion (CTE) among different materials when subjected to temperature changes.



## Key Features

- **6 Unique Case Studies**: Simulates six different structural designs, from a baseline case to complex combinations of buffer and protection layers.
- **Interactive Parameter Control**: Users can modify key material properties (Young's Modulus, CTE, Thickness, Width) and the operational temperature range (ΔT) to see their immediate impact on stress levels.
- **Real-time Stress Calculation**: The simulation calculates the maximum stress (in MPa) for each case based on a bi-layer thermo-mechanical stress model.
- **Advanced Stress Modeling**: The physics engine accounts for stress concentration at sharp geometric corners and the mitigating effects of protective layers.
- **Visual Feedback**: Each case is represented by a clear SVG diagram. An optional "Stress View" mode visualizes the points of highest stress concentration on the diagrams.
- **Comparative Analysis**: A bar chart provides an immediate comparison of the performance of all six designs, helping to quickly identify the most stable structure.
- **Responsive Design**: The interface is built with React and Tailwind CSS for a seamless experience on both desktop and mobile devices.

## Core Concepts Simulated

### Thermo-Mechanical Stress

When materials with different Coefficients of Thermal Expansion (CTE) are bonded together, a change in temperature (ΔT) causes them to expand or contract at different rates. This mismatch induces mechanical stress at the interface between the layers. The magnitude of this stress is a primary factor in predicting structural failure, such as delamination.

### Stress Calculation Model

The simulation employs a bi-layer stress formula that considers:
- **Young's Modulus (E)**: A measure of a material's stiffness.
- **Poisson's Ratio (ν)**: The ratio of transverse to axial strain.
- **CTE (α)**: The rate of thermal expansion.
- **Layer Thickness (t)**: The geometry of the layers.
- **Temperature Change (ΔT)**: The thermal load on the system.

The model calculates the maximum stress at the most critical interface for each design, providing a quantitative basis for comparison.

## Case Designs Under Analysis

1.  **Case 1: Baseline**: The lens is in direct contact with the primary organic layer, representing the highest potential CTE mismatch.
2.  **Case 2: Stress Buffer Layer**: A "Black Organic Layer" with an intermediate CTE is placed under the lens to serve as a stress buffer.
3.  **Case 3: Edge Protection**: A thin Silicon Nitride (SiNx) layer is added to protect the interface edges and mitigate stress concentration.
4.  **Case 4: Combined Solution**: Merges the benefits of the stress buffer layer (Case 2) and edge protection (Case 3).
5.  **Case 5: Sub-Lens Protection**: A full SiNx layer is deposited under the lens, acting as an adhesion promoter and stress mitigator.
6.  **Case 6: Sub-Lens & Buffer**: The most complex design, featuring a stress buffer layer and a conformal SiNx trench that encapsulates the lens base for maximum stability.

## Technology Stack

-   **Frontend**: React, TypeScript
-   **Styling**: Tailwind CSS
-   **Charting**: Recharts
-   **Icons**: Lucide React

## How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/waterfirst/stress_simulation.git
    cd stress_simulation
    ```

2.  **Install dependencies:**
    (Assuming a Node.js environment)
    ```bash
    npm install
    ```

3.  **Run the development server:**
    ```bash
    npm start
    ```

4.  Open your browser and navigate to `http://localhost:3000` (or the port specified by your development server).
