This project simulates steady-state 1D heat conduction in a slab (or cube with conduction only in the x-direction), assuming:

    Constant thermal conductivity

    Uniform internal heat generation

    Fixed boundary temperatures at both ends

It visualizes the temperature distribution across the length of the slab using a simple Python script with matplotlib.

Problem setup:

    Length of slab: 3 m

    Thermal conductivity (k): 43 W/m-K

    Internal heat generation (q): 120 W

    Temperature at hot end (T₁): 44°C

    Temperature at cold end (T₂): 40°C

The temperature profile follows the analytical solution to the heat equation:



The script calculates and displays:

    Temperature at various positions (in cm)

    The position of maximum temperature (stationary point)

    Maximum and minimum temperatures

    A temperature vs. position plot

Example output:

		stationary point: 1.02 m
  
		temp at point is: 45.46 °C
  
		Max temp: 45.46 °C
  
		Min temp: 40.54 °C
  
![Untitled](https://github.com/user-attachments/assets/ad690426-1555-4900-9fe9-8baf0607d9bf)
