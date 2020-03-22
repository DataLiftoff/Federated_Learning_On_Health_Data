# Federated Learning On Distributed Private Health Data On Smartphones

The **smartphones of the people probably carry the most valueable but also private data**. Since using data promisses to be one of the best ways to fight back against COVID-19, it is highly desirable to get access.


By using a **[Federated Learning](https://federated.withgoogle.com/)** approach with PySyft it is possible to **learn from the private data right on the smartphone, with the data never leaving the device**.

A short [YouTube-Video](https://youtu.be/npr8hW_Fb_4) has been created for this project.  
There is also an [Devpost-project](https://devpost.com/software/08_corona_tracking_id_0139_federated_learning_on_health_data).

# Approach

1. Since there is no private dataset with health data during a virus outbreak, a **simulated dataset has been used to show the prove of concept**.
2. The **dataset contains the health status of each person** (e.g. temperature, movement, ... ) for several days during the virus outbreak.
3. Using PySyft-Workers the **data for each single person is distributed to a worker** (virtual smartphone). Therefor each worker only knows its own health status.
4. A **simple feedforward network is send to each worker during the training process**. The learning takes place directly on the virtual smartphone itself and an updated network is returned to the host. This way the data did never leave the smartphone and stays protected. 
5. The **target variable to predict is the total number of infected people** in this notebook.

# Conclusion

It is **possible to make us of the private health data of the people without lowering the protection of the data**.  
The notebook can be seen as prove of concept that learning on distributed individual health data can start a learning process in neural network. 


# Limitations (With Possible Solutions)

**Limitation:**  
Simulated data without a connection to the real world has been used.  
**Solution:**  
Exchanging the dataset and adjusting the code should be pretty easy.


**Limitation:**  
A trusted App with permission to store private health data on the device is needed on many smartphones.  
**Solution:**  
Probably another team created a similar App during the hackathon or there is an existing one already out there. Merging this approach with such an App is necessary. 


**Limitation:**  
The hardware limitations have been very strict for this notebook.  
**Solution:**  
Running the simulation and training process on a much larger scale should indicate if the approach is promising.
