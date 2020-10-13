# Building of conversational agents using goal-oriented dialog managers (Konversa)

## Brief Overview
The call centers require automation for customer services to provide cost-efficient, reliable, and user-friendly self-services for domain-specific tasks in an interactive manner. Human-Human conversations are a reliable source to build conversational agents to generate natural responses with proper greetings to satisfy the customers. Several components have trained separately to interpret the user’s intention from the utterances, predict the next system action, and generate a proper system response for each turns in the conversation to attain the goal. The technical errors within that business logic integration also have handled by providing a suitable response for the technical error which has faced while having the conversation with the user.\
The Recurrent Neural Networks play a prominent role in designing Interactive Conversational Agents for automation with the requirements mentioned above. Also, the advancements in deep learning techniques have motivated the sector of automation, and digitalization, which plays a crucial role in the Revenue growth of a company. Thus, a customized variant of sequence-to-sequence model architecture has employed to predict the system’s next action, which uses Long Short Term Memory cells. The customized architecture has designed to learn progressively using Progressive Neural Network architecture. Hence, the gate mechanism has also modified according to the specifications of the Progressive Neural Network. Thus, the proposed progressive sequence-to-sequence learning architecture for Dialogue Management uses a transfer learning technique to train progressively of different dialogues either in a single domain or it can also be used to train multi-domain dialogues. To achieve naturalness in responses, the generation of responses has also automatized. To achieve automated responses, the Progressive sequence-to-sequence learning with an Attention mechanism has proposed.\
The conversational agents have evaluated in a live user setting by a total of 14 participants, with equivalent professional and naive participants. The demographic perspective has considered in choosing the participants with the factors, including age group, and sex as well. Each user has participated in two surveys after interacting with each system, one is a web-based survey, and the other is a document-based survey. The Attractiveness of each system has measured from the web-based survey, and the usability metrics complying with ISO standards have measured by the document-based survey. The objective measures from the collective subjective assessment have also determined from the document-based survey. The complete results that have obtained from both the surveys have depicted.

## Contents
1) Introduction
2) Background and Literature Research
3) Related Frameworks
4) Implementation of proposed strategy
5) Evaluation Results and Discussion
6) Conclusion

