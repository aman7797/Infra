1. How do all these tools work together?  Explain with example and execute any sample project

    **Git :** Version Control System tool    
    **Jenkins :** Continuous Integration tool  
    **Selenium :** Continuous Testing tool  
    **Puppet, Chef, Ansible :** Configuration Management and Deployment tools   
    **Nagios :** Continuous Monitoring tool  
    **Docker :** Containerization tool

## Starting with Assignment

### Jenkins Installation
1. Download the  Jenkins zip from [Jenkins website](https://jenkins.io/)
2. Extract the downloaded zip
3. Install the setup
4. Now start the Jenkins by going to the Jenkins Directory `C:\Program Files (x86)\Jenkins`
    
        jenkins.exe start
5. Now open http://localhost:8080/ in browser.
![JenkinsHome](\img\InstallationJenkins.PNG)

### Git Plugin - Installation
1. Open Jenkins Dashboard
2. Click on **Manage Jenkins** 
![JenkinsHome](\img\ManageJenkins.PNG)
3. Now click **Manage Plugins**
![JenkinsHome](\img\ManagePlugin.PNG)
4. Check if Git is installed or not
![JenkinsHome](\img\GitPlugin.PNG)
If Git is not installed   
a. Click on Available  
b. Find Git and click the checkbox  
c. Press Install without restart

### Git and GitHub Integration with Jenkins
1. Click on **New Item**
![JenkinsHome](\img\ManageJenkins.PNG)
2. Enter the Name as per the repositories and select **Freestyle Project**
![JenkinsHome](\img\ItemName.PNG)
3. Select **Source Code Management** as **Git** and enter the Git **Repository URL**
![JenkinsHome](\img\GitRepo.PNG)
4. Not require to change the any other settings
5. Click Save

### Build Project
1. Select the Project
![JenkinsHome](\img\SelectProject.PNG)
Click on Infra
2. Click on Build Now
![JenkinsHome](\img\BuildNow.PNG)
A build will start 
![JenkinsHome](\img\BuildStart.PNG)
3. Select the Build after it get completed you can check the logs of the build under Console Output
![JenkinsHome](https://github.com/aman7797/Infra/blob/master/Assignment%201/img/ConsoleOutput.PNG)


