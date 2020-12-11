
# DS 203: Course Project
## Potentially Hazardous Asteroid Identification:
<p float="left">
<img src="https://s3.india.com/wp-content/uploads/2020/11/as-2.jpg" alt="drawing" height="220" width="300" align="left"/>
<img src="https://cdn.mos.cms.futurecdn.net/hxR7V9GtT6StwNYpCa2ghK-1200-80.jpeg" alt="drawing" height="220" width="310" align="center"/>
<img src="https://static.independent.co.uk/s3fs-public/thumbnails/image/2015/06/29/16/asteroid-alamy.jpg" height="220" width="300" align="right"/>
</p>

### Introduction:
In terms of orbital elements, NEOs (Near Earth Objects) are asteroids and comets with perihelion distance less than 1.3 astronomical units.Since their orbital paths often cross that of the Earth, collisions with near-Earth objects have occurred in the past and we should remain alert to the possibility of future close Earth approaches.The orbit of the asteroid is not very easy to determine considering the number of celestial bodies that influence their trajectory through gravitational forces. As far as, asteroids are
concerned, there are many asteroids called near-earth asteroids, but all are not hazardous.

Potentially Hazardous Asteroids (PHAs) are currently defined based on parameters that measure the asteroid's potential to make threatening close approaches to the Earth. In these report we try a data driven approach to study the parameters the make an asteroid as a PHA. We considered various parameters from the data collected online through multiple sources. These parameters were analysed for the effect they have on they have on the asteroids level of hazard and redundant parameters were eliminated. Different machine learning models we trained on this data in order to identify an optimal classifier that can used for the purpose of Potentially Hazardous Asteroid Identification and prediction models were identified to predict the of minimum orbit intersection distance.

In this project, we predict the threat level of an asteroid from some measureable parameters - Eccentricity of Orbit, Relative Velocity, Absolute Magnitude etc.
________________
### Approach:
The approach presented in the report differs from the common statistical treatment of NEAs andrelies mainly on the application of machine learning techniques.In general, machine learningframeworks are particularly well-suited for function approximation and recognizing complexpatterns and hidden in multidimensional datasets.

In our particular case,  because we are no longer reliant on calculations that attempt to esti-mate the asteroids position at a particular point in time, the machine learning based approachis more resilient to perturbations of the initial conditions, that is, chaotic motion.We did notuse artificially generated data with perturbations because this was causing many models as theparameters are of different scales of magnitudes and may have a complicated non linear re-lationship that could cause slight perturbations of different parameters in the data to defy theunderlying physics that is involved in the problem to different scales, may end up confusing theclassifier ie the classifier may adopt a method where it classifies the artificial data correctly andthe real data would be wrongly classified.

The problem at hand is a discrete binary classification task, where the two mutually exclusiveclasses for the observed objects.  Several models have been analysed ranging from Linear re-gression and Random forests to support Vector machines and Neural networks.The cleaned dataused in the consisted of 16 element uncorrelated fields which were passed on to the potentialclassifiers.
_______________
### Datasets:
* For this project, we collected our datasets from multiple sources. The major sources of data for this project are: 

[https://ssd.jpl.nasa.gov/sbdb_query.cgi](https://ssd.jpl.nasa.gov/sbdb_query.cgi)

[https://cneos.jpl.nasa.gov/](https://cneos.jpl.nasa.gov/)

[https://theskylive.com/near-earth-objects](https://theskylive.com/near-earth-objects)

[https://sbn.psi.edu/pds/archive/asteroids.html](https://sbn.psi.edu/pds/archive/asteroids.html)

[European Space Agency (ESA)](http://neo.ssa.esa.int/close-approaches)

* Some more datasets used for this project are: 

[https://data.world/texas-whiskey/discoverable-datasets/workspace](https://data.world/texas-whiskey/discoverable-datasets/workspace)

[https://data.world/qwofford/hazardous-asteroid-orbits](https://data.world/qwofford/hazardous-asteroid-orbits)

____________________
### Definitions:
1. **Near Earth Object:** A Solar System body is a NEO if its closest approach to the Earth (perihelion) is less than 1.3 astronomical units (AU). 
2. **Potentially Hazardous Object:**  A near-Earth object with a minimum orbital intersection distance with Earth of less than 0.05 astronomical units and an absolute magnitude of 22 or brighter.
3. **NEO Reference ID:** A unique number assigned to every near-Earth asteroid.
4. **Absolute Magnitude:** the visual magnitude an observer would record if the asteroid were placed 1 Astronomical Unit (au) away.
5. **Relative velocity:** The velocity of the asteroid when observed from Earth.
6. **Miss distance:** The distance below which the asteroid will pose a serious threat.
7. **Orbit ID:** N A unique number assigned to every observed orbit of the near Earth objects. More than one asteroid can share the same orbit.
8. **Minimum Orbit Intersection:**  A measure used in astronomy to assess potential close approaches and collision risks between astronomical objects.
9. **Jupiter Tisserand Invariant:** a value calculated from several orbital elements, used to distinguish different kinds of orbits.
10. **Eccentricity:** A dimensionless parameter that determines the amount by which its orbit around another body deviates from a perfect circle.
11. **Inclination:** The orbital inclination measures the tilt of an object's orbit around a celestial body. It is expressed as the angle between a reference plane and the orbital plane or axis of direction of the orbiting object.
12. **Asc Node Longitude:** The ascending Node Longitude is the angle from the origin of longitude, to the direction of the ascending node, as measured in a specified reference plane.
13. **Orbital Period:** The time a given astronomical object takes to complete one orbit around another object.
14. **Perihelion:** The perihelion is the point in the orbit of a planet, asteroid or comet that is nearest to the sun.
15. **Aphelion:** The aphelion is the point in the orbit of a planet, asteroid or comet that is farthest from the sun.
16. **Perihelion Arg:** It is the angle from the body's ascending node to its perihelion, measured in the direction of motion.
17. **Mean motion:** It is the angular speed required for a body to complete one orbit, assuming constant speed in a circular orbit.
18. **Albedo:** It is a measurement of the amount of light reflected from the surface of a celestial object, such as a planet, satellite, comet or asteroid.
19. **Mean Anomaly(ma):** The fraction of an elliptical orbit's period that has elapsed since the orbiting body passed the nearest point of the orbit to the epicenter, expressed as an angle which can be used in calculating the position of that body in the classical two-body problem.
20. **Rotation Period (rot per):** The time that the object takes to complete a single revolution around its axis of rotation relative to the background stars
___________________

#### Models Used:
* For the Machine Learning Part of this project, the models we have used are:
  * Simple Linear Regression
  * Linear Regression with an L1 penalty (Lasso Regression)
  * Linear Regression with an L2 penalty (Ridge Regression)
  * Random Forest Regressor
  * Support Vector Machine
  * Neural Network
* Different Hyperparameters were tested for each model to fine tune the model and optimise the predictions.
_________________
