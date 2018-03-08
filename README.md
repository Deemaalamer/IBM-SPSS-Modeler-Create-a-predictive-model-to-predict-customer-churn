# IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn
Get experience with IBM SPSS Modeler by creating a decision-tree machine-learning model to evaluate the risk that a customer might leave your service. This is a set by step tutorial. Credits to this demo https://www.ibm.com/cloud/garage/demo/try-spss-modeler/

### Duration: 15 minutes
In this tutorial demo, you use IBM SPSS Modeler to build a machine-learning model to predict which customers might leave your service.

## Task 1: Login to IBM Cloud and create Data Science Experince service

1. Login to your IBM Cloud account, if you don't have one already you can signup here.
2. Open the Catalog, click on **Data & Analytics** to refine search.
3. Scrol down and click on **Data Science Experince** service.
4. Click on **Create** to create an instance of the service.
5. Click on **Getting started** to open the tool.

(gif)

## Task 2: Create project

Once you have logged you you can go ahead and create a project.

1. Scrol down the page and click on **(+) New project** icon.
2. Name your project 'Predict customer churn'.
3. Scroll down, under Define storage click on **Add** to create an IBM Cloud Object Storage instance. The service will open up, choose the **Lite** plan then click **Create**.

(gif)

4. Under Spark service click on **Add** to create an IBM Analytics for Apache Spark instance.The service will open up, choose the **Lite** plan then click **Create**.
5. Refresh page to make sure services are added.

(gif)

6. Click Create, to finish creating your project.


## Task 3: Upload data set

1. Download the data set ![Data set](www.google.com)
2. In your project page, nagivate to the Assests tab, drag the data set file you downloaded and drop it in the Load sidebar.
3. Your data set should be loaded successfully shorty!

![Upload dataset](https://github.com/Deemaalamer/IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn/blob/master/images/dsx3.gif)


## Task 4: Create SPSS modele

1. Same page as before, scroll down to the Modeler flows.
2. Hit the (+) New flow icon
3. Under the 'New' tab, name your modeler 'Predictive model', make sure you chose IBM SSPS Modeler Runtime. Then click Create.

![Create SPSS modele](https://github.com/Deemaalamer/IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn/blob/master/images/dsx4.gif)

## Task 5: Inspect the data set
You have a data set with customer data and churn data. The data engineer merged both data sets into one set. The data set is waiting for inspection on the canvas. In this task, you inspect the data set by using IBM SPSS Modeler.

1. Drag and drop your data set to the canvas.
2. Click Customers.xlsx. From the menu that opens, click **Preview**. The first 10 records of the data set are shown.
3. Scroll to inspect the right part of the data set. The last column, CHURN, contains data about whether a customer churned or not. 
4. Click **OK** to close Preview window.

(gif - dsx5&dsx6merge)

3. In the palette, click the Output tab.
4. Add the Data Audit node to the canvas by clicking Data Audit.
5. Connect the Data Audit node to the Customers.xlsx node by clicking Customers.xlsx. The Data Audit node is automatically renamed to "21 Fields."
6. Click 21 Fields. From the menu that opens, click Run. You can review key statistics and metrics for the data set. When you're finished, click OK to close the window.

![Add data audit](https://github.com/Deemaalamer/IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn/blob/master/images/dsx7.gif)

## Task 6: Prepare the data set
Get the data set ready for machine learning.

1. In the palette, click the **Field Ops** tab.
2. Add the **Type** node to the canvas by clicking **Type**.
3. Connect the Customers.xlsx node to the Type node by clicking Customers.xlsx.
4. Click **Type**. From the menu that opens, click **Open**.
5. In the right side bar, expland **settings**.
6. Click **Configure types**.
7. Set the measurement level of the columns by clicking Read Values. On the CustomerID row, click Input. From the menu that opens, click Record ID to change the role.
6. Scroll to the CHURN row.
7. Click CHURN and change the role from Input to Target. The CHURN row is used as the target to predict in your machine-learning model.
8. Click Apply and then click OK.

![Prepare data](https://github.com/Deemaalamer/IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn/blob/master/images/dsx8.gif)

## Task 7: Train the model
Train a C&R Tree model with your data set.

1. In the palette, click the **Modeling** tab.
2. Add the C&R Tree node to the canvas by clicking **C&R Tree**.
3. Connect the **C&R Tree** node to the Type node by clicking **Type**. The C&R Tree node is automatically renamed to "CHURN."
4. Click CHURN. From the menu that opens, click Run. The model is trained and a new CHURN node that looks like a golden nugget is added to the canvas.
5. From the output click on results. Review the model and notice which features are important predictors. When you're finished, click OK to close the window.

![Train model](https://github.com/Deemaalamer/IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn/blob/master/images/dsx9.gif)

## Task 8: Evaluate and visualize the model
Evaluate the model performance and visualize the model by using a gain chart.

1. In the palette, click the **Output** tab.
2. Add a Table node to the canvas by clicking **Table**.
3. Add an Analysis node to the canvas by clicking Analysis.
4. Connect the CHURN golden nugget node to the Table and Analysis nodes by clicking the CHURN golden nugget node.
5. &&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
5. Click the CHURN golden nugget node again. From the menu that opens, click Run from here. In the window that opens, review the results on the Table tab.
6. Scroll to the right and notice that two columns were added to the data set: $R-CHURN and $RC-CHURN. The $R-CHURN column is the prediction column. The $RC-CHURN column is the confidence level column. Click OK to close the window.
7. Review the model performance, or accuracy, in the Analysis table. Click OK to close the window.

![Evaluate model](https://github.com/Deemaalamer/IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn/blob/master/images/dsx10.gif)

8. In the palette, click the Graphs tab.
9. Add the Evaluation node to the canvas by clicking Evaluation.
10. Connect the Evaluation node to the CHURN golden nugget node by clicking the CHURN golden nugget node.
11. Click R-CHURN. From the menu that opens, click Run. Review the gain chart. When you're finished, click OK to close the window.

![Evaluate model](https://github.com/Deemaalamer/IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn/blob/master/images/dsx11.gif)


## Summary

You completed the tutorial. Congratulations!

In this tutorial, you completed these tasks:

**1. Inspected a data set for customer churn**
**2. Prepared the data set for machine learning**
**3. Trained and evaluated a machine-learning model**
**4. Displayed a gain chart of the model**

This tutorial scratches the surface of many of the powerful capabilities of IBM SPSS Modeler. 
