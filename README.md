# Cruise Control Simulation with Simulink

## Objective
This project simulates a cruise control system for a vehicle using MATLAB/Simulink. The system is designed to maintain a constant speed by balancing applied force and drag force under various conditions.

## System Dynamics
The vehicle dynamics are modeled using the following equation:
\\[
\\frac{dv}{dt} = \\frac{F}{m} - kv
\\]

### Parameters:
- **F**: Force applied to the vehicle (N).
- **m**: Vehicle mass (kg).
- **k**: Drag coefficient (resistance due to air or terrain).
- **v**: Vehicle speed (m/s).




## Model Description
The Simulink model is composed of the following blocks:
- **Constant Block**: Represents the applied force (F).
- **Gain Blocks**: Models inverse mass (1/m) and drag coefficient (k).
- **Integrator Block**: Computes speed by integrating acceleration over time.
- **Sum Block**: Combines forces to calculate net acceleration.
- **Product Block**: Calculates drag force (kv) by multiplying speed and the drag coefficient.
- **Scope Block**: Displays the speed vs. time graph for analysis.



## Scenarios Simulated
1. **Flat Road (Default Conditions)**
   - Drag coefficient: k = 1.0
   - Steady-State Speed: ~1.0 units
   - Time to Stabilize: ~3 seconds

2. **Uphill Road (Increased Resistance)**
   - Drag coefficient: k = 1.5
   - Steady-State Speed: ~1.2 units
   - Time to Stabilize: ~4 seconds

3. **Downhill Road (Reduced Resistance)**
   - Drag coefficient: k = 0.5
   - Steady-State Speed: ~0.7 units
   - Time to Stabilize: ~3 seconds


## How to Run the Model
1. Open the `CruiseControl_FinalModel.slx` file in MATLAB/Simulink.
2. Configure the desired parameters in the Constant Block (force, F) and Gain Blocks (1/m, k).
3. Run the simulation by clicking the **Run** button.
4. Observe the results in the Scope Block.

## Future Improvements
- Integrate a PID controller to dynamically adjust force based on speed error.
- Simulate time-varying drag coefficients for more realistic road conditions.
- Incorporate terrain profiles (e.g., slopes) for advanced testing scenarios.

## Author and Links
- **Author**: Vishnu PV
- **GitHub Repository**: https://github.com/vishnupv7


## Results and Observations
The simulation demonstrated stable and predictable behavior under all tested conditions. The system successfully adapts to varying drag forces, showcasing the fundamental functionality of a cruise control system. The results validate the reliability and consistency of the model.
