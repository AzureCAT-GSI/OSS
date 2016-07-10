#Java Demo
Included below are step-by-step instructions for demonstrating Azure Eclipse Add-in and its integration with Azure Web Apps

##Pre-requisites
**Steps needed to setup the demo**

  1. Install Java SDK 8 from [here] (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
  2. Intall Eclipse IDE (Neon) from [here] (https://www.eclipse.org/downloads/)
  3. Install Tomcat from [here] (http://tomcat.apache.org/download-80.cgi) *(download and extract the zip file)*

  ![Download Tomcat](media/image002.jpg)

##Setup Eclipse Plugin for Java
**Install the Azure toolkit for Eclipse**

  4. Launch Eclipse IDE. From the welcome screen, click **Help** and then click **Install New Software**
    ![Help Menu Item](media/image022.jpg)

  5. In the next screen, in the Work with text box type **http://dl.microsoft.com/eclipse** and press **ENTER**. Select **Azure Toolkit for Java**, clear the check box for **Contact all update sites during install to find required software**, and then click **Next**. 
    ![Install Screen](media/image024.jpg)

  6. In the Install Details dialog box review the components that will be installed and then click Next.
  7. In the Review Licenses dialog box, accept the terms of the license, and then click Finish.
  8. Once the installation is completed, you will be prompted to restart Eclipse. Click Yes from the dialog box to restart Eclipse.

*(**IMPORTANT** - HDInsight plugin for Eclipse will not install if Scala IDE for Eclipse is not installed. you can add the Scala IDE plugin by going to Help -> Install New SoftWare, and add http://download.scala-ide.org/sdk/lithium/e44/scala211/stable/site as source to download Scala Plugin for Eclipse.)*

##Log into Azure Subscription
  9. Open the Azure Explorer. From the Window menu in the IDE, click Show View and then click Other. From the dialog box that opens, expand Azure, click Azure Explorer, and then click OK.
    ![Azure Explorer](media/image064.jpg)

  10. Right-click the Azure node in the Azure Explorer, and then click Manage Subscriptions.
  11. In the Manage Subscriptions dialog box, click Sign in and enter your Azure credentials.
    ![Manage Subscriptions](media/image065.jpg)

  12. After you are logged in, the **Manage Subscriptions** dialog box lists all the Azure subscriptions associated with the credentials. Click **Close** in the dialog box.


##Create a Demo Web Project

  13. Create a new Dynamic Web Project in Eclipse
      ![Dynamic Web Project](media/image028.jpg)

  14. Provide a name for the project and click finish
      ![Web Project Properties(media/image030.jpg)

  15. Within Eclipse’s Project Explorer view, expand AzureJavaProject. Right-click WebContent, click New, and then click JSP file. Name it *index.jsp*. Click Finish
      ![New JSP file](media/image032.jpg)

  16. Add the below line within <body/> tags - <b><% out.println("Hello From Microsoft"); %></b>
      ![Edit JSP file](media/image038.jpg)

  17. Notice the red X icon in the margin at the top of the index.jsp file.  If you hover over that, you’ll see an error: *The superclass "javax.servlet.http.HttpServlet" was not found on the Java Build Path* - Resolution explained below...
	![Error](media/image040.jpg)

  18. Right-click on the ‘AzureJavaProject’ project and choose Properties.  
  19. Go to the Project Facets node, choose the Runtimes tab, and click New.
	![Project Facets](media/image042.jpg)

  20. Select 'Apache Tomcat v8.0' 
	![Server Runtime](media/image044.jpg)

  21. On the Tomcat Server page, provide the path to the folder where you extracted Apache Tomcat to in the “Tomcat installation directory” textbox.  Click Finish.
	![Tomcat Server](media/image046.jpg)

  22. *Check* the server in the *runtimes* pane
	![Projet Facets](media/image048.jpg)

 
#Create an Azure Deployment Project

  23. Right-click the web project and choose *package for Azure*
	![Package for Azure](media/image066.jpg)

  24. Click 'New' from 'Deploy to Azure Web App Container' popup
	![New Web App](media/image067.jpg)

  25. Fill-in details for the new Web App
	![New Web App Properties](media/image068.jpg)

  26. New Web App is Provisioned
	![Web App Provisioned] (media/image069.jpg)

  27. Publish the Web App. Click 'Published' link to view the Site.
	![Published Web App](media/image070.jpg)

  28. View the newly provisioned Web App in the [Azure Portal] (http://portal.azure.com)
	![Web App in Portal](media/image071.jpg)

  29 Highlight Java selection in Azure Web Apps Settings
	![Java Properties](media/image072.jpg)

 
##How to Debug Azure Web Apps in Eclipse

  30. In Eclipse, right click on a Web App project and select Debug As, then click on Azure Web App
	![Debug As](media/image073.jpg)

  31. Accept the default values set by the Toolkit and click on Debug
	![Debug Web App](media/image075.jpg)

  32. If a popup is displayed, click OK
	![Enable Remote Debugging](media/image074.jpg)

  33. IDE will go ahead and enable remote debugging on Azure and launch a command prompt or shell that will prepare necessary remote connection for debugging. Then, insert a break point in a JSP or servlet in the Web App, open the Java Web App URL in a browser, and the IDE will now enter into debug mode. Start stepping through code and inspecting variables, as you have always been
	![Debug Web App](media/image076.jpg)

*(**For More Details** - Read the documentation pages about remote debugging Java Web Apps on Azure in [Eclipse](https://azure.microsoft.com/en-us/documentation/articles/app-service-web-debug-java-web-app-in-eclipse/))*
