<img width="196" height="216" alt="image" src="https://github.com/user-attachments/assets/38e8b101-21f3-4542-a7af-08072c8b4bee" /><img width="770" height="81" alt="image" src="https://github.com/user-attachments/assets/add23ad9-a1bd-4c42-9899-ae2bcd9dabdd" />**R3MV architecture**

This study introduces a unique CNN, PHMBCNN, designed to enhance classification accuracy using a progressive learning strategy. We propose the R3MV three-tier decision fusion system, which integrates predictions from 

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

**PHMBCNN Architecture**
The proposed PHMBCNN is a Progressive Heterogeneous Multi-Block CNN. It is made up of four computational blocks called 
  RMD Block: Residual blokc+ MBConv+ DSC block
  XRM Block: Xception block+ Residual+ MBConv block
  SEMD Block: Squeeze Excite block+ MBConv+ DSC block
  MRD Block: MBConv block+ Residual+ DSC block.

  The first sub block in all four blokcs are used for extracting the features from the input and sequential sub blokcs are used for processing those features.

<img width="958" height="813" alt="image" src="https://github.com/user-attachments/assets/1c462a22-f235-4d9f-8719-052a6e4b6c4d" />


