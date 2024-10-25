# Physics with Python 👩‍💻 💙

In this project, we aim to use Python and Jupyter Notebook to solve a problem about Felix Baumagartner's free fall!

## Getting Started
This project helps you get familiar with Jupyter Notebook and the libraries `matplotlib` and `numpy`. You'll learn how to process data and represent it graphically.

## Objectives
- Part 1 : Exploitation of Experimental Data
- Part 2 : Modelisation of Free Fall
- Part 3 : Simulation of Felix Baumgartner's Free Fall

## Free Fall Simulation
One of the problems we solve is the simulation of free fall. Free fall is the motion of an object under the influence of gravitational force only. This simulation helps visualize the trajectory and velocity of an object in free fall.

In this project, we specifically analyze the experimental data from Felix Baumgartner's jump. He went to a dive into the sky and here we are using the data before he opended the parachute!! 

### Requirements
- Python 3.x
- `numpy`
- `matplotlib`
- Jupyter Notebook

You can install the required libraries using:
```sh
pip install numpy matplotlib
```

## Project Structure

## Our objectives with details 
- Part 1: Exploitation of Experimental Data
- Part 2: Modeling of Free Fall
- Part 3: Simulation of Felix Baumgartner's Free Fall

## Project Structure
The project is divided into three main parts:

### Part 1: Exploitation of Experimental Data
1. **Plotting Speed and Altitude Curves**:
   - Import the necessary libraries (`numpy` and `matplotlib`).
   - Use data from the files "Alt-Vit-Baumgartner.txt" and "Alt-Vit-son.txt".
   - Plot the speed of Baumgartner and the speed of sound as functions of altitude on the same graph, with the x-axis inverted (decreasing altitudes).

2. **Analyzing Maximum Speed**:
   - Determine the maximum speed reached by Baumgartner and the corresponding altitude.
   - Calculate the average speed up to 20 km altitude and over the entire free fall (before parachute deployment at 2.5 km altitude).

3. **Determining Supersonic Altitudes**:
   - Identify the altitudes where Baumgartner's speed exceeds the speed of sound.
   - Use regularly spaced altitude values (every 100 m) and interpolate Baumgartner's and the sound's speeds for these altitudes.
   - Find the altitudes where the interpolated speed of Baumgartner is greater than or equal to the interpolated speed of sound.

### Part 2: Modeling of Free Fall
1. **Force Analysis - Model with Constant Air Density**:
   - **Gravitational Force**:
     - Define the function `AccPes(z)` to calculate the gravitational acceleration as a function of altitude.
     - Calculate the gravitational acceleration for various altitudes and analyze its dependence on altitude.
   - **Drag Force**:
     - Define the function `Frott(v, rho)` to calculate the drag force as a function of velocity and air density.
   - **Equilibrium Condition and Maximum Speed**:
     - Calculate the theoretical maximum speed using a constant air density model and compare it with the measured maximum speed.

2. **Force Analysis - Model with Air Density Variation with Altitude**:
   - **Experimental Curve**:
     - Plot the experimental curve of air density as a function of altitude using data from "Alt-Masse-vol.txt".
   - **Atmospheric Model**:
     - Determine the expression for air density as a function of pressure and temperature using the ideal gas law.
     - Study the variations of air density with altitude using appropriate atmospheric models for different altitude ranges.
     - Define the function `MassVol_th(z)` to calculate theoretical air density as a function of altitude.
     - Plot the experimental and theoretical air density curves on the same graph.
     - Calculate the new theoretical maximum speed considering the variation of air density with altitude and compare it with the measured maximum speed.

### Part 3: Simulation of Felix Baumgartner's Free Fall
1. **Acceleration**:
   - Define the function `Accel(z, v)` to calculate Baumgartner's acceleration during free fall, considering the drag force and gravitational force.
   - Neglect the dependence of gravitational acceleration on altitude and fix it at \( g = 9.75 \, \text{m/s}^2 \).

2. **Euler-Cromer Method**:
   - Simulate Baumgartner's motion using the Euler-Cromer method to determine his acceleration, velocity, and altitude as functions of time.
   - Define the number of iterations and the time step (\( \Delta t = 52 \, \text{ms} \)).
   - Store the values of acceleration, velocity, and altitude in arrays and define the initial altitude.

3. **Analysis of Simulation Results**:
   - Determine the altitude at which Baumgartner opens his parachute and compare it with the measured value.
   - Plot the experimental and simulated velocity curves as functions of time and compare the maximum simulated velocity with the measured value.
   - Plot the histogram of relative errors between the experimental and simulated velocity curves.
   - Comment on the initial, zero, and final values of the acceleration curve.

## Contributing
If you are interested in a specific part, want more details, or found some mistakes, please send a merge request or open an issue, so we can chat about physics and code!
