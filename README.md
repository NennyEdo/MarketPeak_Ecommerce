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
         
            
