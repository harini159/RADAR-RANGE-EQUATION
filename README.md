# RADAR-RANGE-EQUATION
Aim: 
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results 
through Python programming. 
Theory: 
The Radar Range Equation is a fundamental formula used in radar system design to determine the 
maximum range at which a radar can detect a target. It is given by: 

 
Procedure:
1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use 
Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 
2. Import Necessary Libraries: Import the math library in Python. 
3. Define the Radar Range Equation Function: Create a function to calculate the maximum range 
using the Radar Range Equation. 
4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, 
transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 
5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 
6. Execute the Program: Run the Python script to calculate and display the maximum range of the 
radar.

Program:
```
 
Pt = 1e3 
G = 30 
f = 10e9 
c = 3e8 
λ = c / f 
σ = 1 
L = 1.5
R = np.linspace(1e3, 1e3, 1000) 
 
Pr = (Pt * G**2 * λ**2 * σ) / ((4 * np.pi)**3 * R**4 * L) 
Pr_dBm = 10 * np.log10(Pr * 1e3) 
plt.figure(figsize=(10, 6)) 
plt.plot(R / 1e3, 
Pr_dBm,label=”Receive 
power”); 
plt.title("Received Power vs Radar Range") 
plt.xlabel("Range (km)") 
plt.ylabel("Received Power (dBm)") 
plt.grid(True) 
plt.legend() 
plt.tight_layout() 
plt.show()
```
OUTPUT:

<img width="785" height="715" alt="image" src="https://github.com/user-attachments/assets/0738c125-c078-4ef6-aefa-4d632423611c" />

Result:
Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python 
program. 
