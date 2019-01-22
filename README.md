# Review-Handwritten-Signature-Verification
Review the state of art works of handwritten signature verification works. 

Depending on the acquisition method, signature verification systems are divided into: **online (dynamic)** and **offline (static)** with **Writer Dependent** or not categories. 
- In **online case**, an acquisition device, such as a digitizing table, is used to acquire the user’s signature. The data is collected as a sequence over time, containing the position of the pen, and in some cases including additional information such as the pen __*inclination\velocity\angle\curvature\full acceleration\coordinates\pressure*__ 倾角\速度\角度\曲率\全加速度\坐标\压力
- In **offline signature** verification, the signature is acquired after the writing process is completed. In this case, the signature is represented as a __digital image or picture__
- Also, the can be devided into **writer independent** and **writer dependent** classification cases
- **SVM** (Support Vector Machines) model is one of the most effective classifier for signature verification
- **Texture features** (especially Local Binary Patterns LBP) is the best hand-crafted feature extractors in signature verification


## Open source works
In many cases, the open source projects were deployed by matlab or python. 
### Offline project- Luizgh
- https://github.com/luizgh/sigver_wiwd  (Python)
```
Hafemann, L. G., Sabourin, R., & Oliveira, L. S. (2017, November).
[1] Offline handwritten signature verification—literature review
    URL: https://arxiv.org/pdf/1507.07909.pdf
[2] Learning Features for Offline Handwritten Signature Verification using Deep Convolutional Neural Networks
    URL: http://dx.doi.org/10.1016/j.patcog.2017.05.012 (preprint)
[3] Fixed-sized representation learning from Offline Handwritten Signatures of different sizes 
    URL: https://doi.org/10.1007/s10032-018-0301-6 (preprint)
```
  - **Luizgh Offline Expert!** 
  - Project site: https://www.etsmtl.ca/Unites-de-recherche/LIVIA/Recherche-et-innovation/Projets/Signature-Verification
  - DCNN Deep convolutional neural network
  - **SigNet** adopted as the feature approach
    - wget "https://storage.googleapis.com/luizgh-datasets/models/signet_models.zip"
      - 3 signet models: Refere to paper [2]
        - signet.pkl; signetf_lambda0.95.pkl; and signetf_lambda0.999.pkl
      - Input scaned signatures need to be preprocess_signature() before the CNN. The aim is to make sure the input image/signature under the same resolution by wrap/crop/resize functions
    - wget "https://storage.googleapis.com/luizgh-datasets/models/signet_spp_models.zip"
      - 4 signet models: Refere to paper [3]
        - signet_spp_300dpi.pkl; signet_spp_300dpi_f.pkl and 600_dpi
        - (with or without _f_ ) Training the model with or without forgeries
        - 300 or 600 is the scaned resolution of input image
        - 300dpi: input_size: (428, 612) and image_size: (476, 680)
        - 600dpi: input_size: (856, 1224) and image_size: (952, 1360)
      - Improve the preprocess_signature() by the introduced SPP methodology.
        - SPP the final layer in CNN, make sure CNN can handle any scale/size input image and generate the same sized feature vectors
  - Be aware: 
    - the input signature image picture is 1 color channel file **gray color** rather than RGB.
    - The **time consumption** is high due to the limitation of **Theano** of DNN platform 
  - *****questions need to be confirmed *****
    - Check the Euclidean Distance threshold in the paper (interactive_example.ipynb)
        - For actual classification, the simplest approach is computing the distance (in feature space) between a query signature and a reference. This is easy to implement (see the jupyter notebook example), but not very powerful. 
        - Most commonly, people train **Writer-dependent classifiers** (one binary classifier for each user).  

----------------------------------

### Offline projects 
- https://github.com/EB324/signature_verification
- https://github.com/Malkhan52/Offline-Signature-Recognition 
- https://github.com/Aftaab99/OfflineSignatureVerification
- https://github.com/ASoleimaniB/DMML **UTSig DataBase author!**

### Online projects
- https://github.com/jeongmincha/Online-Signature-Verification
- https://github.com/ThompZon/online-signature-verification
- https://github.com/kin3tik/Verifier
  - With project report at: https://github.com/kin3tik/Verifier/blob/master/doc/Project%20Report.pdf
- https://github.com/DonatoMeoli/DS-SRS
  - With project paper at: https://github.com/DonatoMeoli/DS-SRS/blob/master/paper.pdf
- https://github.com/ethanyxfang/MDB-DTW-for-signature-verification
  - Paper Link: https://rd.springer.com/chapter/10.1007/978-3-319-97909-0_68

### Interesting Paper with identical name:
Online Signature Veriﬁcation on Mobile Devices
  - 2014 by Nasir D. Memon (Hey prof, long time no see, how are you?)
  - https://www.researchgate.net/publication/262055983_Online_Signature_Verification_on_Mobile_Devices
  - 2016 by Prof.Jadhav Hemant B (Read the conclusion suggested.)
  - http://www.ijste.org/articles/IJSTEV2I10172.pdf


### Database Download-Able
- offline: **UTSig** (University of Tehran Offline Signature Dataset)
  - scanned png files
  - URL: https://sites.google.com/site/amirsoleimanibajestani/publication
