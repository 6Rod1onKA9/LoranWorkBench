# Development of an Application for LORAN Measurement Visualization

**Objective:**
Develop an application that reads data from the emulated LORAN measurement service provided as a Docker image and visualizes the positions of the object and base stations on a graph in Cartesian coordinates.

# Theoretical Information

**LORAN** (Long Range Navigation) is a hyperbolic navigation system that uses the time difference of arrival (TDoA) of signals from several base stations to determine the location of an object. To accurately determine the position in a two-dimensional space, at least three fixed base stations are required.

LORAN systems are used for long-distance navigation, employing radio signals to calculate the distances between the base stations and the receiver.

*Hyperbolic Positioning*

**Hyperbolic positioning** is a method for determining the location of an object or signal source based on measuring the time differences of arrival (TDoA) of signals from the object to multiple receivers located at known points. This method is widely used in navigation, radar, and mobile phone location systems.

The principle behind hyperbolic positioning is that the difference in the time of arrival of signals from the source to different receivers forms hyperbolic lines of positions. Each pair of receivers forms a hyperbola on the plane, representing the set of points that have the same difference in distances to these two receivers. The location of the signal source is found along this hyperbola.

To determine the location of a receiver in a two-dimensional space, at least three signal sources are required to form two hyperbolas. The intersection of these hyperbolas determines the location of the receiver. In three-dimensional space, at least four signal sources are required to form three hyperbolas and determine the location in three dimensions.

*Least Squares Method*

The **Least Squares Method** (LSM) is a method used to determine the coordinates of an object by minimizing the sum of squared deviations between measured and computed values. This method allows finding the best approximation of the object's position when measurements contain errors or noise. It is applied to problems such as trilateration, triangulation, and multilateration, where distances, angles, or time differences of signal arrival are used to estimate the object's position.

*Gradient Descent*

**Gradient Descent** is an iterative numerical optimization method used to minimize a loss function. It allows finding model parameters that reduce errors in estimating the object's coordinates. Gradient Descent is widely applied in coordinate determination tasks where the goal is to minimize the difference between the measured and calculated values of distances, angles, or signal arrival times.

# Tasks

**Develop an application to display the position of the object and base stations:**

- Develop a web application that connects to the WebSocket server and reads the signal reception times from the base stations.
- Use the time differences of signal arrivals to calculate the location of the object.
- Display the received data on a Cartesian coordinate graph.

**Processing and visualization of data:**

- Process the data received through WebSocket and display the position of the object and base stations on a graph.
- Calculate the object's coordinates using the least squares method and gradient descent.

**Graph configuration:**

- Display the coordinates of the base stations and the object in Cartesian coordinates.
- Use different colors or styles of points to represent the base stations and the object.

# Solution

**User interface of the application:**

