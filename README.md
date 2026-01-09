# Airline-Pricing-Overbooking-Optimization 

# Highlight part:
#Please refer to simulation.ipynb, the Monte_Carlo funtion is the hightlight part, which simulates the real-world scenario of ticket booking of airline company

# Monte Carlo Simulation Scenario & Purpose:
Airline Companies usually oversell tickets to maximize the profits of each scheduled flight because there is a probability that some passengers who booked tickets will not take on the plane, overselling can raise the seat utilization. However, the exact number of overselling tickets is uncertain, which is very significant to be kept in a reasonable range. If overbooking numbers are not well controlled, it will lead to finance compensation and customer loss due to the absence of seats for excess passengers, or profit loss due to low seat utilization.

So in this model. we will simulate the real-world airline booking scenario based on Monte Carlo simulation principle to find out the best overbooking number range and purse the maximum profits for an airline company.

## Simulation's variables of uncertainty
We will take all the following variable into consideration, which are related to the profits of a single airline flight.
#### The demand of each class of a scheduled flight
The demand of a certain flight follows the binomial distribution in which the largest case numbers are 120% of the capacity, we randomly generate integers from this binomial distribution to represent the numbers of people who want to buy a ticket. Our decision is based on the reference.
#### The number of final show-up passengers 
The number of final show-up passengers also follows binominal distribution based on the reference, in which the largest case numbers are the number of sold tickets. Final show-up passenger number are randomly assigned from the binomial distribution we created.
#### The distribution of no-show passengers on different flight class (including business and economy)
In this model, we have considered two flight classes including the business and economy, and we will assign a total overbooking numbers of certain flight, overbooking tickets for two class are randomly generated from the total, and the combination of the two equals to the total overbooking numbers.
#### The different finance compensation to excess passengers who do not have a seat 
Based on the US policy, the compensation for bumped passengers varies according to the waiting time for changed flight schedule. There are three categories, for people who have waited within one hour, there is no compensation. For those who have waited for one to two hours and more than two hours, the compensations are $400 and $800 respectively. SO, we set the probability of no compensation to 60%, $400 to 30% and %800 to 10%.
#### The probability of no-show passengers who canceled the tickets before departure
For the cancellation, we randomly generate numbers from the number of no-show passengers, for those who cancelled before departure, there is a refund when computed the revenue of a flight.

## Hypothesis or hypotheses before running the simulation:
We assume a fixed air route, so the types of airplanes and the cost of each seat can be confirmed. 
The hypothesis is that within a certain range, the profits will grow following the overbooking numbers' increasement. Then there is a peak to achieve the maximum profits, however the profits will begin to drop after the peak as the overselling keep increasing due to the compensation for the excess passengers.

## Analytical Summary of your findings: (e.g. Did you adjust the scenario based on previous simulation outcomes?  What are the management decisions one could make from your simulation's output, etc.)?
The outputs of this program include a plot, a table and the optimizing result, which can show users how many tickets they should overbook to maximize the profit based on the certain flight type. These outputs prove that our hypothesis is right that overbooking tickets must be controlled in a fixed range or the company will lose revenue. In the fixed range, the largest overselling number can bring the highest revenue.

## Instructions on how to use the program:
The user will need to input the type of flight and other variables according to the reminder. And the program can compute how many tickets the airline should overbook to maximize the profit. For input variables like show up probability and the demand probability, we have provided a suggestion and of course the user can input these numbers according the statistics figure from the own situation. Moreover, we also create two files to demonstrate our result, including .py and .ipynb files. The reason why we create two files is that .py file can output different result of different airplane type with one whole code and .ipynb file is easier to read one result.

## All Sources Used:
Oberstone, J. L. (2010). Spreadsheet Simulation of Airline Reservation Policy Using Multimedia Software. International Journal of Advanced Corporate Learning (iJAC), 3(1). doi:10.3991/ijac.v3i1.1169

Basa, G., & Kedir, A. (2017). Modeling and optimization of the single-leg multi-fare class overbooking problem. Momona Ethiopian Journal of Science, 9(2), 200. doi:10.4314/mejs.v9i2.5

