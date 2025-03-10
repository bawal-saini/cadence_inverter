# cadence_inverter
A CMOS inverter design in Cadence Virtuoso using the GPDK 180nm technology process. This repository includes the schematic design, layout, DC and transient simulation results, and AV extraction. The design is absolutely following all rules, hence DRC and LVS are running without errors.
# CMOS Inverter in GPDK 180 Technology (Cadence Virtuoso)

This repository contains the design and simulation of a **CMOS inverter** using the **GPDK 180nm technology** process in **Cadence Virtuoso**. The project includes the schematic design, layout, DC and transient simulation results, and AV extraction. The design successfully passed both **Design Rule Check (DRC)** and **Layout vs Schematic (LVS)** verification without any errors.

## Design Overview

- **Technology**: The design is implemented using the **GPDK 180nm technology** process.
- **Schematic**: The CMOS inverter is built using **PMOS** and **NMOS** transistors. The schematic is created in the Cadence Virtuoso schematic editor.
- **Layout**: The layout is designed using the Cadence Virtuoso layout editor. It adheres to the design rules of the GPDK 180nm process to ensure manufacturability.

## Prerequisites

To run the design and simulations, you need:
- **Cadence Virtuoso** (version 6.1.8 or later)
- **Spectre simulator** (for DC and transient analysis)
- **GPDK 180nm technology** library (can be installed via Cadence's PDK installer)

## Design Steps

1. **Schematic Design**: The schematic of the CMOS inverter was created using Cadence Virtuoso's schematic editor. The inverter uses a **PMOS** and **NMOS** transistor configuration to achieve inversion of the input signal.
2. **Layout Design**: The layout of the CMOS inverter was designed with respect to the **GPDK 180nm** design rules. The layout was verified with **DRC** and **LVS** to ensure the design's correctness and compliance with the process technology.
3. **Simulations**: DC and transient analyses were run using **Spectre** to evaluate the inverter’s performance. Additionally, the voltage gain (AV) was extracted from the transient simulation results.

## Results

- **Transient Analysis**: The following plot shows the transient response of the CMOS inverter to a step input signal. Notice the propagation delay and voltage swing.
  ![Transient Analysis](images/transient-analysis.png)

- **DC Analysis**: The DC operating point of the CMOS inverter, showing the static characteristics of the transistors.
  ![DC Analysis](images/dc-analysis.png)

- **Layout**: The layout view of the CMOS inverter created using GPDK 180nm design rules.
  ![Layout](images/layout.png)

- **Design Verification**:
  - **DRC (Design Rule Check)**: The design was successfully verified using **DRC** in Cadence Virtuoso and passed without any errors, ensuring that the layout meets the required design rules for the 180nm process.
  - **LVS (Layout vs. Schematic)**: The layout was also verified against the schematic using **LVS**, and it passed without errors, confirming that the layout matches the schematic design.

## How to Run the Simulations (Step-by-Step)

1. **Clone this repository** to your local machine.
2. **Open Cadence Virtuoso** and set up the appropriate technology library (GPDK 180).
3. **Load the schematic**:
   - Open the **CMOS inverter schematic** from the `schematic/` folder.
   - Connect the required simulation components (voltage sources, probes, etc.).
4. **Run DC Analysis**:
   - In Virtuoso, go to the **Simulation -> Launch -> ADE** and set up the DC analysis.
5. **Run Transient Analysis**:
   - Set up the **transient simulation** with the appropriate time step and time parameters.
6. **Extract Voltage Gain**:
   - Measure the output response to the input signal and extract the voltage gain.
7. **Check LVS and DRC**:
   - **LVS** (Layout vs Schematic): Verify that the layout matches the schematic by running LVS in Cadence Virtuoso. Ensure the layout passes without errors.
   - **DRC** (Design Rule Check): Verify the layout against the design rules for GPDK 180nm by running DRC. Ensure the layout passes without any design rule violations.
   
After completing these steps, you should have the transient, DC, and AV results available. Additionally, the design passes both DRC and LVS checks, confirming its correctness.

## Dependencies

- **Cadence Virtuoso** (version 6.1.8 or later)
- **Spectre** simulator (for DC and transient analysis)
- **GPDK 180nm technology** library

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

