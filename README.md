# Detecting Adverse Drug Events From Conversational Texts

Adverse Drug Events (ADEs) are potentially very dangerous to patients and are top causes of morbidity and mortality. Many ADEs are hard to discover as they happen to certain groups of people in certain conditions and they may take a long time to expose. Healthcare providers conduct clinical trials to discover ADEs before selling the products but normally are limited in numbers. Thus, post-market drug safety monitoring is required to help discover ADEs after the drugs are sold on the market. 

Less than 5% of ADEs are reported via official channels and the vast majority is described in free-text channels: emails & phone calls to patient support centers, social media posts, sales conversations between clinicians and pharma sales reps, online patient forums, and so on. This requires pharmaceuticals and drug safety groups to monitor and analyze unstructured medical text from a variety of jargons, formats, channels, and languages - with needs for timeliness and scale that require automation. 

In the solution accelerator, we show how to use Spark NLP's existing models to process conversational text and extract highly specialized ADE and DRUG information, store the data in lakehouse, and analyze the data for various downstream use cases, including:

- Conversational Texts ADE Classification
- Detecting ADE and Drug Entities From Texts
- Analysis of Drug and ADE Entities
- Finding Drugs and ADEs Have Been Talked Most
- Detecting Most Common Drug-ADE Pairs
- Checking Assertion Status of ADEs
- Relations Between ADEs and Drugs

There are three noetbooks in this package:


1. `./01-ade-extraction`: Extract ADE, DRUGS, assertion status and relationships betwene drugs and ades
2. `./02-ade-analysis`: Create a deltakake of ADE and drugs  based on extracted entities and analyze the results (drug/ade correlations)
3. `./03-config`: Notebook for configurating the environment

<img src="https://drive.google.com/uc?id=1TL8z5cjKLgXjqCcbgIA4Lfg8M6lXmyzG">

## License
Copyright / License info of the notebook. Copyright [2021] the Notebook Authors.  The source in this notebook is provided subject to the [Apache 2.0 License](https://spdx.org/licenses/Apache-2.0.html).  All included or referenced third party libraries are subject to the licenses set forth below.

|Library Name|Library License|Library License URL|Library Source URL|
| :-: | :-:| :-: | :-:|
|Pandas |BSD 3-Clause License| https://github.com/pandas-dev/pandas/blob/master/LICENSE | https://github.com/pandas-dev/pandas|
|Numpy |BSD 3-Clause License| https://github.com/numpy/numpy/blob/main/LICENSE.txt | https://github.com/numpy/numpy|
|Apache Spark |Apache License 2.0| https://github.com/apache/spark/blob/master/LICENSE | https://github.com/apache/spark/tree/master/python/pyspark|
|MatPlotLib | | https://github.com/matplotlib/matplotlib/blob/master/LICENSE/LICENSE | https://github.com/matplotlib/matplotlib|
|Seaborn |BSD 3-Clause License | https://github.com/seaborn/seaborn/blob/master/LICENSE | https://github.com/seaborn/seaborn/|
|Plotly|MIT License|https://github.com/plotly/plotly.py/blob/master/LICENSE.txt|https://github.com/plotly/plotly.py|
|Spark NLP Display|Apache License 2.0|https://github.com/JohnSnowLabs/spark-nlp-display/blob/main/LICENSE|https://github.com/JohnSnowLabs/spark-nlp-display|
|Spark NLP |Apache License 2.0| https://github.com/JohnSnowLabs/spark-nlp/blob/master/LICENSE | https://github.com/JohnSnowLabs/spark-nlp|
|Spark NLP for Healthcare|[Proprietary license - John Snow Labs Inc.](https://www.johnsnowlabs.com/spark-nlp-health/) |NA|NA|


|Author|
|-|
|Databricks Inc.|
|John Snow Labs Inc.|

## Disclaimers
Databricks Inc. (“Databricks”) does not dispense medical, diagnosis, or treatment advice. This Solution Accelerator (“tool”) is for informational purposes only and may not be used as a substitute for professional medical advice, treatment, or diagnosis. This tool may not be used within Databricks to process Protected Health Information (“PHI”) as defined in the Health Insurance Portability and Accountability Act of 1996, unless you have executed with Databricks a contract that allows for processing PHI, an accompanying Business Associate Agreement (BAA), and are running this notebook within a HIPAA Account.  Please note that if you run this notebook within Azure Databricks, your contract with Microsoft applies.

The job configuration is written in the RUNME notebook in json format. The cost associated with running the accelerator is the user's responsibility.

## Instruction
To run this accelerator, set up JSL Partner Connect [AWS](https://docs.databricks.com/integrations/ml/john-snow-labs.html#connect-to-john-snow-labs-using-partner-connect), [Azure](https://learn.microsoft.com/en-us/azure/databricks/integrations/ml/john-snow-labs#--connect-to-john-snow-labs-using-partner-connect) and navigate to **My Subscriptions** tab. Make sure you have a valid subscription for the workspace you clone this repo into, then **install on cluster** as shown in the screenshot below, with the default options. You will receive an email from JSL when the installation completes.

<br>
<img src="https://raw.githubusercontent.com/databricks-industry-solutions/oncology/main/images/JSL_partner_connect_install.png" width=65%>

Once the JSL installation completes successfully, clone this repo into a Databricks workspace. Attach the RUNME notebook to any cluster running a DBR 11.0 or later runtime, and execute the notebook via Run-All. A multi-step-job describing the accelerator pipeline will be created, and the link will be provided. Execute the multi-step-job to see how the pipeline runs.