# Starbucks Capstone Challenge
In this project I do some EDA of starbucks data.

The business questions I want to ask are as follows:

1 Female customers or male customers, which group is the majority? 

2 Are my customers wealther than the average US people?

3 Could the company make specific promotion strategy according to individual attribute? 

4 How to use funnel analysis to help more people to use their promotions? 

# Dataset overview

The program used to create the data simulates how people make purchasing decisions and how those decisions are influenced by

promotional offers. Each person in the simulation has some hidden traits that influence their purchasing patterns and are 

associated with their observable traits. People produce various events, including receiving offers, opening offers, and making 

purchases. As a simplification, there are no explicit products to track. Only the amounts of each transaction or offer are 

recorded. here are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO 

offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a 

reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a 

requisite amount that the user is expected to spend. Offers can be delivered via multiple channels. The basic task is to use 

the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.

## Data Dictionary
### profile.json：

Rewards program users (17000 users x 5 fields)

gender: (categorical) M, F, O, or null

age: (numeric) missing value encoded as 118

id: (string/hash)

became_member_on: (date) format YYYYMMDD

income: (numeric)

### portfolio.json：

Offers sent during 30-day test period (10 offers x 6 fields)

reward: (numeric) money awarded for the amount spent

channels: (list) web, email, mobile, social

difficulty: (numeric) money required to be spent to receive reward

duration: (numeric) time for offer to be open, in days

offer_type: (string) bogo, discount, informational

id: (string/hash)

### transcript.json：

Event log (306648 events x 4 fields)

person: (string/hash)

event: (string) offer received, offer viewed, transaction, offer completed

value: (dictionary) different values depending on event type

offer id: (string/hash) not associated with any "transaction"

amount: (numeric) money spent in "transaction"

reward: (numeric) money gained from "offer completed"

time: (numeric) hours after start of test

# Results

Now we know that there are more female customers than males in the data set, and the female customers intend to have a higher

income. The whole group of customers in the group have a higher salary than the US median income, and this shows that 

Starbucks is favourable by the middle class.

Among all the offers, the offer with difficulty 10 has the highest completion rate, which may shed light on future promotion strategy of Starbucks.

Unfortunately, these clusters seem to be appropriate for segmenting the customers’ attribute, but not for the transactional 

information. This will be one direction of my future studies. I also want to do supervised learning to find a more effective

promotion strategy given customers’ historical data.

# Licensing, Acknowledgements, etc.
Code released under the MIT license.

Thanks to Starbucks for the dataset, and to Udacity for bringing the opportunity to work with it.