## Introduction
In service innovation, digitalization plays an important aspect, which has paved the way for Information and Communication Technology-enabled (ICT-enabled) services, and it has introduced significant changes in the interaction between customers and the service providers. The ICAs have become actors in the value creation process, which satisfies the roles of service employees. When compared to other technologies used in the service systems, ICAs have the potential to perform interpersonal interactions in online service encounters, and thus enhancing the service quality, efficiency, and experience of the customers. It plays a dual-role by representing the technology and taking an active part in interacting with the customers. Hence, it has to be designed with the abilities to represent human characteristics to play a role in customer service.\
The use of technology for the delivery of services has brought changes in customer behavior, which has evolved to a personalized approach over the last two decades, and it has many direct and indirect interventions through multiple channels. The digitalization has intervened the customer engagement with the following trends among the access of the customers as follows,
* __Natural Interactions__ The experience of the customer is of the utmost importance, such that easier access, an appealing experience, and the respective actions for the user’s input.
* __Flexibility__ Accessing the service through multiple channels at any time 
* __Responsive Service__ A proper response according to the requirements and to provide individual attention
* __Clarity in the information__ Delivery of concise and relevant information about the products to the customer.\
Reports and Data, which is a Market Research and Consulting firm, have analyzed that the market size for chatbots had reached a value of 1.17 Billion United States dollars (USD) in 2018. This has anticipated to reach up to 10.08 Billion by the year 2026, at a Compound Annual Growth Rate (CAGR) of 30.9%1 and it has forecasted that the CAGR of 31.6% especially in the business sector of customer services (https://www.reportsanddata.com/press-release/global-chatbot-market, _version: August 2019_).
* __Service reliability__ The customers and service employees conversations are complex since the requirements of each customer involve various tasks, and they expect individual attention and high-quality service delivery while handling their tasks. Hence, ICAs are often limited to perform basic tasks. It is unable to assure ICAs to handle complex problems.
* __Cooperative principle in the conversation__ According to the theory of H. Paul Grice, who proposed the cooperation principle of four maxims states that Quantity, Quality,
Relation, and Manner are important to have a meaningful conversation. The Quantity defines the informative contributions, and quality represents truthfulness in the contribution, Relation means the relevant information in the responses and Manner defines the transparency in the information with proper delivery ethics [3]. Thus the ICAs must
comply with these four maxim principles while handling the conversations.
* __Responsiveness__ The present ICAs are unable to deliver human-like conversations, as they provide general information. It makes the customers or the users have a feeling that they are talking to a robot. Additionally, the ICAs could not have long conversations to reach a specific goal and evaluating whether the customer requests’ has handled in the desired direction. Hence, the interaction process is intrusive by using certain rules. The improper interpretation of users’ requests results in an inappropriate response.

## Background and Literature Research
### basics of Machine Learning Models
* __Probability Theory__ _Conditional Probability_ It is the probability of an event, for which another event has occurred. The determination of conditional probability is possible if and only if an event has occurred, which means that an event has to happen to determine the conditional probability.\
* __Gradient based optimization__ The criterion considered in any of the optimization techniques is a critical point, local minimum, local maximum, global minimum. When a derivative of a function is zero, then the point at which it occurs is called a critical point. A point where the value of a function is lower than all its neighboring points, and it is impossible to decrease the function gradually is local minimum, whereas local maximum is vice-versa of a local minimum. A point which is neither maximum or else minimum is a saddle point. The absolute lowest value of a function is the Global Minimum. A deep learning model can have multiple global and local minima. The multiple local minima, which are not optimal, and the saddle points with flat regions, have to be optimized while training the deep learning model. This optimization technique has known as Gradient descent optimization.
* __Over fitting and Under fitting__ The factors which influence the capability of the machine learning models are Training error and Test error. The ability of the machine
learning algorithms is inversely proportional to the training error and the test error. Based on the factors mentioned above, the machine learning algorithms have to undergo two
challenges, namely Under fitting and Over fitting.
– _Under fitting_ When the machine learning models are incapable of attaining a low error value on the set of data samples which it has trained, then it causes the machine
learning model to underfit.
– _Over fitting_ When there is a large gap between the training error and the test error, then the machine learning model tends to overfit.
* __No Free Lunch Theorem__ It states that every machine learning algorithms have the estimation of the same error rate for any unobserved inputs provided with an average of
all possible data generating distributions. It means that it is not possible to conclude that one machine learning algorithm is the most sophisticated universally, but rather each machine learning algorithm has better sophistication depending on the distribution of data.
* __Regularization__ This technique employed in deep learning algorithms to reduce the generalization error. Drop out is one of the most used regularization techniques. Though there are other regularization techniques, such as L1-Regularization, and L2-Regularization, drop out averages the predictions of the parameters by randomly dropping out the hidden units along with their lateral connections for all the possible settings.
### Self-Attention Mechanism
The self-attention or intra-attention mechanism has computed using the following equation,\
a<sub>i</sub><sup>t</sup> = *v<sup>t</sup>tanh*(_w_<sub>h</sub>_h_<sub>i</sub> + _w_<sub>h</sub>_x_<sub>t</sub> + _w_<sub>h˜</sub>_h˜_<sub>t-1</sub>)\
s<sub>i</sub><sup>t</sup> = *Softmax*(a<sub>i</sub><sup>t</sup>)\
For each time step, the relation between x<sub>t</sub> and the hidden state h<sub>T</sub> has computed to determine the probability distribution for previous tokens over the hidden state vectors. Then, the vector information has determined for previously hidden tape and memory tape.\
<p>
    h<sub>t</sub> = <span>&Sigma;</span>
    s<sub>i</sub><sup>t</sup> h<sub>i</sub>
</p>
<p>
    c<sub>t</sub> = <span>&Sigma;</span>
    s<sub>i</sub><sup>t</sup> h<sub>i</sub>
</p>
The cell formulation of input, forget, output and Cell gates have then computed and the architecture of self-attention mechanism has depicted below,
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Figures/ProposedWork/Architectures/Self%20Attention%20Mechanism.PNG?raw=true)
### Sequence-to-sequence Learning
The sequence to sequence models using LSTMs has designed to overcome the challenge faced by sequence problems of the fixed dimensionality of inputs and outputs. The key idea is to take one input sequence, reading sequence by sequence for each time step, and obtain a large fixed 3-Dimensional vector representation. The obtained vector representation has then used by another LSTM to decode a target sequence conditioned on the read input sequence. LSTMs can learn from data with long-range temporal dependencies. The architecture of the Sequence-to-sequence learning model has depicted below. The aim of LSTM in this model is to estimate the conditional probability. The length of the target sequence may differ from the length of the input sequence. The fixed dimensionality representation of a vector has computed by the hidden state of LSTM, which has then fed as the initial state for the computation of the conditional probability of the target sequence.
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Figures/ProposedWork/Architectures/Sequence_to_sequence_Learning.PNG?raw=true)

