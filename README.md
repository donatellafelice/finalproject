# finalproject
looking for linguistic differences between debate and dialogue

## Question: 
#While we can look at a conversation and reasonably accurately know if our counterpart is receptive or a good conversation partner, and machines can tell too, do we know what we need to do to reproduce that? Can we explain what makes a conversation a debate or a dialogue through linguistics? Conversation is an important part of life. However, the burgeoning field of conversation research has shown that people are poor self-evaluators who are often unable to tell how their conversational style will be interpreted (Candor; Yeomans, et al. 2020). Conversational Receptiveness, a concept developed by researchers in 2020, is difficult to display, even when researchers specifically advise participants to do so. Only when advised of a very specific “recipe” were participants in the study able to change their conversation style. 

## Data set: 
#I will draw from existing data provided through a series of studies conducted at Booth School of Business. I would be looking at leveraging existing packages and algorithms to try understanding the linguistic markers present in the transcripts of the experiments. I intend to explore both algorithmic and machine learning based approaches to classification and quantitative analysis. Through these techniques, I hope to build an overall picture of the different elements that mark a conversation more debate or dialogue-like. 
#Data:  
#Studies 1 -3: Consequences of debate vs. dialogue (Risen, Wald 2023)
#In Study One, participants role played a hiring decision in which they needed to share information to reach the best possible outcome. These were zoom conversations recording from the virtual lab and a research assistant was present throughout the discussion. The pairs in the dialogue and control conditions were more likely to choose the best candidate, in part due to better information sharing. Study Two are text-based conversations between pairs who also needed to choose the best candidate. Participants in the dialogue condition felt a higher degree of inclusion and satisfaction. Study Three is also a text-based conversations where participants discuss a disagreement of a personal belief. 
#Studies 4 – 7: Causes of debate vs. dialogue. (Risen, Wald 2023)
#Studies four and five were pilot studies that helped identified features that encourage the spontaneous occurrence of each approach (debate or dialogue). Features that encourage debate are identified as: stronger disagreement, more personally certain, moral issue, topic is important to the participant and the issue is viewed as personally relevant. Features that encouraged dialogue weaker level of disagreement, less personal certainty, identifying the goal as learning (instead of convincing), interest in the other group’s impression of the speakers, and shared group membership. Study Six was held over Zoom, and consists of participants discussing topics they disagree about after being told they either did or did not share goals and values with the other person. However, this manipulation was unsuccessful, so instead the results were examined for the features identified in studies four and five. In Study Seven, participants are told to discuss their personal disagreements with either the shared or not share goals and values on the topic of disagreement – which was successful. Notably, this study was conducted via text. 

## Method and outline proposed: 

#Parts of speech tagging/counting/Bag-of-Words: The Bag of Words model is a common, simple approach to natural language processing. The package takes a set of text, normalizes it (removing punctuation, very uncommon words, and the most common words), and counts each individual word. In doing so, it destroys the structure of the texts and looks discretely at how many words appear in each document. Bag of words normally removes stop words or the most common expression, but in this case, we will leave those words in to try and evaluate the different styles of the speakers, as well as look for language coordination (as described by Dajescu-Niculescu-Mizil). 


#Vectors/Continuous-Bag-of-Words: A second method of enquire will be conducted using the Doc2Vec and Word2Vec packages. Both packages examine the proximity of objects to other objects (either words to other words, or documents to other documents, or words within documents compared to words within other documents) to assign them a multidimensional vector. Vectors, being numbers, can be added and subtracted, or used to examine other numbers that may be closer to them or further apart. I hope this technique will reveal if words in the debate condition mean different things to the same words in the control and dialogue condition. I also hope to understand how close certain documents are to others (which is the most debate like conversation). 


#Human coding towards ML classification: I hope also to have a small training set coded, perhaps on the existing code book developed by Risen and Ward, in order to co-opt existing models of politeness, rudeness, or assertiveness and be able to identify markers on debate or dialogue on a larger corpus. It may be possible to leverage machine learning to code a large corpus like the Candor Corpus through semi-unsupervised learning, which could lead to new discoveries.  However, this may fall outside the scope of the project and will depend on my ability to leverage existing models. 


#Algorithmic Analysis: Finally, I intend to run algorithmic analysis on my findings. I will leverage regression modelling to understand how prevalent these patterns are throughout the control groups, while examining the timing of their appearance on the dependent variable conditions. Through regression modelling I hope to learn if these types of linguistic markers are able to predict the outcomes of the experiment (how people feel after the experiment, if the participants achieve the idea outcome when using certain language, etc). Once my initial explorations have been completed, more interesting or novel regressions may present themselves. 


## Challenges: 
#Conversational data presents a number of challenges. There are at least two voices involved in a conversation, unlike in a web document, post, or letter, where there is generally one speaker, or a series of speakers with a single voice. This presents the first question that will need to be answered through my exploratory research: should the conversations be examined as individual documents, should each turn be examined, or the whole text from an individual speaker? Several authors provide insight into this, and it appears that different methods are suited for different purposes. As of my current understanding, I believe it may be best to code at a turn level (for example: Is this turn more or less dialogue? Is this turn exhibiting signs of debate) but examine at a conversation or speaker-based level. The disparity here is due to another two concerns: How will I account for the change in a participant’s language over the course of a conversation or the influence of their partner? And, what will the scale of coding for dialogue and debate be? For example, the initial part of a conversation may be more like a dialogue, but things may escalate into a debate? Even in single turn or sentence, the tone may change. These questions will need to be answered through a deeper understanding of the current theories surrounding NLP and behavioural science as well as a series of exploratory trials (some of which have already begun, see Appendix C). I believe there empirical answers to how to deal with these problems, but they will need to be accounted for throughout my exploration and research. 


## Projected Results:
#I imagine that there will be clear linguistic markers associated with the debate condition. I think we are likely to see many similarities between the dialogue and control condition. I believe that people often are unsure about how to be firm but amenable, so I imagine people will use less firm language in the control condition than in the dialogue condition. I would argue it will be possible to train a classifier to identify debate like speech on a turn-based level. 
