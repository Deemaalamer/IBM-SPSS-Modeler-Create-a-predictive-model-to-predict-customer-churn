# IBM-SPSS-Modeler-Create-a-predictive-model-to-predict-customer-churn
Get experience with IBM SPSS Modeler by creating a decision-tree machine-learning model to evaluate the risk that a customer might leave your service. This is a set by step tutorial. Credits to this demo https://www.ibm.com/cloud/garage/demo/try-spss-modeler/

### Duration: 15 minutes
In this tutorial demo, you use IBM SPSS Modeler to build a machine-learning model to predict which customers might leave your service.

## Task 1: Create project and upload data set

## Task 2: Create SPSS modele

## Task 3: Inspect the data set

You have a data set with customer data and churn data. The data engineer merged both data sets into one set. The data set is waiting for inspection on the canvas. In this task, you inspect the data set by using IBM SPSS Modeler.
<ul>
<li>1. Click Customers.xlsx. From the menu that opens, click Preview. The first 10 records of the data set are shown.</li>
<li>Scroll to inspect the right part of the data set. The last column, CHURN, contains data about whether a customer churned or not. Click OK to close Preview window.</li>

In the palette, click the Output tab.

Add the Data Audit node to the canvas by clicking Data Audit.

Connect the Data Audit node to the Customers.xlsx node by clicking Customers.xlsx. The Data Audit node is automatically renamed to "17 Fields."

Click 17 Fields. From the menu that opens, click Run. You can review key statistics and metrics for the data set.

Click the Quality tab to review the data set quality. When you're finished, click OK to close the window.

</ul>

Task 2: Prepare the data set

Get the data set ready for machine learning.

    In the palette, click the Field Ops tab.

    Add the Type node to the canvas by clicking Type.

    Connect the Customers.xlsx node to the Type node by clicking Customers.xlsx.

    Click Type. From the menu that opens, click Edit.

    In the Type window, set the measurement level of the columns by clicking Read Values. On the ID row, click Input. From the menu that opens, click Record ID to change the role.

    Scroll to the CHURN row.

    Click CHURN and change the role from Input to Target. The CHURN row is used as the target to predict in your machine-learning model.

    Click Apply and then click OK.

Task 3: Train the model

Train a C&R Tree model with your data set.

    In the palette, click the Modeling tab.

    Add the C&R Tree node to the canvas by clicking C&R Tree.

    Connect the C&R Tree node to the Type node by clicking Type. The C&R Tree node is automatically renamed to "CHURN."

    Click CHURN. From the menu that opens, click Run. The model is trained and a new CHURN node that looks like a golden nugget is added to the canvas.

    Click the CHURN golden nugget node. From the menu that opens, click Edit. Review the model and notice which features are important predictors. When you're finished, click OK to close the window.

Task 4: Evaluate and visualize the model

Evaluate the model performance and visualize the model by using a gain chart.

    In the palette, click the Output tab.

    Add a Table node to the canvas by clicking Table.

    Add an Analysis node to the canvas by clicking Analysis.

    Connect the CHURN golden nugget node to the Table and Analysis nodes by clicking the CHURN golden nugget node.

    Click the CHURN golden nugget node again. From the menu that opens, click Run from here. In the window that opens, review the results on the Table tab.

    Scroll to the right and notice that two columns were added to the data set: $R-CHURN and $RC-CHURN. The $R-CHURN column is the prediction column. The $RC-CHURN column is the confidence level column. Click OK to close the window.

    Review the model performance, or accuracy, in the Analysis table. Click OK to close the window.

    In the palette, click the Graphs tab.

    Add the Evaluation node to the canvas by clicking Evaluation.

    Connect the Evaluation node to the CHURN golden nugget node by clicking the CHURN golden nugget node.

    Click R-CHURN. From the menu that opens, click Run. Review the gain chart. When you're finished, click OK to close the window.

Summary

You completed the tutorial. Congratulations!

In this tutorial, you completed these tasks:

    Inspected a data set for customer churn
    Prepared the data set for machine learning
    Trained and evaluated a machine-learning model
    Displayed a gain chart of the model

This demo scratches the surface of many of the powerful capabilities of IBM SPSS Modeler. To explore more capabilities, sign up for a free trial.
Learn more

Data and analytics reference architecture
