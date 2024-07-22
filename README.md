![emist](https://github.com/user-attachments/assets/a9c30724-2bdf-411c-ae8c-3fa2e37dde43)

Emmision computes satellite by satellite.

![sat_pos](https://github.com/user-attachments/assets/25983d99-8157-4f41-ad89-6ce04f113378)

Satellite position computes.

![CA](https://github.com/user-attachments/assets/288e456d-60f0-41df-9c8e-883f05d94f84)

My satellites for C/A . There is 6 online satellites in my epoch. G13, G14, G15, G17, G19 and G30.

![elev](https://github.com/user-attachments/assets/b3d72e05-4d4f-4105-94c1-1af39618d454)

Elevation computes each satellite for Ionospheric delay.

![ion_result](https://github.com/user-attachments/assets/01afa5a3-6b91-425f-9bff-56b80ee6caac)

The purpose of this report is to outline the process of calculating station coordinates using GPS code observations with the least squares method. GPS (Global Positioning System) is a satellite-based navigation system that provides accurate positioning information. By analyzing code observations from GPS satellites, we can determine the coordinates of a station on the Earth's surface. The least squares method is commonly used to iteratively estimate the station's position by minimizing the residuals between observed and expected pseudoranges.
- GPS code observations: Collect the code observations from multiple GPS satellites at the station of interest. These observations include the pseudoranges, which are the measured distances between the satellites and the station.
- Satellite positions: Obtain precise satellite positions at the time of observation. These positions can be obtained from GPS ephemeris data or navigation messages.
- Initialization: Set an initial estimate for the station's coordinates (X=0, Y=0, Z=0).

- Iterative Least Squares:
a. Calculate expected pseudoranges: Using the current estimate of the station's coordinates and satellite positions, compute the expected pseudoranges.
b. Calculate residuals: Subtract the observed pseudoranges from the expected pseudoranges to obtain the residuals.
c. Build the design matrix: Differentiate the pseudorange equation with respect to the receiver coordinates to construct the design matrix.
d. Compute the weight matrix: Determine the measurement variances and form the weight matrix.
e. Solve the least squares equation: Multiply the design matrix by the weight matrix and solve the resulting linearized least squares equation to obtain the correction vector.
f. Update the receiver coordinates: Add the correction vector to the current estimate of the station's coordinates.
Check convergence: Calculate the differences in each component of the correction vector. If all differences are below a specified threshold (1 mm), the iterations can be terminated.
Magnitude of Corrections: Compare the values of the applied corrections (ionosphere, troposphere, and TGD) to the initial receiver coordinates. Assess whether the corrections are significant relative to the initial estimate.
Effect on Station Coordinates: Analyze the differences between the coordinates obtained from excluding and including corrections. Evaluate if there are notable deviations in the final position.