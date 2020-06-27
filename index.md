---
layout: page
---

#### Automatic prediction of crystal lattice parameters from powder X-ray Diffraction data

Powder diffraction is a widely used X-ray based method used to study the structure of crystalline materials. These techniques are particularly insightful in allowing us to understand why particular materials have certain physical properties (such as strength, conductivity, stiffness etc). Using this knowledge, we are better able to intelligently design new materials with desired attributes. Currently, the analysis of powder diffraction data can take significant time and human effort, and therefore any efforts to automate this process will be very useful. 

<img src="images/crystalML.png" width="750"/>

In this project, we develop supervised learning models to predict the shape of the unit-cell of a crystal from both simulated and experimental powder diffraction data collected at the Stanford Synchrotron Radiation Lightsource (SSRL). As shown in the image above, the unit-cell shape is fully defined by six numbers, three lengths and three angles, and therefore this problem can be formulated as a relatively standard regression task with six outputs. We hope to share some of our results soon! 

Collaborators: Richard Walroth, Vivek Thampy, Kevin Stone and Professor Evan Reed 
Supervisors: Chris Tassone, Daniel Ratner and Professor Mike Dunne 


#### Accurate photonizing and contrast estimation for X-ray Photon Correlation Spectroscopy 

Many important physical processes occur on very (very) short timescales (i.e. on the order of femtoseconds). At the Linac Coherent Light Source (LCLS), we study these phenomena using incredibly bright, pulsed X-rays; one technique is known as X-ray Photon Correlation Spectroscopy. Essentially, the idea is to shoot two sequential X-ray pulses (with variable time-delay) at a sample and obtain two snapshots (X-ray images) of the the sample structure at different times. If the X-ray images are the same at both time points, this implies that the structure has not changed between the two pulses. Conversely, if the X-ray images are very different, it implies that something has changed in the sample over that corresponding time-scale. By systematically changing the time-delay, therefore, we are able to map out very complex processes in materials and create "molecular movies". 

<img src="images/LCLS_CNN.png" width="750"/>

The figure-of-merit for X-ray images changing is known as the contrast. The ultimate goal of our work is, therefore, to accurately estimate the contrast from X-ray detector images. In order to determine the contrast, it is first neccesary to count the number of photons hitting the detector at each pixel. Our input to the model is the raw detector image (which may have significant noise, charge-sharing etc) and our output is a sparse-matrix corresponding to the photon counts at each pixel (photonizing). In the image above, we show that we can accurately photonize the input using a CNN. 

Collaborators: Yanwen Sun, Diling Zhu 
Supervisors: TJ Lane, Daniel Ratner and Professor Mike Dunne 

## Past Projects 

#### Neural Network Loss Landscapes 

<img src="images/disconnectivityGraphs.png" width="750"/>

collaborators: Philipp Veepoort, Alpha Lee and David Wales (PI)
   
#### JPL Research 

<img src="images/UVtime.png" width="750"/>

collaborators: Fred Grieman, Xu Zhang (PI)  

#### Machine Learning for cardiac ultrasound time-series data <a href="Papers/SPIE2017.pdf">[PDF]</a></div>

<img src="images/CardiacUltrasound.png" width="750"/>

collaborators: Baichuan Yuan, Geoffrey Iyer, Nuoyu Li, Xiaochuan Xu, Ruohan Zhan, Rafael Llerena, Jesse Yen and Andrea  Bertozzi (PI).




