# iCalibrate

## Requirement:

Each sensor module comes with a datasheet that describes how with change of a certain set of parameter, the output signal changes. The relation between these parameters is determined in batch at the end of the manufacturing process. 

For developers, choosing the correct component is of paramount importance. Hence, these data sheets are carefully anaylyzed before placing orders or integrating with the considered hardware.

However, non-ideality is a concept known to all Engineers. The formulae for electronics are derived from concepts of physics and almost every quarter, numerous papers are presented which address the exceptions of the existing mathematical models and propose a new and more accurate one.

In practice, the output characterstics of sensors may change drastically. These undersired changes may be due to incompatibility or faulty design of the circuit.

## Proposed Solution:

Even if deviated from the expected results, there still exists relation between the considered parameter and output signal considering the intrinsic properties of the sensor. Leveraging this fact, it can be ssumed that it is possible to propose an alternate mathemcatical model for the characteristics of the sensor by empirical analysis. 

In earlier times, empirical analysis was generally avoided because of insenstivity and inaccuracy of the models at the time. Machine Learning based prediction models can solve this problem. 

## Implementation:

Taking the exaple of a strain gauge, which measures the force applied to it on basis of the output voltage, the first step is to acquire data of the change in input with change in force (concerned parameter). 

This data is taken to build and analyze regression models that predict output voltage based on the concerned parameter. 

## Procedure for the user:
An Excel file is uploaded in the repo. Edit the Values in the file once the Data Acquisition is completed and then simply run all cells of the notebook. 

The program ends with an I/O function where the user can simply enter the output voltage to see the value of concerened parameter.

## Improvements from Existing Systems:

### 1. Accuracy: 
#### 96%  

### 2. No need of further scaling and processing.
#### The output values will be in the same scale as that of the Training Data on which the model is built on.

### 3. Easy integration with embedded systems.
#### The sensors are usually connected to the IoT using some microcontroller or microcomputer. The coefficient matrix obtained after training can simply be transferred on the device or the program. This significantly reduces the efforts on edge processing.
