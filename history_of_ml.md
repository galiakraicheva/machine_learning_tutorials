# A brief History of Artificial Intelligence

## Ancient Times and Middle Ages: Setting the Theoritical and Philosophical Grounds of AI

Reference: These notes summarise the Course material of DLBDSEAI01 Artificial Intelligence at the IUAS. 

The field of Artificial Intelligence has its roots in Ancient Ages with Greek Philosophers like Aristotle, who first tried to formalize human thinking in a way that made it possible to imitate and replicate it. In the Middle Ages, Leonardo da Vinci created a hypothetical machine on paper that was a black box, accepting an input and giving out output based on some program, stored in the memory of the machine. 

Later in the XVI century Hobbes and Descartes developed phylosophical theories about rationalism and how rationing is similar to materialism and calculus so it can be copied in machines. 

In the XVII century, David Hume did an extensive work on induction and reasoning. He said that our knowledge of the world is only empirical (what we have seen, what we have experienced, etc.). When we say that the Sun will rise tomorrow, it is because so far it has risen every day so far but there is no real reason why the past should resembles the future. However, most of reasoning is based on repeated exposure and experience (as in the case of an AI nowadays). 

## How Artificial Intelligence Developed as a Scientific Field
In 1950, Alan Turing formalised human thinking and defined his famous test: the turing test. The test describes a situation in which there are three participants in the interaction: a human judge, a human respondent and a machine (AI). The human judge doesn't know who answers the question (if it is the machine or the human). If the human judge can't distingish if it is the machine or the human, then the machine is considered real AI that passes the test. 

In 1956, there was the first AI conference where the term was coined by John McCarthy. He establishe AI as a separate field of study in a collaboration with the MIT and IBM in 1958. The initial attempts were for AI systems to implement logical calculus problems. 

In 1959, Marvin Minsky started the MIT Artificial Intelligence Laboratory. He combined AI with cognitive science. 

About the same time, the prominent linguist Noam Chomsky made advancements in formal language theory and the idea of universal grammar as well as Chomsky hirearchy that helped the development of Natural Language Processing (NLP). With respect of NLP, the initial attempts were focused on very limited environments, with the microworld approach, which aimed to simplify the environment as much as possible, which gave good results. 

### Key AI institutions
The most prominent institutions in the past and nowadays, are MIT and Dartmouth College as well as IBM, Intel and American government-sponsored security projects and institutions. 

### Key disciplines contributing to AI's separation in a new discipline 
There are 4 main disciplines that have contributed to the development of AI: 
- **Decision theory:** the field that combines mathematical probability and economic utility. This field helps AI make decisions based on uncertainty and trade-offs. It is the stydy of how agents make choices given some constraints, some available information, preferences and possible outcomes.
- **Game theory:** this field is very connected to AI especially in situations where AI should interact with other agents and make decisions based on the behavour of another agent (competitive or cooperative environments). For example, self-driving cars operate in a cooperative environment with other cars on the road or chess-players try to outsmart each other.
- **Neuroscience:**: the two fields of neuroscience and AI both seek to explain intelligence, cognition and reasoning and have influenced each other profoundly. A very obvious example is the creation of artificial neural networks that mimics the way the brain work. Just as the neurons in the human brain operate and strenghten or weaken connections between them so does an artifical neural network has 'neurons', organised in layers that are connected by weights that change over time with activity.
- **Linguistics:** this field is connected to AI in a subfield, called Natural Language Processing that aims at making computers understand and replicate speech and written text. Examples include: context free grammars and dependency parsing that are used in AI models.

Historically, AI algorithms and programs were written mainly in Lisp (created by John McCarthy), later Prolog and now Python. 

## 1960s: Early AI Optimism and the Symbolic AI emphasis
**Symbolic AI** is based on the idea that reasoning can be put into formal rules and manipulation of symbols. The goal was to encode human reasoning into formal rules that machines can execute. It was believed that a computer can solve any problem that humans can if it was given enought rules and data. It had some success with very controlled environments like playing chess or giving limited verbal commands to a computer but failed in the real world. The complexity of the real world soon made these attempts of formalizing through rules unmanageable. In addition to the lack of computing power, these systems were doomed. 

