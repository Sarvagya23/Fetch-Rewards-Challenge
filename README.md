
This document explains the steps invovled in accessing the data, focusing on unwrapping the jsons, adding them to different tables and getting insights thereafter.



## First: Review Existing Unstructured Data and Diagram a New Structured Relational Data Model

Refer to the ER_Diagram.png in the repository.

The primary keys across all three tables have been updated to user_id, brand_id, and receipt_id to reflect a more intuitive structure within the revamped database design.

A novel table, rewardReceipt, has been extracted from the 'rewardsReceiptItemList' field of the receipt table. This table is instrumental in delineating each transaction's items eligible for rewards, establishing a direct linkage between purchases and their corresponding rewards criteria. This linkage facilitates the accurate calculation and allocation of rewards to users based on their shopping activities.

Given the lack of uniqueness for 'brandCode' in this context, 'rewards_receipt_id' has been instituted as the new primary key for the rewardReceipt table. The inability to construct a composite unique key due to multiple items tied to a single 'receipt_id' further justifies this choice.

SQL Query for Specific Business Query
For direct SQL queries addressing specific business inquiries, please refer to the sql directory. This includes table creation queries and solutions tailored to the updated database structure available here.

Data Quality Evaluation
An in-depth analysis of Data Quality Issues is documented within the data_quality folder. This folder houses a Jupyter Notebook containing Python scripts for the evaluation of each JSON file. Additionally, reformatted JSON files post-structure revamp are located in the new_data directory.

 - brands_Analysis.ipynb
 - receipts_Analysis.ipynb
 - users_Analysis.ipynb


## Fourth: Communicate with Stakeholders
I have added the Business_Email.pdf which is a reference for the email to be sent to the stakeholders to get more clarity on the data to get more insights and make thing more clear before proceeding to work further.
