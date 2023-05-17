
# Analyzing Modern Deep Learning Approaches for Spoiler Detection in Text

When choosing to watch a movie or TV show, reviews and ratings are often relied upon to make informed decisions. However, these reviews can inadvertently reveal significant plot details, leading to spoilers that diminish the viewing experience for newcomers. In our project, our aim is to address this issue by utilizing deep learning techniques to identify spoilers with improved accuracy.Inspired by Anyelo Lindo's research in his PhD dissertation, we seek to experiment with different architectures and assess their effectiveness in spoiler detection. In our analysis, DistilBERT with extra processing (not sampled) at 25% data achieved a higher training accuracy of 0.83 and testing accuracy of 0.78. 


## Models Used

![success](https://iili.io/HU6MkCb.png)


![failed](https://iili.io/HU6W6Lg.png)


![bert_comparative](https://iili.io/HU6XF24.png)


Overall, our results demonstrated that architectural choices, data preprocessing techniques, and data sampling strategies significantly impact the performance of the models. DistilBERT emerged as the top-performing with an accuracy of 78.49\%. With BERT Comparative, we see that inclusion of movie plot data in BERT training showed potential for improving spoiler understanding. This model as performed well with 78.18\% accuracy. 


## Repository Structure

The File Structure is given below:- 


```dataset``` : This folder contains all the dataset files used to train the models

```AlBERT``` : Folder containing Variations of AlBERT model

```BERT Comparative```: Folder containing Variations of BERT Comparative model

```DistilBERT``` : Folder containing Variations of DistilBERT model

```GPT-2``` : Folder containing Variations of GPT-2 model

```RoBERTa```: Folder containing Variations of RoBERTa model

```Small BERT```: Folder containing Variations of Small BERT model

A single model folder can have many folders each containing a vairation of the model mentioned in the table above. Each folder has the following format of the name: ```x% isSampled type_of_processing```. Here isSampled would denote if data used was sampled, and type_of_processing will denote the data processing techniques applied according to the table below:- 

| Processing  Technique | Lower | Remove Link | Remove Double Space | Special  Characters | Expand Contraction | Remove Accented Characters | Stopwords |
|:---------------------:|:-----:|:-----------:|:-------------------:|:-------------------:|:------------------:|:--------------------------:|:---------:|
|   Little Processing   |   No  |     Yes     |         Yes         |          No         |         No         |             No             |     No    |
|    Extra Processing   |  Yes  |     Yes     |         Yes         |         Yes         |         No         |             No             |     No    |
|   Double Processing   |  Yes  |     Yes     |         Yes         |         Yes         |         No         |             No             |    Yes    |
|   Special Processing  |  Yes  |     Yes     |          No         |         Yes         |         Yes        |             Yes            |     No    |



## Steps to Run 

The code uses Google Colab, and Drive so that we could have trained the models faster since the data is closer to ~850MB and loading it everytime is difficult. So the steps to run any model is:- 


1. Go to the folder of any architecture. 

2. Select the Variation of the Model as per table given above. 

3. Go to the notebook and add it to Google Colab. 

4. Download ```dataset``` , upload all the files to Google Drive of that account. 

5. Connect to a GPU. Keep in mind that these notebooks were trained mostly on Pro Version of Google Colab, and we used High RAM VMs and powerful GPUs, so you may face RAM issues 

6. Click Run All to train and evalute the respective model
<<<<<<< Updated upstream
=======
## Authors

- [@dipitvasdev](https://www.github.com/dipitvasdev)
- [@palakkeni5](https://github.com/palakkeni5)
- [@Maadesh](https://github.com/Maadesh)

## Ackowledgements 

- [https://www.tensorflow.org/text/tutorials/classify_text_with_bert](https://www.tensorflow.org/text/tutorials/classify_text_with_bert)


- [Fine-tuning a BERT model](https://www.tensorflow.org/tfmodels/nlp/fine_tune_bert)

- [How to randomly select rows from Pandas DataFrame](https://www.geeksforgeeks.org/how-to-randomly-select-rows-from-pandas-dataframe/#)

- [GPT2_Transfer_Learning_final.ipynb](https://github.com/almarengo/gpt2-text-classification/blob/main/GPT2_Transfer_Learning_final.ipynb)
>>>>>>> Stashed changes
