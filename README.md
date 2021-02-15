# NNDatcom
## Summary
Unpublished thesis paper on investigating the possibility of using of artificial neural networks to solve engineering problems.

## Concept
Goal: Understanding how to perform an analysis of an 3D aerodynamic shape using a solver comprised solely of Artificial Neural Networks trained using full-scale 3D Computational Fluid Dynamics Solvers. As demonstrated by even the largest ResNet which takes much less than 1 second to predict an answer even on a single GPU, it is theoretically possible to massively reduce the time to solve an extremely complex problem by "paying the price" of having a much longer data-generation and training period. As such techniques should first be created to reduce the length of these periods to scale to larger and more complex problems.

## Source code
The intention is to merge it into the current repo with the thesis at a later date. Most of the source code and an example of some result outputs can be found in a separate repo here: https://github.com/gavinIRL/NNDatcomSource

## Methodology
The first step to proving the basic concept is by using DATCOM, which is a semi-empirical method of estimating the performance of mostly aircraft-like shapes by outputting stability and dynamic control "derivatives". These derivatives general describe flight characteristics such as the performance (lift, drag) and reaction (change in angle of attack due to elevator deployment) of an aircraft for a given geometry. Written in FORTRAN in the 1970s and hence much less computationally expensive than CFD, DATCOM utilises formulae and look-up tables to estimate certain key performance characteristics of aircraft. While DATCOM is far from 3-Dimensional Computational Fluid Dynamics in terms of complexity and flexibility, it has the ability to generate a large dataset for training a neural network in a reasonable length of time on consumer-grade hardware. The equations and use of look-up tables make the output sufficiently difficult to solve for even in comparison to Computational Fluid Dynamics.

## Results and Conclusion 
There is clear evidence that a neural network can be trained to accurately solve difficult engineering problems given sufficient data and time to train. Some approaches have been adopted to artificially increase the input size to something resembling a typical 2-Dimensional CFD problem while maintaining the smaller output size and the accuracy is mostly unchanged with only the expected significant increase in training time.

## Next Steps
Expand the approach to a 2-Dimensional solver based entiely on CFD-generated datasets with the intention of creating a universal/general solver for fixed-size meshes, or at the very least a narrow but still usably broad solution envelope to further demonstrate the concept. And beyond that developing a 3-Dimensional Solver using CFD-generated datasets.

## Author Update February 2021
As hypothesized in the thesis paper there are several challenges to scaling up the output size (and to a lesser extent input size also). The author sadly turned down two offers of PhD studentships (in addition to the preferred third option collapsing prior to the Studentship offer being made) in favour of an alluring employment opportunity to be a Design Engineer in the area of aircraft engine testing. Therefore, the continuation of this branch of research has been relegated to a spare-time activity. 

Due to personal circumstances the author will be able to devote significantly more free time to continuing this research and therefore individual repos will be created and maintained documenting some of the alive and stale streams of code that have been written in the time since the thesis concluded, and will upload all future progress as they are created.

A list of all related repos will be maintained for reference below:
1) https://github.com/gavinIRL/NNDatcomSource
