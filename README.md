 # EVALUATION-OF-RADAR-RANGE-USING-PYTHON-
# NAME : KRISHNA KUMARI E
# REG NO :  212224060127
__Aim__:

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results 
through Python programming.

__Theory__:

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum 
range at which a radar can detect a target. It is given by:

<img width="573" height="442" alt="image" src="https://github.com/user-attachments/assets/ba374d30-d11f-41e5-a4fc-a42dde71d8e7" />

__Procedure__:

1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use 
Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 
2. Import Necessary Libraries: Import the math library in Python. 
3. Define the Radar Range Equation Function: Create a function to calculate the maximum range using 
the Radar Range Equation. 
4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, 
transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 
5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 
6. Execute the Program: Run the Python script to calculate and display the maximum range of the radar.


# Algorithm__:
1.Set values for power, gain, frequency, speed of light, and other constants. 
2.Calculate wavelength = speed of light ÷ frequency. 
3.Create a list of distances (range). 
4.For each distance: 
5.Calculate received power using the radar formula. 
6.Convert received power to dBm.

# PROGRAM :
```
import numpy as np 
import matplotlib.pyplot as plt 
Pt = 1000 
G = 1000 
f = 10e9 
c = 3e8 
lambda_ = c / f 
sigma = 1 
L = 1 
R = np.linspace(1e3, 1e5, 1000) 
Pr = (Pt * G**2 * lambda_**2 * sigma) / (((4 * np.pi)**3) * R**4 * L) 
Pr_dBm = 10 * np.log10(Pr * 1e3) 
plt.figure(figsize=(10, 6)) 
plt.plot(R, Pr_dBm, color='blue', label='Received Power (dBm)') 
plt.xlabel('Range (m)') 
plt.ylabel('Received Power (dBm)') 
plt.title('Radar Received Power vs Range (Inverse Form)') 
plt.grid(True) 
plt.legend() 
plt.gca().invert_yaxis() 
plt.tight_layout() 
plt.show() 
```

# Output__:
 <img width="676" height="398" alt="image" src="https://github.com/user-attachments/assets/a06d317f-f54a-4b92-be0c-03d4c6fc4264" />
  
# Result :
Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program. 

   




