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
- In **online case**, an acquisition device, such as a digitizing table, is used to acquire the user’s signature. The data is collected as a sequence over time, containing the position of the pen, and in some cases including additional information such as the pen inclination, pressure, etc. 
- In **offline signature** verification, the signature is acquired after the writing process is completed. In this case, the signature is represented as a digital image
- Model: **SVM** (Support Vector Machines) is one of the most effective classifier for signature verification
- Feature: **Texture features** (especially Local Binary Patterns LBP) is the best hand-crafted feaature extractors in signature verification
- Luizgh proposed project: https://www.etsmtl.ca/Unites-de-recherche/LIVIA/Recherche-et-innovation/Projets/Signature-Verification
  - Convolutional Neural Network CNN approach to learning both writer-independent and writer-dependent features
  - Sigver_Wiwd on github: https://github.com/luizgh/sigver_wiwd