## Late 1970s: First AI Winter (the Fall of Symbolic AI)
Disappointment due to the failure of symbolic AI to perform satisfactory in general purpose tasks. For example, US and UK government inspected the progress on machine translation from Russian and the AI failed to understand the context. For example, it translated phrases as "out of sigh, out of mind" as "invisible idiot". 

Reason for the fall: powerful algorithms but not enough data and computing power. 

## Early 1980s: The Rise of Expert Systems
After the fall of symbolic AI, there was a paradigm shift. In response to the fail to tackle general purpose tasks, the AI community decided to narrow down the scope and focus on expert systems. Expert systems focus on providing rules and knowledge only on a limited subject and giving very specific well-defined tasks. Such AI sustems were used in healthcare (for example: to spot bacterial infections according to symptoms and lab results and to perscribe antibiotics), in finance and manifacturing. MIT created the Lisp machine that was optimised for running Lisp and had advanced developer tools for symbolic AI development. 

There are 3 approaches to expert systems: 
1. **Case-based systems:** in case-based reasoning, the system decided what to do based on a database of past cases. If the case is new, it finds the most similar past case and tries to adapt the solution to the new situation. For example: A medical perscription based on the previous case with similar symptoms. It is good, if the field doesn't allow formal rule definition and it is addaptable to change. It is bad, if you lack extensive well-labeled data. 
2. **Rule-based systems:** in rule-based reasoning, all decisions are taken based on strict if-then rules. For example, a system about computer diagnosis may take decisions based on rules like "If the computer doesn't start AND there is electricity coming up to the CPU AND there is no electricity coming out of the CPU, THEN replace the CPU.". They are good, if there are strict system rules. They are bad, if they need to be extended or the complexity of the rules increases. 
3. **Model-based systems:** in model-based reasoning, the system uses a predefined model to test against the real-world data and to make decisions what to do. For example, if it is a car diagnosis system, it can have a model of all the car components and how they interact. The system then might decide which parts are broken, comparing the behaviour of the parts with the model that it expects. It is good, for complex systems that are difficult to put in formal rules. It is bad because it requires a lot of computational intensity. 

## Late 1980s - Early 1990s: Second AI Winter (the Fall of Expert Systems)
Despite the initial excitement, the limitations of the expert systems soon became apperent. These systems couldn't improve after a certain point and could not adapt or generalise on new data. This made keeping the expert knowledge database and the rule system very expensive to maintain. In addition, with the growth of the knowledge base, it was very difficult to write rules that don't knotradict each other. The Lisp machine project failed because the Lisp machines were costly compared to the newly developed workstation and personal computers. These new machines run UNIX and could provide even faster speed of execution of Lisp programs than the Lisp machines. 

Reasons for the Second AI Winter: powerful algorithms, better computing power, little data available

## Middle 1990s: Revival of the Interest in AI and First Neural Networks
The Second AI winter brought another paradigm shift. Instead of expert systems, the new focus was on connectionism. The first neural networks were developed to mimic the human brain. Neural networks were theorised as early as the 1950s but were impossible to happen due to computational limitations. In 1986 was developed the **backpropagation algorithm** that made the neural networks more precise. Blackpropagation algorithm allows the neural network to learn from the errors, changing the weights that 'connect' the different 'neurons' just as neuroplasticity changes the strenght of the connections between the neurons depending on the work the brain does. However, in the 1990s there was still a lack of big datasets and limited computational power. 

## 2000s: The Big Data Revolution, Data-Driven AI and Machine Learning
The natural continuation of the paradigm of connectionism found its continuation in the machine learning paradigm. In the mid 2000s big companies like Facebook, Google and Amazon started collecting vast amounts of data. The smart phones were invented and that gave a push of data-driven machine learning techniques. Instead of relying on hand-written rules, machines wer left to discover patterns by themselves by analysing large datasets. Support Vector Machines and Decision trees were popular algorithms at that time for classification and regression tasks. 

The most popular algorithms in the 2000s were still limited in complexity to handle more advanced data like big picture datsets or NLP. 

## 2010s: Deep Learning Revolution
With the advancements in computational power and the big datasets available, paradigm shifter to deep learning. **Deep learning** is a subset of machine learning that deals with neural networks with many layers (hence the name "deep").

