# Classification model to detect pneumonia

## Context

This model detects pneumonia based on chest x-ray images. It is a convolutional neural network, with transfer learning using VGG16. Its final accuracy on the test set is 89%. The data was taken from Kaggle [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia).

The project was inspired by the article on AI detection of COVID-19 pneumonia, available on [Medical News](https://www.news-medical.net/news/20200409/Ai-used-to-detect-COVID-19-pneumonia.aspx). Majority of people with COVID-19 have mild symptoms such as coughing and fever. In some cases, however, severe pneumonia in both lungs can develop, which can be deadly. There is a significant pressure on the hospital staff during the outbreak, as well as the shortage of the the medical equipment and PPE. Potentially AI could allow the doctors to determine whether the patients require supportive care or could recover at home.

_"Pneumonia can be subtle, especially if it’s not your average bacterial pneumonia, and if we could identify those patients early before you can even detect it with a stethoscope, we might be better positioned to treat those at highest risk for severe disease and death",_ said Dr. Albert Hsiao in the article.

## Data

<img src='assets/intro_01.png' />

*Illustrative examples of chest x-rays in patients with pneumonia. The normal chest X-ray (left panel) depicts clear lungs without any areas of abnormal opacification in the image. Bacterial pneumonia (middle) typically exhibits a focal lobar consolidation, in this case in the right upper lobe (white arrows), whereas viral pneumonia (right) manifests with a more diffuse ‘‘interstitial’’ pattern in both lungs* [(Kermany DS, Goldbaum M, Cai W, et al. (2018))]('http://www.cell.com/cell/fulltext/S0092-86741830154-5).

Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.

For the analysis of chest x-ray images, all chest radiographs were initially screened for quality control by removing all low quality or unreadable scans. The diagnoses for the images were then graded by two expert physicians before being cleared for training the AI system. In order to account for any grading errors, the evaluation set was also checked by a third expert.