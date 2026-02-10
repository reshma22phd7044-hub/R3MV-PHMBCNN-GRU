This study introduces a unique CNN, PHMBCNN, designed to enhance classification accuracy using a progressive learning strategy. 


**PHMBCNN Architecture**

The proposed PHMBCNN is a Progressive Heterogeneous Multi-Block CNN. It is made up of four computational blocks called 
  a. RMD Block: Residual blokc+ MBConv+ DSC block
  b. XRM Block: Xception block+ Residual+ MBConv block
  c. SEMD Block: Squeeze Excite block+ MBConv+ DSC block
  d. MRD Block: MBConv block+ Residual+ DSC block.

  The first sub block in all four blokcs are used for extracting the features from the input and sequential sub blokcs are used for processing those features.

<img width="958" height="813" alt="image" src="https://github.com/user-attachments/assets/1c462a22-f235-4d9f-8719-052a6e4b6c4d" />

**PHMBCNN-GRU Architecture**
PHMBCNN-GRU is build by adding GRU layer at the end of th ePHMBCNN architecture, this will enhanec the models perfromance.

**R3MV architecture**

We propose the R3MV three-tier decision fusion system, which integrates predictions from 

(i) individual CNN model predictions, 

(ii) a feature fusion classification architecture, and 

(iii) a meta-classifier trained on the outputs of the CNN models.

<img width="1354" height="594" alt="image" src="https://github.com/user-attachments/assets/ed8b2693-31b0-4b5a-96c8-2186f8baaa67" />

**(i) Individual CNN models:**

1. GoogleNet
2. MobileNetV2
3. InceptionResNetV2
4. DenseNet201
5. NASNet
6. PHMBCNN-GRU

A pretrained version of models are used for the remaining Deep Learning modles. The prediction results of all these individual models are saved for later purpose.

**(ii) Feature Fusion Classification**
In this block the features are extracted from all the individual models and MLP classifier is used or classification of skin lesion image. to improve the performence of classification, the extracted features are refined by using the PCA and Mutual Information ranking. The Top k- no of features are passed as input to the MLP classifier.

**(iii) Decision level Classification**
in this level SVM classifier is used as meta classifier and trained on the predictions of the individual classifiers. to improve the classification rate the model combinations producing the higher classification accuarcy are considered for final state of classification.

**Final stage-Majority Vote**
Majority voting mechnism is applied on all the predicions of individual models, feature fusion MLP classifier, decision levle SVM classifier. this type of frame work improves the overall reliaility on the final outcome as it passed threough three level of decision mechanism.


