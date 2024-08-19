Introduction

Alzheimer’s disease (AD) is a prevalent neurodegenerative disorder characterized by memory loss and cognitive decline. AD currently ranks as the fifth leading cause of death among those 65 and older, and is expected to affect 13.8 million Americans by 2050. Further, the economic burden of AD care by 2022 was $339.5 billion. Early detection of AD considerably impacts different biological, demographic, psychosocial, and economic factors for individuals and families, making it essential to investigate these social determinants of health.

In this project we analyze a vast National Institute of Health dataset collected by the National Alzheimer's Coordinating Center (NACC). The NACC database comprises data from more than 47,000 participants, encompassing over 174,000 clinical assessments, and includes the Uniform Data Set (UDS) and the Biomarker Data Set (BDS). Measures of cross sectional data from patients' initial visits were analyzed and included health history, demographics, and biomarkers (Aβ1-42 and T-Tau in cerebrospinal fluid), all of which are indicative of AD diagnosis. 

Methods

We use a combination of inferential and predictive tools in order to effectively address the two goals of our study.  First, we employ bootstrap LASSO regression confidence intervals on the binary response variable “diagnosis”, whose outcome consists of two labels, referring to either a diagnosis of at least a mild cognitive progression of the disease, or the negative assessment of the disease among the subjects. The LASSO model allows us to perform variable selection and handle potential multicollinearity among predictors. We complement this by then utilizing a Random Forest model to further assess the importance of these variables.
Finally, to build a predictive model for Alzheimer’s diagnosis, we further deploy Random Forests, while also implementing a one-layer Neural Network.

Results

The LASSO model found that there are a host of variables that impact AD diagnosis. These variables include T-Tau,  A𝛽1-42,  age, systolic blood pressure, years of education, depression,  sex, and marital status.  Our neural network and random forests model returned promising accuracies of  83% and 81%, respectively.
