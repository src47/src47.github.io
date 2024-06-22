---
layout: page
---
                
### About Me 

I am a final year PhD student at Stanford University and SLAC National Accelerator Laboratory, advised by Professor [Mike Dunne](https://profiles.stanford.edu/Mike-dunne). My research focuses on developing AI-based methods to infer structural and dynamical materials properties from X-ray and neutron scattering experiments and to design targeted and intelligent data acquisition strategies. 

Prior to Stanford, I obtained an MPhil degree in Scientific Computing from Cambridge University under the supervision of Professor [David Wales](https://www.ch.cam.ac.uk/group/wales/person/dw34) and a BA in Chemistry from Pomona College under the supervision of Professor [Fred Grieman](https://www.pomona.edu/directory/people/frederick-j-grieman). 

### PhD Projects

#### Targeted materials discovery using Bayesian algorithm execution

<img src="images/bax_overview.png" width="750"/>

Very brief summary: this paper proposes several techniques to intelligently locate subsets of a material design space that are aligned with complex, user-defined goals. More details to come! For now, please check out our arxiv [pre-print](https://arxiv.org/abs/2312.16078) and [code](https://github.com/src47/multibax-sklearn) for further details!

#### Capturing dynamical correlations using implicit neural representations

<img src="images/machine_learning_la_final.jpg" width="750"/>
Graphic created by Gregory Stewart!

More details to come! For now, please check out our [publication](https://www.nature.com/articles/s41467-023-41378-4), [code](https://github.com/slaclab/neural-representation-sqw) and [press](https://www6.slac.stanford.edu/news/2023-10-12-new-ai-driven-tool-streamlines-experiments) article for further details!

#### Accurate Photonizing and Contrast Estimation for X-ray Photon Correlation Spectroscopy

<img src="images/josh_speckle.png" width="750"/>

Many important physical processes occur on very (very) short timescales (i.e. on the order of femtoseconds). At the Linac Coherent Light Source (LCLS), we study these phenomena using incredibly bright, pulsed X-rays; one technique is known as X-ray Photon Correlation Spectroscopy. At a high-level, the idea is to use extremely coherent light to collect scattering from individual atom positions as images known as speckles (an example image is shown above, courtesy of Josh Turner). 

To study dynamics, two sequential X-ray pulses are shot (with variable time-delay) at a sample to obtain two snapshots (X-ray speckle images) of the sample structure at different times. If the speckle images are the same at both time points, this implies that the structure has not changed between the two pulses. Conversely, if the X-ray images are very different, it implies that something has changed in the sample over that corresponding time-scale. By systematically changing the time-delay we are able to map out very complex processes in materials and create "molecular movies". 

<img src="images/LCLS_CNN.png" width="750"/>

The figure-of-merit for quantifying how two X-ray images are different is known as the contrast. The ultimate goal of our work is, therefore, to accurately estimate the contrast from X-ray detector images. In order to determine the contrast, it is first neccesary to count the number of photons hitting the detector at each pixel. Our input to the model is the raw detector image (which may have significant noise, charge-sharing etc) and our output is a sparse-matrix corresponding to the photon counts at each pixel (photonizing). In the image above, we show that we can accurately photonize the input using a CNN. 


Please check out our [publication](https://aca.scitation.org/doi/10.1063/4.0000161), [code](https://github.com/slaclab/ml_xpfs) and [press](https://www6.slac.stanford.edu/news/2022-11-07-artificial-intelligence-deciphers-detector-clouds-accelerate-materials-research) article for further details..

#### Automatic prediction of crystal lattice parameters from powder X-ray Diffraction data

Powder diffraction is a widely used X-ray based method used to study the structure of crystalline materials. These techniques are particularly insightful in allowing us to understand why particular materials have certain physical properties (such as strength, conductivity, stiffness etc). Using this knowledge, we are better able to intelligently design new materials with desired attributes. Currently, the analysis of powder diffraction data can take significant time and human effort, and therefore any efforts to automate this process will be very useful. 

<img src="images/crystal_ML.png" width="750"/>

In this project, we develop supervised learning models to predict the shape of the unit-cell of a crystal from simulated data as well as experimental data collected at the Stanford Synchrotron Radiation Lightsource (SSRL). As shown in the image above, the unit-cell shape is fully defined by six numbers, three lengths and three angles, and therefore this problem can be formulated as a standard non-linear regression task with six outputs. Please check out our [publication](http://scripts.iucr.org/cgi-bin/paper?vb5020) for more information.

