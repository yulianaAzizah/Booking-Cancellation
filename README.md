# BOOKING-CANCELLATION

## BUSINESS UNDERSTANDING

### Introduction
The positive impacts of technology and information development for human life is the easier of accessing information. This is then implemented by product and service providers to make it easier for customers to obtain information regarding products/services and make transactions remotely. In the hospitality industry, this opportunity is used to provide online reservation services that allow potential customers to book a rooms and services in advance (Antonio, et al (2019)).<br>

However, the openness of information and the easier of making reservations is also accompanied by the convenience of customers in canceling reservations. This will give uncertainty to the hotel because there is a possibility that a sudden reservation cancellation. This can be a loss that must be borne by the hotel because the room that should be filled ends up being an empty room (Antonio, et al (2017)).<br>

Identification made by Chen and Xie (2013) and Chen, Schwartz, and Vargas (2011), currently most of cancellation because customers want to get the best price. Sometimes after placing an order, the customer continues to search further for the same product/service that has been ordered. Customer behavior like this will certainly have an impact on losses. Therefore, this needs serious attention so that the decisions taken regarding the reservation cancellation policy have a good impact for the hotel and customers. However, as a service provider, hotels must also not be too rigid in implementing policies because it can damage the hotel's reputation<br>

### Problem Statement
Questions to be answered in this project include:
1.	What are the parameters and performance of machine learning models that can predict the hotel reservation cancellations from the Hotel Booking dataset?
2.	How much potential benefit can be obtained if the model is applied in the industry?
3.	What are the factors that influence customers to cancel hotel reservations?

### Objectives
This project is expected to minimize false negative prediction results, the prediction that customers who do not cancel reservations but actually cancel reservations. That way, the magnitude of the loss and the factors causing it can be identified to become a parameters for hotel management in making policies and improvements.

### Production Scenario
There are many factors that influence hotel cancellations by customers. However, these factors may change according to technological developments and customer needs. So that predictions of hotel reservation cancellation can be included in business analysis on a regular basis. In this case, some recommendations that can be given include:

1.	The analysis is carried out after making improvements to the most influential factors so that it can be seen the effectiveness of the improvements made
2.	The analysis is carried out periodically once a month and is included in the monthly management review<br><br>
![download](https://user-images.githubusercontent.com/106572825/191748288-fb2b0ecd-d6b8-4f3d-b1d4-04773637429f.png)

### Metric Evaluation
To measure the performance of the model, the evaluation metric that will be used in this model is Recall.<br>

Recall = (True Positive) / (True Positive + False Negative)<br>

False Negative (FN): The results of this prediction show that the reservation is not canceled but the actual result is cancelled. The impact of this result is loss of revenue and in terms of work efficiency and hotel finances.<br>

By applying the recall metric, the machine learning model that is built wants to minimize the prediction results that are False Negative, the prediction results that show orders not being canceled even though they are actually cancelled.

## RESULT
1.	Machine learning result show that: <br>
o	The best model performance is XGBoost<br>
o	The model can minimize the prediction of customers who make cancellations but are considered not to make cancellations with the Recall matrix model. In this case, the model is able to predict 87% who cancel hotel reservations

2.	If this program is implemented, the company at least increase its revenue potential by € 409,482.89 during the 2015-2017.

3.	Based on the Hotel Booking dataset, the most influential factor in determining whether a reservation will be canceled or not is "is_room_diff" (the difference between the room requested by the customer and the one provided by the hotel).

4.	There are some limitations that are expected in this prediction model:<br>
o	The model is only able to predict lead_time with a limit of 0 to 296 days<br>
o	The model is only able to predict adr with a limit of €0 to €227<br>
o	The model is only able to predict total_of_special_request with a limit of 0 to 3

## DATA VISUALIZATION
Data Visualization can be accessed in [here](https://public.tableau.com/views/HotelBookings_16631504869120/Dashboard1?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link)
