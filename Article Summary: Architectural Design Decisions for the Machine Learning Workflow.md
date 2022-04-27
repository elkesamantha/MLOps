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

As with many other ML tasks, data processing can be performed manually or in an automated fashion. Data may be ingested manually, in real time (for example, streamed), batched, online, and offline with various implications for latency, throughput, reliability, and so on; Data labeling (for instance, for classification tasks) is another activity that may be performed manually as well as automatically, and we consider the implications. 



## 3.2 Model Building

## 3.3 AutoML