### Progressive Neural Network
To learn the complex sequence of tasks, Progressive Neural Network has proposed, which has the ability to both transfer the knowledge and avoid Catastrophic Forgetting(CF) to give human-like intelligence. It has stated that CF has overcome the leverage of prior knowledge through the lateral connections, which has previously learned. The transfer of knowledge between the neural networks plays a key role in multi-taking. Hence, Progressive neural Network has proposed, which has the support for transferring the knowledge across various domains and simultaneously overcoming CF. The hidden layer connections of updated weight values from the previously learned tasks have used to extract useful features for the new task. It has helped in achieving the feature hierarchy at each layer. The continual learning remains a challenging task in machine learning, where the agents not only learn to generalize for the series of tasks that have the experience but also the ability to transfer the learned knowledge from one domain to another domain.
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Figures/ProposedWork/Architectures/Progressive%20Neural%20Network.PNG?raw=true)

## Implementation of proposed strategy
### Neural Network architecture for Dialogue Management
The proposed architecture has the goal to estimate the conditional probability, which is similar to the sequence to sequence learning architecture. But, this Encoder-decoder architecture has modified to learn progressively for incremental learning to support transfer analysis, in order to develop a model suitable for domain-specific, and also for multi-domain scenarios. The proposed neural network has LSTMs stacked upto the size of ’2’ and has adapted for transfer analysis upto three domains.\
For the incremental learning, each upper stacked hidden layer in the succeeding column has trained not only from the previous hidden layer’s states and outputs, but also from the preceding column’s previous hidden layer outputs and states. Thus, the computation complexity increases, which is proportional to the increase in the size of the column. The current inputs used for training the succeeding column , has also fed into the LSTMs of previous columns which has frozen. By freezing the previous columns, the weight information does not get updated for the current input, but rather it utilizes the previously trained weight matrices to form the cell and hidden state outputs for the current inputs [1][5]. The proposed architecture to learn progressively for single domain or multi domain transfer analysis has depicted below. The proposed approach has also an advantage of using it for incremental learning for a single domain purpose, where the possibility of re-training the new domain-specific data becomes easier using the pre-trained old domain-specific data. This architecture has the flexibility to adapt itself for relative Multi-domain training, such that pre-trained information has its utility in the succeeding domain.
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Figures/ProposedWork/Architectures/Progressive_sequence_to_sequence_learning.PNG?raw=true)

### Neural Network architecture for Natural Language Generation
An attempt has made to generate the natural long sequences of sentences using an intraattention (Self-Attention) mechanism. LSTMs produces a vector state representation, such that the next state has computed based on the current state, which means that for the current state ht, the next state ht+1 conditionally independent in nature from previous states h1, ..., ht−1, and tokens x1, ..., xt. Since the update of states occurs in a Markov manner, LSTMs have assumed to summarize well for the current state for the tokens which have seen so far. It has stated that this assumption may fail, when the sequence is long [2]. The information has processed subsequently in LSTMs by a sequential order, but there are no mechanisms to relate the tokens for modelling the structured output. Thus LSTMs with intra-attention mechanism has proposed to process the contextual representation for each input token, and retaining the contextual information between the tokens to produce the structured output. The architecture of Progressive LSTM with an intra-attention Mechanism has depicted in Figure below.
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Figures/ProposedWork/Architectures/Progressive_sequence_to_sequence_learning_with_attention.PNG?raw=true)

