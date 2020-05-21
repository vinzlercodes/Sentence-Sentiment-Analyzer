The NLP system is based on the **Skip-Gram Model** for Word2Vec methodology. We also perform word-embedding instead of one-hot encoder methodology.

A 1D Convolution Neural Network is used for modelling of the NLP system.

The project is trained on the **Sentiment140** dataset consisting of 160,000 tweets which can found [here](http://help.sentiment140.com/for-students).

**Implementation**:

**1)** We start by importing all the libraries that are required for the algorithm

![NLP1](https://user-images.githubusercontent.com/34100245/82439466-5a6d6480-9ab8-11ea-9561-8be4a4a4c7ac.PNG)

**2)** We then load our data and into the test and train sets respectively and set the main data as the **train_data** since that is our main dataset for the modelling and training of our model


![NLP2](https://user-images.githubusercontent.com/34100245/82440054-5726a880-9ab9-11ea-9be4-c52d1b887326.PNG)

**Incase the code is unable to process the data properly or you want a faster training process, Google colab is another great source,
just upload the data in a folder on Google Drive and mount the Drive and aaply the same code with the Drive file path.**

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

**9)** We then define the maximum length of each input and make sure that they are all the same length for proper processing and training and if the lengths are smaller as compared add null value (0s) at the end to increase the lengths

![NLP9](https://user-images.githubusercontent.com/34100245/82449709-45e59800-9ac9-11ea-9070-37e114298daa.PNG)

**10)** We then split our main dataset into a training and testing datasets with those specific labels. Since in the dataset the positive and negative comments are split 50-50 we have to append first half of the positives and negatives into the testing set so that when run it can identify between the 2. We then remove the **testing dataset** values and append the rest of the positive and negative values for the **training set** .

![NLP10](https://user-images.githubusercontent.com/34100245/82452812-6152a200-9acd-11ea-8da2-07f3a9fc7308.PNG)

**11)** We then finally design our CNN model

![NLP11](https://user-images.githubusercontent.com/34100245/82457629-471bc280-9ad3-11ea-8799-74b5e4ad33d2.PNG)

![NLP12](https://user-images.githubusercontent.com/34100245/82457702-5bf85600-9ad3-11ea-90c3-5643689d32fb.PNG)

**12)** We then configure our training variables of the **Embedding Dimensions** , **Number of Filters** , **Fully Connected Nodes** and 
**Number of Classes** ,  also the **Droput Rate** . We also then mention the **Number of Epochs** and also the **Batch Size**

![NLP13](https://user-images.githubusercontent.com/34100245/82459042-12106f80-9ad5-11ea-9625-9ca4582138f3.PNG)

**13)** We then feed the above configurations into the training class

![NLP14](https://user-images.githubusercontent.com/34100245/82460227-8bf52880-9ad6-11ea-8dc8-f22cf153370e.PNG)

**14)** We then compile the model for 2 cases: for both **Binary and Multi Class Classifications** . We also define a file path where we can save our model trained weights to use later without having to train all over again

![NLP15](https://user-images.githubusercontent.com/34100245/82460674-16d62300-9ad7-11ea-93e2-8893d67a054d.PNG)

**15)** We then finally call the training **fit()** function and execute the training of our model (***the training will take a long time so I suggest taking a break***) The first 2 epochs are showcased for refernce. The final accuracy reached was ~96%

![NLP16](https://user-images.githubusercontent.com/34100245/82461138-b398c080-9ad7-11ea-920f-5a8a125a83bf.PNG)

![NLP17](https://user-images.githubusercontent.com/34100245/82461175-bf848280-9ad7-11ea-9563-c2cdc60ff7b5.PNG)

**16)** We then apply this trained model to the testing data set to see its testing accuarcy 

![NLP18](https://user-images.githubusercontent.com/34100245/82462533-5271ec80-9ad9-11ea-82e5-2f7a6e51fb77.PNG)

**17)** Finally we test it on user input messages

![NLP19](https://user-images.githubusercontent.com/34100245/82463312-4dfa0380-9ada-11ea-8c06-2653096f2529.PNG)

![NLP20](https://user-images.githubusercontent.com/34100245/82463351-5b16f280-9ada-11ea-9d1c-295f95fe62c6.PNG)




If you like the work and my methodology please do leave a review and a star.

***Thank You***





