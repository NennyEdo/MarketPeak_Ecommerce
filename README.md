#  Deploy an e-commerce website on AWS EC2 instance.
-This project utilizes Git for version control in linux environment to deploy an e-commerce website on AWS EC2 instance.
## Tasks
1. Implement version control with Git.
   
   1.1. Initialize Git Repository.
   
  - Create project directory named "**MarketPeak_Ecommerce**" and initialize Git repository.
    ```bash
      mkdir MarketPeak_Ecommerce
      git init
    ```
    
     1.2. Obtain and prepare e-commerce website Template [Sample Template](https://www.tooplate.com/download/2130_waso_strategy)

     -Extract downloded template to "**MarketPeak_Ecommerce**"

    1.3. Stage and commit template to Git.
       - Add website to the git repository.
         ```bash
            git add .
       - set git global configuration with username and email.
         ```bash
            git config --global user.name "NennyEdo"
            git config --global user.email "myemail@example.com"
       - commit changes with descriptive message.
         ```bash
            git commit -m "Initial commit with basic e-commerce site structure"
         
      1.4. Create and push code to remote Repository

       - Remote reository name and actual git username "**MarketPeak_Ecommerce**"
          ```bash
          git remote add origin https://github.com/your-git-username/MarketPeak_Ecommerce.git
          ```
       - upload local Repository content to Github
         ```bash
         git push -u origin main
         ```
   2. AWS Deployment
      
      2.1. Set up an AWS EC2 instance
      -    Log in to AWS Management console
      -    Launch an EC2 Instance with Amazon linux
      -    Connect to instance with SSH
     
      2.2. Clone Repository on Linux server with SSH authenticaion
      
      -    Go to the Github repository
      -    On your EC2 instance, generate SSH-Keypair using SSH-Keygen
      -    Display and copy key
     
        ```bash
        cat /home/ubuntu/.ssh/id_rsa.pub
        ```
      -   Add SSH public key GitHub account
      -   Clone SSH to Repository
     
        ```bash
        git clone git@github.com:yourusername/MarketPeak_Ecommerce.git
         ```
      2.3. Install Web server on EC2

      - Install Apache web server on linux to host "**MarketPeak_Ecommerce**"

        ```bash
        sudo apt update -y
        sudo apt install httpd -y
        sudo systemctl start apache2
        sudo systemctl enable apache2
        ```
      - This will update linux server, install apache, strts and boot webserver.

      2.4. Configure Httpd for website.
      - This directory /var/www/html/ is created by default once Apache is installed on linux server to host web contents like HTML and CSS files for those visiting this site.

         ```bash
         sudo rm -rf /var/www/html/*
         ```
      - This will clear default httpd web directory

         ```bash
         sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/
         ```
      - Once the default web dierectory is cleared, copy MarketPeak e-commerce files to /var/www/html/
      - Apply changes by reloading httpd
     
        ```bash
         sudo systemctl reload httpd
        ```
      2.5. Access website from browser using IP address
      
      3.0. Continous integration and deployment workflow
      
      **Step1**: Developing new features and fixes

      - Creatig new branch "**development**"
        
        ```bash
        git branch development
        ```
      **Step2**: Version ontrol with Git
      
      
        
      
      
      
      

         
                  
          
         
            
