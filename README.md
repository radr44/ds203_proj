
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





