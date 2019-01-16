# Review-Handwritten-Signature-Verification
Review the state of art works of handwritten signature verification works

## Paper Luizgh (2017)
```
Hafemann, L. G., Sabourin, R., & Oliveira, L. S. (2017, November).
Offline handwritten signature verification—literature review
In Image Processing Theory, Tools and Applications (IPTA), 2017 Seventh International Conference on (pp. 1-8). IEEE.
URL: https://arxiv.org/pdf/1507.07909.pdf
```
Depending on the acquisition method, signature verification systems are divided in two categories: **online (dynamic)** and **offline (static)**. 
- In **online case**, an acquisition device, such as a digitizing table, is used to acquire the user’s signature. The data is collected as a sequence over time, containing the position of the pen, and in some cases including additional information such as the pen inclination\velocity\angle\curvature\full acceleration\coordinates\pressure 倾角\速度\角度\曲率\全加速度\坐标\压力
- In **offline signature** verification, the signature is acquired after the writing process is completed. In this case, the signature is represented as a _digital image_
- Model: **SVM** (Support Vector Machines) is one of the most effective classifier for signature verification
- Feature: **Texture features** (especially Local Binary Patterns LBP) is the best hand-crafted feaature extractors in signature verification
- Luizgh proposed project: https://www.etsmtl.ca/Unites-de-recherche/LIVIA/Recherche-et-innovation/Projets/Signature-Verification
  - Convolutional Neural Network CNN approach to learning both writer-independent and writer-dependent features
  - Sigver_Wiwd on github: https://github.com/luizgh/sigver_wiwd

## Open source works
In many cases, the open source projects were deployed by matlab. 
### Offline projects
- https://github.com/luizgh/sigver_wiwd  
  - **Offline Expert!** 
  - DCNN Deep convolutional neural network
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

### Online project paper:
- https://www.researchgate.net/profile/Napa_Sae-Bae2/publication/262055983_Online_Signature_Verification_on_Mobile_Devices/links/55b1f52408ae092e96500858/Online-Signature-Verification-on-Mobile-Devices.pdf?origin=publication_detail
- http://www.ijste.org/articles/IJSTEV2I10172.pdf

### Database Download-Able
- offline: **UTSig** (University of Tehran Offline Signature Dataset)
  - scanned png files
  - URL: https://sites.google.com/site/amirsoleimanibajestani/publication
