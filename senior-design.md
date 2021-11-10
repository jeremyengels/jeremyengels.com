[Home page](https://jeremyengels.com)

# Active Suspension System

For my senior capstone project, my group chose to design an offroad trailer system. Since this was during COVID, we only had to design our project and not assemble any hardware — so my group decided to tackle a relatively large project. Our team consisted of 4 mechanical engineers (3 of whom focused on mechanical design, and I focused on controls), and 3 electrical engineers (who focused on the sensor implementation and power systems). 

### Problem Statement

In a search-and-rescue scenario in intensely offroad environments, patients must be transported and possibly operated upon over difficult terrain. Helicopter airlifts are often prohibitively expensive, both in operational costs and costs to the user (in the US around \$10k and \$40k respectively). However typical offroad suspension systems are inadequate for intensely rough terrain in mountainous or rocky environments.

### Our Solution

Our solution to this problem was a trailer which would be capable of being towed over very rough terrain by any common truck or Jeep. Additionally, since the injured patient could be in a critical condition, a bumpy ride could make injuries worse. For this reason we determined that the trailer must have some kind of active suspension system to minimize the acceleration felt by the passengers inside. 


### The Actuation System


### The Sensing System


### My Contribution: The Control System & General Architecture

So we have actuators and sensors. But what do we do with them? 

This is what most of my work went into for this project. The very cool part about this LiDAR architecture (and, to be fair, the _reason_ we included it in the first place), was to gain access to _future_ disturbance data. Depending on the speed the vehicle was traveling, we had anywhere between 1 and 5 seconds of estimated terrain height in front of the trailer. So the question is how do we implement this into the control system. 

The solution I designed was a combination of feedforward and feedback control. The block diagram for the full control system is shown below. 

