The NLP system is based on the **Skip-Gram Model** for Word2Vec methodology. We also perform word-embedding instead of one-hot encoder methodology.

A 1D Convolution Neural Network is used for modelling of the NLP system.

The project is trained on the **Sentiment140** dataset consisting of 16 million tweets which can found [here](http://help.sentiment140.com/for-students).

**Implementation**:

**1)** We start by importing all the libraries that are required for the algorithm

![NLP1](https://user-images.githubusercontent.com/34100245/82439466-5a6d6480-9ab8-11ea-9561-8be4a4a4c7ac.PNG)

**2)** We then load our data and into the test and train sets respectively and set the main data as the **train_data** since that is our main dataset for the modelling and training of our model


![NLP2](https://user-images.githubusercontent.com/34100245/82440054-5726a880-9ab9-11ea-9be4-c52d1b887326.PNG)

**3)** We can then visualise the dataset on how it looks

![NLP3](https://user-images.githubusercontent.com/34100245/82440482-02376200-9aba-11ea-8e72-6fd5e04302e6.PNG)

**4)** Now that we have succesfully loaded the data we must now pre-process it before modelling the CNN architecture. We start by Data Cleaning out the coulmn values that we do not need

![NLP4](https://user-images.githubusercontent.com/34100245/82440843-9b667880-9aba-11ea-951b-fda57bd9da73.PNG)

**5)** Seeing as to how our new cleaned data looks now

![NLP5](https://user-images.githubusercontent.com/34100245/82441820-2300b700-9abc-11ea-92a6-82be86085bd0.PNG)

**6)** We then further clean off the non string-symbols like ***@*** and any **whitespaces** and also any **weblinks**

![NLP6](https://user-images.githubusercontent.com/34100245/82443179-ade2b100-9abe-11ea-8fad-e8de52d06a1f.PNG)

**7)** We then pre-process the end label value because it return **0 for negative** , **2 for neutral** and **4 for positive** . So we want to bring it to only **binary** i.e. values between 0 and 1. If the value is below **0.5** then its Negative Sentiment, if above 0.5 then Positive Sentiment

![NLP7](https://user-images.githubusercontent.com/34100245/82444291-a02e2b00-9ac0-11ea-9479-0d9d1de09768.PNG)

**8)** We then apply String Tokenizations and also mention the dictionary size and also the word encoding in TensorFlow

![NLP8](https://user-images.githubusercontent.com/34100245/82445626-c785f780-9ac2-11ea-9810-479cd5a15421.PNG)

**9)** 