### Architecture overview of developed Interactive Conversational Agents
The fully automatized ICA has not assisted with any pre-determined logic or rules. The system can decide in all dialogue turns, and it has designed to fulfill the end-goal of the domain-specific task. An overview of the design technique has described below, and the architecture has shown.
* __Natural Language Understanding__ Rasa NLU has used to classify the intents and the associated entities from the annotated corpus data that has employed to train the system. The supervised learning
method has used, and hence it requires a lot of annotated data to learn effectively and perceive the intents and the associated entities. It uses a rasa dialogue state tracker to track the dialogue for the entire conversation. It means that the system can remember the entity values that have specified by the user for the entire conversation. The user has to update the entity in single or multiple dialogues while interacting with the system.
* __Dialogue Management__ The dialogue policy has trained using possible dialogue stories, as mentioned in the section of the Preparation of dataset. The policies should learn from the dialogue stories, and the trained model has stored for the inference. A filtering technique has used for selecting an appropriate input inference for the detected user’s semantic frames.The system decides automatically concerning the system action for the perceived user’s utterance. The policies have developed based on machine learning and deep learning algorithms to predict the system action. A action server has used to handle the predicted actions, where the integration of business logics have performed. The semi-automatized ICA has additional decision layer, where the system has assisted when it has predicted a wrong system action in a dialogue turn.\
* __Natural Language Generation__ A machine algorithm has employed to automate the responses for the predicted system action. The NLG component has trained separately from the rasa framework, and the trained model has used in the rasa action server to deliver a response after integration of the business logics. It involves filtering technique to choose one valid candidate from the list of possible candidates.\
* __Business Logic Integration__ The responses must have the information from API results to deliver a contextual response for the user specifications. The user satisfaction depends on this factor as well. Hence, to deliver a quality product the business logics have included in the automated responses, such as list of available options for the user specifications, quantity of available options, information specific to the available options. When there are no relevant information for the user specifications, it has also handled.
#### Full-Automated Interactive Conversational Agent
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Figures/ProposedWork/Architectures/Full_Automated_InteractiveConversationalAgent.PNG?raw=true)
#### Semi-Automated Interactive Conversational Agent
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Figures/ProposedWork/Architectures/Semi_Automated_InteractiveConversationalAgent.PNG?raw=true)

#### Due to the confidential agreement with the company (regiocom SE), the source code of the novel architecture cannot be published

### Reference
1) Ilya Sutskever, Oriol Vinyals, and Quoc V. Le: Sequence to Sequence Learning with Neural Networks, Proceedings of the 27th International Conference on Neural Information Processing Systems - 2:3104–3112, 2014, https://arxiv.org/pdf/1409.3215.pdf
2) Jianpeng Cheng, Li Dong, Mirella Lapata: Long Short-Term Memory-Networks for Machine Reading, Association for Computational Linguistics,Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing:551-561, 2016, https://arxiv.org/pdf/1601.06733.pdf
3) Sungjin Lee, Qi Zhu, Ryuichi Takanobu, Xiang Li, Yaoqin Zhang, Zheng Zhang, Jinchao Li, Baolin Peng, Xiujun Li, Minlie Huang, and Jianfeng Gao ConvLab: Multi-Domain End-
to-End Dialog System Platform, Microsoft Research, Tsinghua University, Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics: System Demonstrations, 1:64-69, 2019, https://arxiv.org/pdf/1904.08637.pdf
4) Pawel Budzianowski, Tsung-HsienWen, Bo-Hsiang Tseng, Inigo Casanueva, Stefan Ultes, Osman Ramadan, and Milica Gasic: MultiWOZ - A Large-Scale Multi-Domain Wizard-of-Oz
Dataset for Task-Oriented Dialogue Modelling, Association for Computational Linguistics, Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing:
5016–5026, 2018, https://www.aclweb.org/anthology/D18-1547.pdf
5) Andrei A. Rusu, Neil C. Rabinowitz, Guillaume Desjardins, Hubert Soyer, James Kirkpatrick, Koray Kavukcuoglu, Razvan Pascanu, Raia Hadsell: Progressive Neural Networks,
Google DeepMind, London, UK, 2016, https://arxiv.org/pdf/1606.04671.pdf
6) Marc Hassenzahl and Noam Tractinsky: User experience - A research agenda, Behaviour & IT, Darmstadt University of Technology, Darmstadt, Germany, and Ben-Gurion University,
Israel, 2006

### Citation for the proposed work
For the usage of the proposed novel architectures, please cite the reference,\
Saran Karthikeyan, Andreas Wendemuth, Ingo Siegert, Marcus Petersen: *Building of conversational agents using goal oriented dialog managers,* Otto-von-Guericke-Universität Magdeburg, regiocom SE Magdeburg, Germany, March 2020
