# Botnet_detection_using_Netflow
Botnet detection using data from Netflow packets and Machine Learning

POC_code colab shows code for Proof of Concept that jflow (or netflow) monitoring services data can be used to make botnet detection using Machine Learning. This POC was then advanced on in Juniper Networks to build a new product.
In these two notebooks combined, we have implemented the complete Machine Learning workflow starting from Data Cleaning, EDA, Feature Selection and Engineering, Running different models, Hyperparameter tuning, Evaluate and interpret models.

This project uses CTU-13 dataset that was captured in the CTU University, Czech Republic.
Netflow (by Cisco) and Jflow (by Juniper) are flow monitoring services use IPFix Format. They contain information such as Src IP, Dst IP, Src Port, Dest Port, TimeStamp, Protocol, Tot Pkts, Tot Bytes.
Since large number of flows are generated each second, we have used time window concept for feature extraction.
Training models - Random Forest, Gradient Boost and Extra trees are used with and without class weights.
Predictions were made using these models with up to 99% accuracy, 91% F1 score.
Ctu_netflow_detail colab gives deep dive into preprocessing, extensive EDA, feature selection and tuning of models.
