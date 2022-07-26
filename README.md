# 2022-Citadel-Summer-Invitation-Datathon

Introduction:

Since its first launch in 2007 to becoming the world’s largest p2p lending platform in 2014, Lending Club has always made its mission to “provide financial health to Americans through leveraging technology and a marketplace model to seamlessly deliver access to fair and affordable credit”[1]. Starting from May 2017, Lending Club started offering hardship plans to borrowers which allowed for interest-rate only payments in light of unexpected life events, thus, providing additional flexibility to borrowers while securing returns for investors to otherwise charge-off loans[2].
There are numerous causes for hardship submitted by applicants. Nevertheless, a majority of them can be explained by three factors: macroeconomic condition, demographic distribution, and ex-ante credit-worthiness. As such, we seek to explore the relative importance of three factors in relation to hardship status. Specifically, we post two research questions.

Problem 1: Which features contribute more than others in identifying hardship conditions? <br />
Problem 2: Can we predict whether a given individual should be in the hardship program?


Key Findings:

We proceed to answer our questions by framing it into a binary classification problem. We took the accepted debtor dataset and expand it through years, so the expanded dataset is indexed by individual and year. Then, we select and engineered three groups of features: macroeconomic condition factors, demographic distribution, and ex-ante credit-worthiness. This would be the feature of our binary classification model, and the labels are whether a debtor at a specific year enters the hardship plan. After building two "good" models that reached certain out-of-sample accuracy, we would like to evaluate the feature importance in the two models. The two models are SVM and Random Forest. We computed feature importance using mean decrease in impurity and permutation importance metric for Support Vector Machine (SVM) and Random Forests, and developed a final ranking system.

We found the following five most important features that associate to debtor’s hardship status<br />
(a) Debt to income ratio (DTI): Demographic Feature<br />
(b) Total Revolving Balance/Credit Limit (TRBL): Credit Feature<br />
(c) County Unemployment Insurance Benefit amount (UIB): Inter-Temporal Economics Feature <br />
(d) Annual Income (AI): Demographic Feature<br />
(e) Number of open accounts/credit lines (OA): Credit Feature<br /><br />
At the end, we characterized three types of hardship debtors using above five features:<br />
(a) Living in county where unemployment insurance benefit issuance is high and possess high debt-to-income ratio<br />
(b) High Debt-to-income ratio, high number of open credit accounts and low revolving credit <br />
(c) High number of open credit accounts and low income

Note:
The data files are available at https://drive.google.com/drive/folders/17HehvOTnv_u3aAotuNDuE5uf1xg044aA?usp=sharing
