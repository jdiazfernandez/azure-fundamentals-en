---
wts:
    title: 'Create a VM with a Template'
    module: 'Module 02 - Core Azure Services'
---
# Create a VM with a Template

In this walkthrough, we will deploy a virtual machine with a QuickStart template and examine monitoring capabilities.

# Task1: Explore the gallery and locate a template

In this task, we will browse the Azure QuickStart gallery and deploy a template that creates a virtual machine. 

1. In a browser, access the [Azure Quickstart Templates gallery](https://azure.microsoft.com/resources/templates?azure-portal=true). In the gallery you will find a number of popular and recently updated templates. These templates automate deployment of Azure resources, including installation of popular software packages.

2. Browse through the many different types of templates that are available. 

    **Note**: Are there are any templates that are of interest to you?

3. Search for or directly access the 'Deploy a simple Windows VM with tags' template.

    **Note**: The **Deploy to Azure** button enables you to deploy the template via the Azure portal. During such deployment, you will be prompted only for small set of configuration parameters. 

4. Review different options. Click Browse Code button and click Visualize.
   
6. Click the **Deploy to Azure** button. Your browser session will be automatically redirected to the [Azure portal](http://portal.azure.com/).

7. If prompted, sign in to the Azure subscription you want to use in this lab.

8. Click **Edit template**. Review the template. The Resource Manager template format uses the [Bicep format](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview?tabs=bicep). **Discard**. You are returned to the **Custom deployment** blade in the Azure portal.
    
9. On the **Custom deployment** blade configure the parameters required by the template (replace ***xxxx*** in the DNS label prefix with letters and digits such that the label is globally unique). Leave the defaults for everything else. 

    | Setting| Value|
    |----|----|
    | Subscription | **Choose your subscription**|
    | Resource group | **myRGTemplate** (create new) |
    | Region | **West Europe** |
    | Admin username | **azureuser** |
    | Admin password | **Pa$$w0rd1234** |
    | Dns Label Prefix| ***Leave at the default***| 
    | Windows OS version | **2019-Datacenter** |
    | Departament Name | **e.g. your course** |
    | Application Name | **e.g. your subject*** |
    | Created By | **your name** |
    | | |

11. Monitor your deployment. 

# Task 2: Verify and monitor your virtual machine deployment

In this task, we will verify the virtual machine deployed correctly. 

1. From the **All services** blade, search for and select **Virtual machines**.

2. Ensure your new virtual machine was created. 

    ![Screenshot of the virtual machines page. The new VM is shown and running.](../images/0902.png)

3. Select your virtual machine and on the **Overview** pane scroll down to view properties and monitoring data.

    **Note**: The monitoring timeframe can be adjusted from one hour to 30 days.

4. Review different charts that are provided including **VM Availability**, **CPU (average)** and **Disk bytes (total)**. Show more metrics: **Network (total)**, **Disk operations/sec (average)** ...

    ![Screenshot of the virtual machine monitoring charts.](../images/0903.png)

5. Note that you can **Add metric** and change the chart type. As you have time, experiment. 

6. Return to the **Overview** blade.

7. Click on the **Activity log** (left pane). Activity logs record such events as creation or modification of resources. 

8. Click **Add filter**, and experiment with searching for different event types and operations. 

    ![Screenshot of the Add filters page with Event type selected.](../images/0904.png)

**Note**: To avoid additional costs, you can remove this resource group. Search for resource groups, click your resource group, and then click **Delete resource group**. Verify the name of the resource group and then click **Delete**. Monitor the **Notifications** to see how the delete is proceeding.
