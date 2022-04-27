**Article: S. Warnett and U. Zdun, "Architectural Design Decisions for the Machine Learning Workflow" in Computer, vol. 55, no. 03, pp. 40-51, 2022. Doi: 10.1109/MC.2021.3134800**


# 1.Introduction

The article describes a qualitative investigation of architectural decisions faced by professionals as current practices in machine learning (ML).

Ordinary ML developers are not typically trained in software engeneering (SE) and therefore are not routinely applied in engineering and architectural techniques. On the other hand, software engineers and architects typically do not work as ML and therefore regularly concern themselves with solutions for ML systems. The problems resulting from the divergence of these disciplines are further compounded by the technical challenges that often arise in ML projects that are often absent from non-ML projects, such as developing and maintaining ML solutions.

The aimed to identify relevant architectural concepts applied by practitioners in ML data processing, model building, and automated ML (AutoML). The result is a model of architectural design decisions (ADDs), decision options, considerations, and practices and their relations. 

# 2.The ML Workflow

An ML pipeline generally starts via a triggering event—perhaps manually or following a commit to the code base. This initiates the data ingestion step, where the data sets are updated, for example, by fetching the data fresh from a repository or using information received via a stream. The data are then processed in various ways and typically transformed (for instance, normalized then cleaned) before features are extracted. The features and processed data are passed to the model-building components, in which models are trained. The trained models are deployed and can subsequently be used for predictions.


# 3.ADDs

This section  contains detailed about the  model of architectural design decisions.

## 3.1 Data Processing

## 3.2 Model Building

## 3.3 AutoML



