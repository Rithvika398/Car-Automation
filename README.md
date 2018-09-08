Project Title: Car Automation System

Aim:To design a car automation system.The system must have values of the parameters of the car(such as speed, mileage etc) and also the conditions
     of the environment(Rainy season, wet roads,etc) The system must determine the best path for reaching the destination(There may be more than one path at a particular point
     System must select the best one depending on weights assigned to the parameters, for example, road with potholes is likely to cause more damage than wet road). It
     must also keep track of how much fuel will be needed to reach the destination,and if the current fuel level is not sufficient,it must
     provide the best possible alternative for the car to reach the destination)(The output should be something like this-Take left, reduce speed because wet road, Keep toward right,
    take right,increase speed on highway)

Analysis of Problem statement: The car automation system requires us to select the best possible route from a particluar source to a particular destination by optimizing:
                               1) time taken along a certain path
                               2) fuel optimization for the given path
                               3) damage to the car based on the road conditions
                               4) total amount of fuel required to cover the entire journey
                               
                               Thus we optimize all the above 4 quantities, by training the given datasets and then based on the user inputs of source
                               and destination we will find the best possible route from source to destination.

                               Step 1:Decide user inputs and outputs
                               Step 2: Identify list of attributes to be trained
                               Step 3: Create datasets with the given attributes
                               Step 4:Train the datasets
                               Step 5:Create a graph where each node represents a location
                               Step 6:Based on user inputs of source and destination, find all possible paths
                               Step 7:Based on user inputs of other parameters, test the datasets for each possible path
                               Step 8:Obtain the optimized path

Tools used: 1) Java-to create the graph, accept user inputs and display outputs
            2) Weka-to train the datasets and test the user inputted parameters o optimize the selected attributes

Implememntation:
                Step 1:
                        User inputs: a.source
                                     b.destination
                                     c.Tank capacity
                                     d.Maximum speed of the vehicle
                                     e.Mileage of tha car
                        Predictions: Time Multiplication factor
                                     Optimized path
                                     Damage to the vehicle
               Step 2:

                        Attribute:1)Traffic
                                  2)Potholes
                                  3)No. of Signals
                                  4)Weather
                                  5)Tyre Grip
                                  6)pickup of the engine
                                  7)day of the week
               Step 3: For each of the subroutes we created a dataset with 20-25 cases to train the data
               
               Step 4: These datasets(with.arff extension)  were inputted to weka. Weka then trained each of the datasets and by using the 
                       appropriate algorithm we were able to get the percentage accuracy of predicting the target variables i.e.time and fuel
               Step 5,6: Using Java, we created a graph and hard coded the routes that exist between the nodes of the Graph. we the  predicted
                         all the possible routes from source to destination.

               Step 7:We used Wekas results to find the optimized path

               Step 8: The optimized path is displayed along with directions from sorce to destination, information about total fuel consumed, whether
                       the car has enough fuel to make the journey. If the fuel is insufficient, we have also considered whether petrol pumps exist along the way
                       and therefore if the tank can be refilled and the jorney can be completed. Each of the attributes are considered while choosing the optimized path
                       For example: Some routes may remain shut on Sundays for a while, if the climate is wet and the tyre grip is bad, a particular route is not advisable etc.
 
               






                                


