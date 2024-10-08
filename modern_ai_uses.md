Modern AI systems are present in every aspect of our lives even without us knowing about it. All these modern AI systems are weak systems. 

## Weak AI (Narrow AI) vs Strong AI (Artificial General Intelligence) 
**Weak AI:** is an AI system that is trained for a specific task and can't generalise out of the field that it is trained to. It may show superhuman problem-solving but only in one (or several) areas where it is trained. 

**Strong AI**: not created yet in the realms of fantasy so far. It is supposed to have knowledge across different domains and the whole spectrum of human cognitive abilities. It may have motivation and volition as well as self-awareness. It should have a perception of the whole environment. It may reach superhuman intelligence across all fields. It may be able to self-improve recursivly. 

## What are Modern AI Systems Used For? 

### Healthcare and Pharma: The Fastest Growing Area Adopting AI
- detects diseases
- monitior patients
- optimise perscriptions
- wearables can help monitoring, look for anomalies and call emergency if such appear

### Telecommunication and AI: 
- automates networks
- optimises networks
- checks networks' health and safety
- fixes networks before they get broken
- prevents fraudulent behaviour (trained on big data)

### Car Industries and AI: 
- sensors to the car to stay in lane
- emergency brakes
- technical problems sensors
- driver's risky behaviour (like fatigue, alcohol)
- self-driving features
- in production, ensures safe production line and assembly better than humans

### Financial Sevices and AI: 
- detects fraudulent transactions
- detects potential money laundring
- computer vision for checking signatures
- robo-advising: recommends investment oportunities for users
- AI in portfolio optimisation

### Business and Legal and AI: 
- automates repetitive tasks
- robotic process augmentation with ML and computer vision
- reduction of the risk of fraud

### Consumer Goods and Retail and AI: 
- AI predicts customer behaviour
- website trackers to suggest personal purchases
- optimisation of the supply chain
- optimisation of market and store location
- customer service

## Evaulation of AI Systems 
Why is it important? As more and more everyday tasks are performed by AI, there is a growing need for good ways to evaluate the AI results. It is cruial that all datasets are independent and follow a similar probability distribution. 

The avaiable data should be split in three sets: 
1. Training data set: used during the training process
2. Development set: used to validate the results (also called validation set
3. Test set: used for final evaluation. Used to see if the model is not overfitting.

All the three sets must be separate from each other and no data should be in more than one set. They should have a similar distribution like the original dataset. 

### Sample evaluation metrics in binary classification task
1.  $Accuracy = \frac{TP + TN}{TP + TN + FP + FN} = \frac{TP + TN}{all samples}$ -> the percentage of total predictions that were correct
