<properties
	pageTitle="Team Data Science Process: An Overview"
	description="An outline of the key components of the Team Data Science Team."  
	services="machine-learning"
	documentationCenter=""
	authors="bradsev"
	manager="jhubbard"
	editor="cgronlun" />

<tags
	ms.service="machine-learning"
	ms.workload="data-services"
	ms.tgt_pltfrm="na"
	ms.devlang="na"
	ms.topic="article"
	ms.date="09/22/2016"
	ms.author="bradsev;hangzh;deguhath"/>

# Team Data Science Process: An Overview

The Team Data Science Process (TDSP) is an agile, iterative data science methodology to deliver predictive analytics solutions and intelligent applications efficiently. TDSP helps improve team collaboration and learning. TDSP is a distillation of the best practices and structures from Microsoft and others in the industry that facilitate the successful implementation of data science initiatives that help companies fully realize the benefits of their analytics program.

This article provides an overview of TDSP and its main components. We provide a generic description of the process here that can be implemented with a variety of tools. In the detailed articles, we also provide guidance on how to implement the TDSP using a specific set of Microsoft tools and infrastructure that we use to implement the TDSP in our teams. 

## Key components of the TDSP

TDSP comprises of the following key components :  

* A **data science lifecycle** definition  
* A **standardized project structure** 
* **Infrastructure and resources** for data science projects 
* **Tools and utilities** for project execution

## 1. Data Science Lifecycle 

Data Science is a highly iterative discovery process with emphasis on evaluating and validating each step of the process. The process iterations refine the hypotheses and predictive models to obtain a sound solution. The data science lifecycle defines a systematic sequence of steps that starts with the planning step, where the business problem is framed, proceeds to the development of predictive analytics models, and completes with their consumption of predictions by intelligent applications. If you are using an existing lifecycle like [CRISP-DM](https://wikipedia.org/wiki/Cross_Industry_Standard_Process_for_Data_Mining), [KDD](https://wikipedia.org/wiki/Data_mining#Process) or your own custom process that is working well in your organization, you can still use TDSP in the context of those development lifecycles. If you dont have one in use already, TDSP provides a staged data science lifecycle for you to adopt. At a high level, the different methodologies have much in common. You can easily map the correspondences between the steps in the TDSP lifecycle and in these other popular methodologies. Here is a depiction of the TDSP lifecycle. 

![TDSP_LIFECYCLE](./media/overview/tdsp-lifecycle.jpg) 

Details of each stage of the lifecycle in TDSP are found [here](lifecycle-detail.md). 

The following diagram provides the detailed task view for each of the role working together on a data science initiative in each stage of the lifecycle. The prescribed documentation artifacts are indicated in the diagram too. 

![TDSP_SWIMLANE](./media/overview/tdsp-swimlane.png)

## 2. Standardized project structure
Having all projects share a directory structure and use templates for project documents makes it easy for the team members to find information about their projects. All code and documents are stored in a version control system (VCS) like Git, TFS, or Subversion to enable team collaboration. Tracking tasks and features in an Agile project tracking system like Jira, Rally, Visual Studio Team Services, and optionally linking them to a VCS allows closer tracking of code for individual features and enables teams to obtain better cost estimates. TDSP recommends creating a separate **repository** for each project on the VCS for versioning, information security, and collaboration. The standardized structure for all projects helps build institutional knowledge across the organization. 

We provide templates for the folder structure and required documents. The folder structure organizes files such as code for data exploration, feature extraction, and model iterations in standard locations. This makes it easier for team members to understand work done by others and to add new members to teams. It is easy to view and update document templates in markdown format. Use templates to provide checklists with key questions for each project to insure problem is well defined and deliverables meet the quality expected. Examples include:

* a project charter to document the business problem and scope of the project 
* data reports to document the structure and statistics of the raw data
* model reports to document the derived features
* model performance metrics such as ROC curves or MSE

![TDSP_DIR_STRUCT](./media/overview/tdsp-dir-structure.png) 

The directory structure can be cloned from [Github](https://github.com/Azure/Azure-TDSP-ProjectTemplate). 

## 3. Infrastructure and resources for data science projects
TDSP provides recommendations for managing shared analytics and storage infrastructure such as cloud file systems for storing datasets, databases, Big Data (Hadoop, Spark) clusters, and machine learning services. The analytics and storage infrastructure can be on the cloud or On-premises. This is where raw and processed datasets are stored. This infrastructure enables reproducible analysis. It also avoids duplication, which can lead to inconsistencies and unnecessary infrastructure costs. Tools are provided to provision the shared resources, track them, and allow each team member to connect to those resources securely. It is also a good practice have project members create a consistent compute environment so experiments can be replicated and validated by different team members. 

Here is an example of a team working on multiple projects and sharing various cloud analytics infrastructure components. 

![TDSP_INFRA](./media/overview/tdsp-analytics-infra.png)
## 4. Tools and utilities for project execution

Introducing processes in most organizations is challenging. By providing tools to implement the data science process and lifecycle, we not only get the benefits of productivity but also of consistency in its adoption. TDSP provides an initial set of tools and scripts to jump start adoption of TDSP within a team and to automate some of the common tasks in the data science lifecycle such as data exploration and baseline modeling. There is a well-defined structure provided for individuals to contribute shared tools and utilities into their team’s shared code repository.  These resources can then be leveraged by other projects within the team or the organization. In future TDSP also plans to enable the contributions of tools and utilities to the whole community. 
The TDSP utilities can be cloned from [Github](https://github.com/Azure/Azure-TDSP-Utilities). 

## Next steps: [Team Data Science Process: Roles and tasks](./roles-tasks.md)


