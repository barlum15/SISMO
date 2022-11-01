# SISMO
SISMO - SImulation of Slime MOlds

# WHAT IS IT?

The SISMO (SImulation of Slime MOlds) simulates spreading during foraging by the slime mold of the species Physarum polycephalum in NetLogo.
Version 6.2.2 http://ccl.sesp.northwestern.edu/netlogo/6.2.2/

![alt text](https://github.com/barlum15/SISMO/blob/main/SISMO.jpg?raw=true)
![alt text](https://github.com/barlum15/SISMO/blob/main/SISMO_with_network.jpg?raw=true)

# HOW IT WORKS

Initially, the food sources are placed randomly. The core of the slime mold, the plasmodium, is placed centrally in the world. The fixed number of pseudopodia then swarm out to search for food. When a food source is found and the nutrients are depleted, new pseudopodia are hooked with some probability. If food sources are still available, the slime mold will continue to search for them. The shortest paths between food sources and plasmodium are represented by thicker yellow tubes. In nature, the distinct veins of the slime mold are used to transport food. The shortest path is determined using the A* algorithm.

# HOW TO USE IT

Click the SETUP button to set up the pseudopodium (the yellow blob, in the center) and the selected number of foodsources and the selected number of initial pseudopodia. Click the GO button to start the simulation. The movements of the pseudopoida are represented by yellow lines.

The AMOUNT-PSEUDOPODIA slider sets the number of initial pseudopodia.

The slider AMOUNT-FOODSOURCES sets the number of food sources.

The SHOW-NUTRIENT-VALUE switch determines whether the number of nutrients from the food sources should be displayed or not.

The switch SHOW-NETWORK determines whether the created network (blue dots), which is needed for the A* algorithm, should be displayed or not. 

The switch SHOW-INTERSECTION-POINTS determines whether the calculated intersection points (red crosses at the intersections of  the pseudopodia) should be displayed or not.

# THINGS TO NOTICE

The duration of the simulation can vary greatly depending on the number of food sources and the number of selected pseudopodia. A higher number of pseudopodia and food sources results accordingly in a longer simulation time.
The speed should be set slower to make the spreading of the slime mold more vivid.

# THINGS TO TRY

Change the number of pseudopodia and food sources. Display Nutrient values to see how quickly the pseudopodia consume them. Furthermore, the network points can be displayed. If this is the case, then one can see how the network is constructed for the A* algorithm. Furthermore the found intersection points can be displayed.

# EXTENDING THE MODEL

Since the simulation takes quite a long time, one could consider improving the performance. Also, the calculations of the intersections could be outsourced to Python, for example, and the calculations could be run in parallel there.
Furthermore, one could let the pseudopodia disappear over the time. Since slime molds also do this in nature. Only the important thick veins remain the longest.

# NETLOGO FEATURES

`create-link-with` is used to create the links at the intersection points.
`one-of` is used to check if there is already an existing network point at the current coordinates, so that more network points are not created unnecessarily.
`one-of` is used when the nutrients of the foodsource are exhausted to determine the end point for the A* algorithm.

# RELATED MODELS

The A* algorithm used in this model is based on the A* algorithm programmed by Fernando Sancho Caparrini in Netlogo and is adapted for the SISMO: 
http://www.cs.us.es/~fsancho/
https://github.com/fsancho/IA/blob/542a152c7920ec8606656b6c9a46cd4545fc2175/11.%20Machine%20Learning/Self%20Organizing%20Maps/Nav%20Robot/Geom%20A-star.nls

# CREDITS AND REFERENCES

Fernando Sancho Caparrini - "A General A* Solver in NetLogo"
http://www.cs.us.es/~fsancho/?e=131

# COPYRIGHT AND LICENSE

Copyright 2022 Emir Sinanovic & Kristina Wogatai.

![CC BY-NC-SA 3.0](http://ccl.northwestern.edu/images/creativecommons/byncsa.png)

This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 License.  To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/3.0/ or send a letter to Creative Commons, 559 Nathan Abbott Way, Stanford, California 94305, USA.

This model was developed at the university Klagenfurt in a collaboration between Emir Sinanovic and Kristina Wogatai in the course of the connected master theses "Simulation and Mobility Planning
with a Slime Mold Based Algorithm" and "SISMO (SImulation of Slime MOlds):  A Slime Mold Based Algorithm and its Application in Traffic Management". 
