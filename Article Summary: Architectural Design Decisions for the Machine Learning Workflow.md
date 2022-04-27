**Article: S. Warnett and U. Zdun, "Architectural Design Decisions for the Machine Learning Workflow" in Computer, vol. 55, no. 03, pp. 40-51, 2022. Doi: 10.1109/MC.2021.3134800**


# 1.Introduction

The article describes a qualitative investigation of architectural decisions faced by professionals as current practices in machine learning (ML).

Ordinary ML developers are not typically trained in software engeneering (SE) and therefore are not routinely applied in engineering and architectural techniques. On the other hand, software engineers and architects typically do not work as ML and therefore regularly concern themselves with solutions for ML systems. The problems resulting from the divergence of these disciplines are further compounded by the technical challenges that often arise in ML projects that are often absent from non-ML projects, such as developing and maintaining ML solutions.

The aimed to identify relevant architectural concepts applied by practitioners in ML data processing, model building, and automated ML (AutoML). The result is a model of architectural design decisions (ADDs), decision options, considerations, and practices and their relations. 

# 2.The ML Workflow

An ML pipeline generally starts via a triggering event—perhaps manually or following a commit to the code base. This initiates the **data ingestion** step, where the data sets are updated, for example, by fetching the data fresh from a repository or using information received via a stream. The **data are then processed** in various ways and typically **transformed** (for instance, normalized then cleaned) before features are extracted. The features and processed data are passed to the **model-building** components, in which models are **trained**. The trained models are **deployed and can subsequently be used for predictions**.


# 3.ADDs

This section  contains detailed about the  model of architectural design decisions.

## 3.1 Data Processing

Data processing involves ingesting raw information into an ML workflow and transforming it into usable material that can be further processed by ML algorithms. Data are central to ML, and the main benefits of an ML approach lie in the processing of large volumes of information at scale. Typical phases of the data processing task involve selection, transformation, and output as well as the generation, storage, and versioning of artifacts, such as features and subset samples.

As with many other ML tasks, data processing can be performed manually or in an automated fashion. Data may be ingested manually, in real time (for example, streamed), batched, online, and offline with various implications for latency, throughput, reliability, and so on; Data labeling (for instance, for classification tasks) is another activity that may be performed manually as well as automatically. 



## 3.2 Model Building

Building an ML model involves applying a learning algorithm to features of a preprepared data set to yield predictions of a specific type such as qualitative (classification) and quantitative (regression) values. Hyperparameter tuning is the practice of adjusting values used by ML algorithms to optimize their performance metrics. This task may be automated or manual. The actual work involved in model building may be performed with tools, such
as integrated development environments (IDEs) and computational notebooks, or automatically, using AutoML and model-building pipelines.

## 3.3 AutoML

The AutoML decision consists of the following two parts:

1. whether AutoML should be applied;
2. which practices should be automated.

In particular, AutoML can automatically preprocess information during data preparation. It can be used while feature engineering to automatically
generate new features and select meaningful ones. Throughout model training, it can be applied to automatically train models, perhaps using different parameters and ML algorithms by applying hyperparameter tuning to data processing and model-building components and making a model selection, for example, based on ML as well as domain-related metrics. In this context, it can use validation to score the models.

One goal of applying AutoML is to require less manual tool creation effort,thus supporting higher development velocity and agility. This is achieved
through increased process and work automation, offering two further key benefits: via automation, AutoML offers a greater level of explainability and reproducibility in the data processing and model-building tasks, as every step follows precisely specified algorithms. Unfortunately, existing AutoML solutions do not always deliver results to the desired quality standards, which often results in a negative impact on production-ready development, potentially leading to additional development work. Extra tool development for engineering the AutoML solution would also be required in this case.


