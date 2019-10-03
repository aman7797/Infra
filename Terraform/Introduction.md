# Introduction

## Installation

1. Lets start with the updating the system

        yum install update

2. Now install wget and unzip packages if they’re not already installed:
    
        yum install wget unzip

3. Now we will get Terraform zip from the Terraform official website [https://www.terraform.io/downloads.html](https://www.terraform.io/downloads.html)

4. Copy the download link from the website according to the system if it is 32 bit or 64 bit. You can get the link by right clicking and selecting the copy link address.
![installation Link](https://github.com/aman7797/Infra/blob/master/Terraform/img/installationLink.png)

5. Now run the command, to get the Terraform zip on Linux

        wget https://releases.hashicorp.com/terraform/0.11.13/terraform_0.11.13_linux_amd64.zip
    ![installation Link](https://github.com/aman7797/Infra/blob/master/Terraform/img/wgetTerraform.PNG)

6. Unzip the zip file to the  `/usr/local/bin/ `

        unzip ./terraform_0.11.13_linux_amd64.zip -d /usr/local/bin/
    ![installation Link](https://github.com/aman7797/Infra/blob/master/Terraform/img/unzipTerraform.PNG)

7. Terraform is Installed, to check 
        
        terraform -v
    ![installation Link](https://github.com/aman7797/Infra/blob/master/Terraform/img/installedTerraform.PNG)
    