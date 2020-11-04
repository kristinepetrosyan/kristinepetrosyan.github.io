---
layout: post
title:      "How to choose your own training environment for Data "
date:       2020-11-04 18:38:15 +0000
permalink:  how_to_choose_your_own_training_environment_for_data
---


### 1. Jupyter Notebook
Jupyter Notebook is an open source application which helps to create and share documents that contain code, equations, visualizations and text. It supports languages of Python, R and Julia. Their main use is in computational physics and data analysis. Jupyter notebooks are more focused on making work easier to understand.

### 2. Google colab
Google Colab is a cloud service provided by Google and supports free GPU and is based on Google Jupyter Notebooks environment. It helps data scientists to develop deep learning projects using commonly used libraries such as PyTorch, Keras and TensorFlow. It is convenient especially if you don’t want your machine to carry the load of heavy workout of your Data science operations. You can create notebooks in Colab, upload notebooks, store notebooks, share notebooks, mount your Google Drive and use whatever you’ve got stored in there, import most of your favorite directories, upload your personal Jupyter Notebooks, upload notebooks directly from GitHub, upload Kaggle files, download your notebooks, and much more.
From visual perspective Colab looks similar to the Jupyter interface but working in Colab is much more easier compared to working in the Jupyter Notebook. Overall look and functionality is similar but there are few differences:
Most of the menu items are different.
Colab has changed some of the standard terminologies (“runtime” instead of “kernel”, “text cell” instead of “markdown cell”, etc.)
Colab has “playground mode.”
Command mode and Edit mode in Colab work differently than they do in Jupyter.
You can upload a dataset to use within a Colab notebook, but it will automatically be deleted once you end your session so in order to have the saved version you have to save the copy in the drive.
Colab gives you access to a GPU or a TPU. If you connect Colab to Google Drive, that will give you up to 15 GB of disk space for storing your datasets. Sessions will shut down after 60 minutes of inactivity, though they can run for up to 12 hours.The most important strength of Colab is that it’s easy to get started and it’s easy to share notebooks since the sharing functionality works the same as Google Docs. However, the cumbersome keyboard shortcuts and the difficulty of working with datasets are significant drawbacks.

### 3.Azure Notebooks
Azure notebooks is a service provided by Microsoft which is very similar to Colab in terms of functionality and also Amazon SageMaker. Both platforms have a cloud sharing functionality . Azure Notebooks is much faster and is much better than Colab in this regard. It has a memory of 4 gigabytes. Azure Notebooks creates a collection of related notebooks called Libraries. These libraries are the size of each data file as less than 100 megabytes. These Notebooks work with languages like Python and R. Azure Notebooks is more suitable for simple applications.

### 2.Kaggle
Kaggle is a great platform for deep learning applications in the cloud. Kaggle and Google Colab have some similarities and the one of them is that both are products of Google.Kaggle lets the user use the GPU in the cloud for free. It provides Jupyter Notebooks in the browser and most of Jupyter Notebook keyboard shortcuts are exactly the same as Kaggle. It has many datasets that can be imported. Kaggle Kernels often seem to experience a little lag but is faster than Colab. Kaggle has a large community to learn and use data science skills and more suitable for people who do projects in their studies.

### 3.Amazon SageMaker
Amazon SageMaker is a machine learning service which has notebook running on the Jupyter Notebook App. This service which is provided by Amazon helps to create and manage Jupyter notebooks that can further be used to process data and further train and deploy ML models. For the training and deployment of the models, it provides APIs. It allows for easy integration of ML models in applications. Amazon SageMaker offers flexible distributed training options that adjust to your specific workflows.
SageMaker is built on top of other AWS services specifically to help Data scientists. Notebook, training, and deployment machines are just ordinary EC2 instances running specific Amazon Machine Images. Data is stored in S3 object storage which means you have to upload all your data to S3. This might be troubling if you are working with images or huge datasets. SageMaker then automatically downloads the data from S3 to every training instance before starting the training. It takes at least 20 minutes to download 100Gb worth of data and you have to wait at least 25 minutes before the training begins.
### 4.IBM DataPlatform Notebooks
Similar to Amazon, Azure and Google IBM also came up with Watson Data Platform and Data Science Experience (DSX) with support for open-source options. It eventually started its platform for multi-cloud freedom of choice for data science work. This was done with the help of containerization of the product by way of Kubernetes. As a result, it can be deployed in Docker or CloudFoundry containers wherever the data resides. If we compare IBM DataPlatform Notebooks to Google Colab, they have containerization for multi-cloud deployment. IBM supports containerization because it encourages customers to be able to analyze data and build, deploy and run models anywhere. DSX provides permission-controlled, collaborative access to projects, data, data science tools, services, and community space. DataPlatform Notebooks supports languages of R, Python and Scala and supports Jupyter and Apache Zeppelin notebooks. DSX users can use open source libraries including Spark MLlib, TensorFlow, Caffe, Keras and MXNet.

### 5. Saturn Cloud
Saturn Cloud is a new tool for data scientists who are not interested in setting up infrastructure but care more about doing data science easily. This platform helps manage Python environments in the cloud. Using Saturn Cloud you can share your notebooks with others without having to deal with the hassle of making sure they have all the correct libraries installed. This is huge advantage compared to Google Colab. Additionally it allows you to start virtual machines with the whatever memory and RAM required.
Conclusion
Looking at pros and cons of the above mentioned technologies which we went over I felt more inclined towards Google Colab especially for Deep learning projects.

## Google Colab:
- Notebooks can be saved in Google Drive and can be accessed from any computer.
- Don’t need to worry about conda create env
- Sharing with others is super easy just like Google Doc.
- No need to save versions, it is automatic
- Free GPU
- %matplotlib inline not needed
- Many libraries are already installed
- Cleaner interface# Enter your title here

https://kristinelpetrosyan.medium.com/how-to-choose-your-own-training-environment-for-data-science-projects-74e53122cb4a
