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

### Neural Network architecture for Dialogue Management
The proposed architecture has the goal to estimate the conditional probability, which is similar to the sequence to sequence learning architecture. But, this Encoder-decoder architecture has modified to learn progressively for incremental learning to support transfer analysis, in order to develop a model suitable for domain-specific, and also for multi-domain scenarios. The proposed neural network has LSTMs stacked upto the size of ’2’ and has adapted for transfer analysis upto three domains.\
For the incremental learning, each upper stacked hidden layer in the succeeding column has trained not only from the previous hidden layer’s states and outputs, but also from the preceding column’s previous hidden layer outputs and states. Thus, the computation complexity increases, which is proportional to the increase in the size of the column. The current inputs used for training the succeeding column , has also fed into the LSTMs of previous columns which has frozen. By freezing the previous columns, the weight information does not get updated for the current input, but rather it utilizes the previously trained weight matrices to form the cell and hidden state outputs for the current inputs [1][5]. The proposed architecture to learn progressively for single domain or multi domain transfer analysis has depicted below. The proposed approach has also an advantage of using it for incremental learning for a single domain purpose, where the possibility of re-training the new domain-specific data becomes easier using the pre-trained old domain-specific data. This architecture has the flexibility to adapt itself for relative Multi-domain training, such that pre-trained information has its utility in the succeeding domain.
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Progressive_sequence_to_sequence_learning.PNG?raw=true)
### Neural Network architecture for Natural Language Generation
An attempt has made to generate the natural long sequences of sentences using an intraattention (Self-Attention) mechanism. LSTMs produces a vector state representation, such that the next state has computed based on the current state, which means that for the current state ht, the next state ht+1 conditionally independent in nature from previous states h1, ..., ht−1, and tokens x1, ..., xt. Since the update of states occurs in a Markov manner, LSTMs have assumed to summarize well for the current state for the tokens which have seen so far. It has stated that this assumption may fail, when the sequence is long [2]. The information has processed subsequently in LSTMs by a sequential order, but there are no mechanisms to relate the tokens for modelling the structured output. Thus LSTMs with intra-attention mechanism has proposed to process the contextual representation for each input token, and retaining the contextual information between the tokens to produce the structured output. The architecture of Progressive LSTM with an intra-attention Mechanism has depicted in Figure below.
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Progressive_sequence_to_sequence_learning_with_attention.PNG?raw=true)
### Architecture overview of developed Interactive Conversational Agents
#### Full-Automated Interactive Conversational Agent
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Full_Automated_InteractiveConversationalAgent.PNG?raw=true)
#### Semi-Automated Interactive Conversational Agent
![alt text](https://github.com/Naras-KS/Konversa/blob/main/Semi_Automated_InteractiveConversationalAgent.PNG?raw=true)

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
For the usage of the novel architectures in the proposed work, please cite the reference,\
Saran Karthikeyan, Andreas Wendemuth, Ingo Siegert, Marcus Petersen: *Building of conversational agents using goal oriented dialog managers,* Otto-von-Guericke-Universität Magdeburg, regiocom SE Magdeburg, Germany, March 2020
