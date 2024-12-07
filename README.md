Neural Networks CS 752  
Network Traffic w/ Feature Ablation and Additive Attention  
Professor Laura Dietz  
Written by Jack Schneider  
11/27/24

1. **Task:**   
     
   **Definition:** Given inputs of network traffic ***w*** parameters such as packet sizes,bwd metrics, fwd metrics, etc. predict traffic label ***y*** as ‘Benign’ or ‘DDos’. Analyze how ***additive attention*** and ***feature ablation*** affect model performance.  
   **Inputs:** Input of network parameters ***w***, taken from network traffic DDos data set  
   **Outputs:** Output a prediction ***y*** of ‘Benign’ or ‘DDos’  
   **Reimplementation:**  No Reimplementation  
     
2. **Motivation:**  
     
    **Domain:** Network Traffic and Cyber Security  
   **Importance:** Cyber attacks are an ever growing issue for everyday people and company owners. Resulting in the release of personal information like passwords and costing companies millions of dollars in damages.  
   **Helpful:** Solving this task is important because this could help prevent different cyber attacks from occurring. An efficient model could definitely improve the detection of bad network traffic and would be an additional defensive measure for a company saving companies money.  
     
3. **Data set:**  
     
   **Download:** [https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset/data](https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset/data) labeled as “Friday-WorkingHours-Afternoon-DDos.pcap\_ISCX.csv”  
   **Confirmation:** Data has been downloaded and accessed in jupyter notebook  
   **Train/Test split:** First 80% of network traffic examples will be used as training data and the proceeding 20% will be used for testing and validation.  
   **Suitability:** The data that I found will be suitable for training and testing to make accurate predictions with 43.3% of the data being DDos. The train test split contains 78,130 DDos examples in the training set and 19,588 DDos examples in the testing set.   
     
   **Preparations:** To prepare the data for training and testing, separating the data frame into X being everything not ‘ Label’ and Y being ‘ Label’. Then removing any numbers that are nan and clipping the values to be in a smaller range of numbers to prepare for normalization. After preparing the data to be suitable for training the data is then split 80% train and 20% test and loaded into train and test data loaders. Each iteration of the data loader has the shape (64,78) where 64 is the batch size and 78 is the number of features.  

Results and deeper discussion can be found in my project report
