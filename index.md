---
layout: page
---

I am a first-year PhD student at Stanford University and SLAC National Accelerator Laboratory, advised by Professor [Mike Dunne](https://profiles.stanford.edu/Mike-dunne). My primary research focuses on developing automatic data analysis methods for experiments in Chemistry and Materials Science. Some side interests include theoretical studies of machine learning loss landscapes and using computational methods to discover novel energy and biological materials! Prior to Stanford, I obtained an MPhil degree in Scientific Computing from Cambridge University under the supervision of Professor [David Wales](https://en.wikipedia.org/wiki/David_J._Wales) and a BA in Chemistry from Pomona College. 

## Projects

#### Automatic prediction of crystal lattice parameters from powder X-ray Diffraction data (2020 -- )

Powder diffraction is a widely used X-ray based method used to study the structure of crystalline materials. These techniques are particularly insightful in allowing us to understand why particular materials have certain physical properties (such as strength, conductivity, stiffness etc). Using this knowledge, we are better able to intelligently design new materials with desired attributes. Currently, the analysis of powder diffraction data can take significant time and human effort, and therefore any efforts to automate this process will be very useful. 

<img src="images/crystalML.png" width="750"/>

In this project, we develop supervised learning models to predict the shape of the unit-cell of a crystal from both simulated and experimental powder diffraction data collected at the Stanford Synchrotron Radiation Lightsource (SSRL). As shown in the image above, the unit-cell shape is fully defined by six numbers, three lengths and three angles, and therefore this problem can be formulated as a relatively standard regression task with six outputs. We hope to share some of our results soon! 

Collaborators: Richard Walroth, Vivek Thampy, Kevin Stone and Professor Evan Reed 
Supervisors: Chris Tassone, Daniel Ratner and Professor Mike Dunne 


#### Accurate photonizing and contrast estimation for X-ray Photon Correlation Spectroscopy (2020 -- )

Many important physical processes occur on very (very) short timescales (i.e. on the order of femtoseconds). At the Linac Coherent Light Source (LCLS), we study these phenomena using incredibly bright, pulsed X-rays; one technique is known as X-ray Photon Correlation Spectroscopy. Essentially, the idea is to shoot two sequential X-ray pulses (with variable time-delay) at a sample and obtain two snapshots (X-ray images) of the the sample structure at different times. If the X-ray images are the same at both time points, this implies that the structure has not changed between the two pulses. Conversely, if the X-ray images are very different, it implies that something has changed in the sample over that corresponding time-scale. By systematically changing the time-delay, therefore, we are able to map out very complex processes in materials and create "molecular movies". 

<img src="images/LCLS_CNN.png" width="750"/>

The figure-of-merit for X-ray images changing is known as the contrast. The ultimate goal of our work is, therefore, to accurately estimate the contrast from X-ray detector images. In order to determine the contrast, it is first neccesary to count the number of photons hitting the detector at each pixel. Our input to the model is the raw detector image (which may have significant noise, charge-sharing etc) and our output is a sparse-matrix corresponding to the photon counts at each pixel (photonizing). In the image above, we show that we can accurately photonize the input using a CNN. 

Collaborators: Yanwen Sun, Diling Zhu 
Supervisors: TJ Lane, Daniel Ratner and Professor Mike Dunne 

#### Visualizing and Interpreting Neural Network Loss Landscapes under Mislabelling and Reduced-Connectivity (2019)

Neural network loss landscapes are often incredibly complex functions of trainable parameters. Gaining a better understanding of the structure of these landscapes might be useful in allowing for the development of better optimizers and loss functions, thereby improving the predictive capacity of neural networks. Unfortunately, due to computational limitations, there has been relatively little work exploring the full structure of these non-convex functions. 

Our approach involves creating topological maps (disconnectivity graphs) of the surface, like those shown below. In these images, the vertical axis represents the neural network training loss. The branches of the graph correspond to the minima of the loss function. More specifically, each branch represents the vector of parameters containing the weights for the neural network, and terminates at a height on the vertical axis corresponding to the training loss function. The branches join together at regularly spaced intervals on the vertical axis when they can interconvert via pathways mediated by index one saddle points. The inspiration for such a decomposition comes from free energy lanscape physics, where minima correspond to stable molecular structures and index 1 saddle points correspond to transition states. 

<img src="images/disconnectivityGraphs.png" width="750"/>

In particular, our work focused on using disconnectivity graphs to study how the loss function for single-layered neural networks changes as deliberate errors (mislabelling) is introduced into the training dataset as well as how they change when connections between neurons are systematically broken. Our main findings show that the number of minima grow as the mislabelling fraction increases. For example, the image on the right corresponds to mislabelling ten percent of the dataset; the image on the left corresponds to control "clean" dataset. Here we color each minima by its performance on the test set as measured by AUC. Interestingly, the lowest training loss minima do not neccesarily correspond to the best test performance. 

To learn more about our work in this area, please check out the paper links! 

Paper: "Perspective: new insights from loss function landscapes of neural networks" <a href="https://iopscience.iop.org/article/10.1088/2632-2153/ab7aef/meta">[LINK]</a>
Thesis: "Machine Learning Landscapes for Neural Networks with a Single Hidden Layer." <a href="Papers/SPIE2017.pdf">[PDF]</a> 
Collaborators: Philipp Veepoort and Alpha Lee 
Supervision: Professor David Wales
   
#### Methane Oxidation on Mars (2017)

Based on current models (atmospheric flow and meteroite impacts), there should be a relatively substantial amount of methane on Mars. Therefore, it was very suprising when the Curiosity Mars Rover reported that almost no methane could be detected from its measurements. Our project essentially studies the reason for this discrepency. Our hypothesis is that UV light from the sun activates a molecule known Magensium Perchlorate and causes it to oxidize methane into other carbon derivatives. We performed infrared spectroscopy measurements on a cell containing Magnesium Perchlorate and UV light. 

<img src="images/UVtime.png" width="750"/>

Shown above is the effect of irradiating Magnesium Perchlorate with UV light over time. In particular, note the large peak that grows between 1200 and 1500 wavenumbers. This peak corresponds to formation of various (previously uncharacterized) chlorine derivatives. Thus, our experiment shows that UV light can activate the surface of Magnesium Perchlorate. Future work will likely include studying how this activated surface interacts with methane. 

Supervisors: Xu Zhang and Professor Fred Grieman 

#### Studying Heart Ultrasounds via Unsupervised Learning <a href="Papers/SPIE2017.pdf">[PDF]</a> (2016)

<img src="images/CardiacUltrasound.png" width="750"/>

Collaborators: Geoffrey Iyer, Nuoyu Li, Xiaochuan Xu, Ruohan Zhan, Rafael Llerena, Jesse Yen 
Supervisors: Baichuan Yuan and Professor Andrea Bertozzi




