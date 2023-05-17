
# Analyzing Modern Deep Learning Approaches for Spoiler Detection in Text

When choosing to watch a movie or TV show, reviews and ratings are often relied upon to make informed decisions. However, these reviews can inadvertently reveal significant plot details, leading to spoilers that diminish the viewing experience for newcomers. In our project, our aim is to address this issue by utilizing deep learning techniques to identify spoilers with improved accuracy.Inspired by Anyelo Lindo's research in his PhD dissertation, we seek to experiment with different architectures and assess their effectiveness in spoiler detection. In our analysis, DistilBERT with extra processing (not sampled) at 25% data achieved a higher training accuracy of 0.83 and testing accuracy of 0.78. 


## Models Used

![success][https://iili.io/HU6MkCb.png]


![failed][https://iili.io/HU6W6Lg.png]


![bert_comparative][https://iili.io/HU6XF24.png]


Overall, our results demonstrated that architectural choices, data preprocessing techniques, and data sampling strategies significantly impact the performance of the models. DistilBERT emerged as the top-performing with an accuracy of 78.49\%. With BERT Comparative, we see that inclusion of movie plot data in BERT training showed potential for improving spoiler understanding. This model as performed well with 78.18\% accuracy. 


## File Structure

The File Structure 
## Steps to Run 

The code uses Google Colab, and Drive so that we could have trained the models faster since the data is closer to ~850MB and loading it everytime is difficult. So the steps to run any model is:- 


1. Go to the folder of any architecture. 

2. Select the Variation of the Model as per table given above. 

3. Go to the notebook and add it to Google Colab. 

4. Download ```dataset``` , upload all the files to Google Drive of that account. 

5. Connect to a GPU. Keep in mind that these notebooks were trained mostly on Pro Version of Google Colab, and we used High RAM VMs and powerful GPUs, so you may face RAM issues 

6. Click Run All to train and evalute the respective model