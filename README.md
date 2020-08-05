## Earthquakes data analysis

In this project we are going study a dataset of earthquakes occurred in a time window of almost 30 years in South California. The catalog includes the magnitude, time of occurrence (s), and 3D coordinates (m) of each earthquake.

Interactive presentation:  	Earthquakes_notebook.ipynb

Module with all codes: Earthquakes.py

Main investigation: to study how the waiting time distribution between two consecutive earthquakes depends on the minimum magnitude considered (e.g. if we consider only earthquakes of magnitude 5 or greater we expect to wait longer times between two events, but how much longer than for example if we consider those of magnitude 4 or greater?).

**Main achievement**: detected waiting-time scaling property (and critical exponent) w.r.t. the magnitude threshold above which the earthquakes are considered. 

**More in depth**
The scaling phenomenon happens if two conditions are verified:
* the system is scale-free, i.e. it doesn't have any characteristic scale in the distribution of a given quantity, except a "correlation length" (that for example for the waiting times is given by the cutoff time);
* the exponent of the distribution is the same for all distributions.

More in concrete, if we have a distribution of a variable <img src="https://render.githubusercontent.com/render/math?math=\mathbf{x}"> (waiting time or distance) which scales in another variable <img src="https://render.githubusercontent.com/render/math?math=y"> (magnitude threshold or area of observation), to obtain the rescaled distribution <img src="https://render.githubusercontent.com/render/math?math=P(z)"> from <img src="https://render.githubusercontent.com/render/math?math=P_y(\mathbf{x}) = \mathbf{x}^{\delta} \cdot f(\mathbf{x}/\mathbf{x}_{cut}(y))"> we have to divide <img src="https://render.githubusercontent.com/render/math?math=\mathbf{x}"> for <img src="https://render.githubusercontent.com/render/math?math=\mathbf{x}_{cut}"> and multiply <img src="https://render.githubusercontent.com/render/math?math=P_y(\mathbf{x})"> for <img src="https://render.githubusercontent.com/render/math?math=\mathbf{x}_{cut}(y)">  (so that the distribution remains normalized).

In this way we obtain a unique powerlaw with critical exponent <img src="https://render.githubusercontent.com/render/math?math=\delta"> with a cutoff independent from the <img src="https://render.githubusercontent.com/render/math?math=y">. 

<img src='Supplementary material/time-scaling.png' >
