
# Methodology
We used Bio.Entrez package of Python 3 to query , search and fetch the metainformations of the RCT studies in PubMed (search period from 2010 to 2020 February; Protocol of the systematic review has been published https://www.sciencedirect.com/science/article/abs/pii/S1087079221000307). The three BERT models of distillBERT, BioBERT and SciBERT are used to classify the title and abstract via  Pytorch. We manually labelled the text by reading abstract. After diagnosing the wrong predictions, a stacked model was built by featuring the probability predicted by distillBERT and keywords of the search domains (complementary and alternative medicine). For the studies labelled as 1 (positive) based on the abstract, their full texts in PDF format were fetched from PubMed Central when available. Haystack question-answering pipeline(https://github.com/deepset-ai/haystack/#tutorials) was then fine-tunned and applied to the preprocessed full text to extract key information for further article screening. 

# pipeline
![](https://github.com/Xiaowen-JI/Systematic_review_automation_CAMs-treatment/blob/f042bcdbf47dc278c9aa2405b291c3363246f63d/pipeline.JPG)


# flowchart
![](https://github.com/Xiaowen-JI/Semi-automation-of-systematic-review-of-clinical-trials-in-medical-psychology-with-BERT-models/blob/69c9fd2e62c1fabc4399915fd589269e18e3a16b/Flowchart.jpg)

# Stacked Model Design (by Salash)
![](https://github.com/Xiaowen-JI/Semi-automation-of-systematic-review-of-clinical-trials-in-medical-psychology-with-BERT-models/blob/c86f5c2e089dd69ea1c197c133fd7afcdac97600/StackedModelDesign.jpg)