The key breakthroughs in AI in the years 2010-2020: 
- Improved Convolutional Neural Networks that became the foundation of the modern computer vision systems.
- Recurrent Neural Networks (RNNs) and Long Short-Term Memory Machines (LSTMs): these architectures are used to handle sequential data like speech and text recognition. They were very successful in machine translation and speech recognition.
- AlphaGo (2016): the computer algorithm developed by DeepMind won over the human champion in Go, so it showed that computers can have superhuman performance in specific complex stratigic tasks.
- Voice assistante like Siri and Alexa showed everyday business success of deep learning.

Problems of deep learning: 
Although powerful, it requires vast amount of training data and computational resources. From ethical side, it lack explainability and is difficult to understand making it dangerous for areas like healthcare or finance. 

## 2020s-Present: Focus on General AI and Ethical AI
Most of the AI nowadays is **Narrow or weak AI**: meaning that it has only specialised in one particular task and event thoug it can be superior to humans in it, is fails in other domains. For example, an AI that is excellent in Chess, will fail to play Go unless it is especially programmed to do that. **Artificial General Intelligence** is an AI that possesses human-like intelligence in all aspects humans can perform well in. As it may mean also developing emotions, feelings, motivation or self-awereness, the field of ethical AI is crucial to humanity's progress and safety. New ideas like adversarial learning came into place. **Adversarial learning** refers to a training technique where two models are trained and compete to produce better results. These models are generator that creates syntetic and adversarial data and a discriminator that tries to distinguish between real data and the syntetic data. This is used for example, in self-driving cars to avoid misleading a sign if there are minor variations from what it should look like or in cybersecurity to prevent attacks on algorithms with manipulated data. 

## Short Summary of the Trends in AI Development
In the earlies attempts, the focus of AI was on formalising logical calculus and having success in NLP in very limited environments. The first wave of AI research delt with logical inference. 

The second wave of AI research (1980s) focused more on knowledge respresentation. Researchers realised that intelligent behaviour was not only based on logical inference but also on the general knowledge of how the world works. In addition in the late 1980s with the backpropagation algorithm, there was the first real interest in neural networks. 

In the 1990s when an AI managed to win over Garry Kasparov in chess, AI started becoming more used in commercial software and had real-life applications. In the 1990s the field of AI was broadened with ideas from decision theory, mathematics, statistics, and others that helped it become a rigorous and mature scientific field. 

The paradigm of an intelligent agent became popular and the focus shifted instead of mimicing human intelligence to creating intelligent behavour and the study of intelligence in general. As an analogy, people first used to imitate bird wings for flight craft but then it turned out that the most successful aircraft doesn't come from imitation. 

After 2012, deep learning made possible advancements in areas that previously had limited success which also brought a revived interest in reinforcement learning and new ideas came around like adversarial learning. 

## Close Fileds of Study that Contribute to AI Research and Vice Versa
- **Linguistics:** our thoughts are very linked with our language and one step further, creativity and thought can be liked to linguistics. For example, a child can say things that it has never heard before. This is very important for linguistic AI and the study of intelligence in general.
- **Cognition:** many of the models in neural networks are influenced by our perception of how the brain functions. In return, using the articial neural networks, cognitive scientists can test theories and make predictions. Another example is the Reinforcement learning that is very similar to the Brain's reward system. 
- **Games:** this refers to game theory, decision theory but also to strategic games like chess, checkers, poker, go, etc. When AlphaGo won against a human, DeepMind trained later a better model called AlphaZero and it could outline strategies that weren't discovered by humans before that.
- **The Internet of Things:** all the wearables collect lots of information about us that generates huge datasets that can help AI algorithms get better. In the same time, AI algorithms can improve the wearables. The ethics of using this information is also an important question. Medical data from a wearable can help the user with medication intake, doctor's appointments, etc but if used against the user, can make his/her health insurance more expensive, etc.
- **Quantum computing**: the field of quantum computing can lead to new algorithms that outperform the present ones. There are still in initial stage the algorithms of Quantum Neural Networks (QNNs) and Quantum Support Vector Machines. There are experiments with Quantum reinforement learning. In the same time, AI can advance quantum computing by means like **quantum error correction**. Quantum computers operate in a very fragile envoronments that are suseptable to noise and others. With the help of machine learning there can be better quantum error correction. 






