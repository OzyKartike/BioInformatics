# BioInformatics
Dopamine neurotransmitters and their receptors are integral to the cell-to-cell communication responsible for transferring information in neurons(Bhatia et al., 2023; Kalani et al., 2004). Dopamine D2 receptor is a DRD2 gene encoded protein which is widely targeted in the development of novel antipsychotic medication (Bhatia et al., 2023; Zięba et al., 2019). For this purpose, we developed a quantitative structure-activity relationship (QSAR) model to predict bioactivity against the DRD2 receptor. A dataset of 1240 compounds with reported IC50 values against the DRD2 was sourced from ChEMBL. Compounds were identified as biologically inactive or active depending on IC50 values: IC50 values greater than 10000 nm were identified as active, while those below 1000 were found to be inactive (IC50 values between these two ranges were discarded). A Nipals algorithm was used to develop a PLS model to predict the bioactivity of compounds against DRD2. Molecular descriptors for each compound were extracted with PaDEL, and the molecules were split into a 70% training and 30% testing dataset. The descriptors were fed into the PLS algorithm, and the obtained PLS model was characterized by an R² value of 0.11 as well as a mean squared error of 44.94. 

The pIc50, number of hydrogen donors, and number of hydrogen acceptors are examples of calculated descriptors which are shown below as visual aids. The Mann-Whitney U test was also used for demonstrative purposes to show whether these descriptors were related to the bioactivity of the molecules. However, keep in mind the QSAR model looks at 100s of descriptors.

![alt text](https://media.discordapp.net/attachments/753460073786769428/1142942668922552430/image.png?width=1322&height=1198)

**Figure 1**: The Mann-Whitey U test conducted on PIC50 values in active and inactive compounds shows a statistically significant difference between the two bioactivity classes. 

![alt text](https://media.discordapp.net/attachments/753460073786769428/1142943427919626281/image.png?width=1388&height=1230)

**Figure 2**: The Mann-Whitey U test conducted on the number of hydrogen donors in active and inactive compounds shows a statistically significant difference between the two bioactivity classes. 

![alt text](https://media.discordapp.net/attachments/753460073786769428/1142944156927406100/image.png?width=1406&height=1198)

**Figure 3**: The Mann-Whitey U test conducted on number of hydrogen acceptors in active and inactive compounds fails to show a statistically significant difference between the two bioactivity classes. 

One of the next steps we would like to work on is how to refine the regressive model by optimizing the number of components in order to obtain a higher coefficient of determination.

Credit to the data professor, Chanin Nantesenamat, for providing the idea for the project, as well as the code which we adapted for our purposes. 

## refrences

Bhatia, A., Lenchner, J. R., & Saadabadi, A. (2023). Biochemistry, Dopamine Receptors. In StatPearls. StatPearls Publishing. http://www.ncbi.nlm.nih.gov/books/NBK538242/

Kalani, M. Y. S., Vaidehi, N., Hall, S. E., Trabanino, R. J., Freddolino, P. L., Kalani, M. A., Floriano, W. B., Kam, V. W. T., & Goddard, W. A. (2004). The predicted 3D structure of the human D2 dopamine receptor and the binding site and binding affinities for agonists and antagonists. Proceedings of the National Academy of Sciences of the United States of America, 101(11), 3815–3820. https://doi.org/10.1073/pnas.0400100101

Zięba, A., Żuk, J., Bartuzi, D., Matosiuk, D., Poso, A., & Kaczor, A. A. (2019). The Universal 3D QSAR Model for Dopamine D2 Receptor Antagonists. International Journal of Molecular Sciences, 20(18), 4555. https://doi.org/10.3390/ijms20184555

#### How to run code for different protein or same protein strand:
1. First clone the project
   ``` git clone https://github.com/OzyKartike/BioInformatics.git ```
2. Open the `drd2_final_code.ipynb`
3. Run the code from top to bottom for the same results either on `google colab`, `Jupyter Notebook`, or `Visual Studio Code`
4. To run the same project but on different protein strands simply edit under the `Identifying the target compound` section
 
