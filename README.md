# AWS GitHub CodePipeline S3

This repository provides a comprehensive guide on setting up an AWS CodePipeline to automate the deployment of a static website hosted on Amazon S3. 

## Acknowledgment
Thank you to **Tiny Technical Tutorials** for the inspiration and guidance in creating this tutorial.

## Flowchart
![WhatsApp Image 2024-11-25 at 16 55 23_32d6f75a](https://github.com/user-attachments/assets/56394fa7-ec27-4815-9348-cf4d268bd6fc)
![WhatsApp Image 2024-11-25 at 16 57 22_418793e3](https://github.com/user-attachments/assets/449f30de-29c9-4a4a-bc07-1ebd6cf39369)

## Step 1: Forking the GitHub Repository
1. Fork the repository from the following URL:  
   [https://github.com/tinytechnicaltutorials/codepipeline-s3-game](https://github.com/tinytechnicaltutorials/codepipeline-s3-game)

![WhatsApp Image 2024-11-25 at 16 55 23_c1b31773](https://github.com/user-attachments/assets/971a0e5f-7039-44ff-a7e0-dd0c9ad454e2)

## Step 2: S3 Setup
1. **Creating a Bucket:**
   - Go to the S3 service in the AWS Management Console and create a new bucket.
   
2. **Disable Block All Public Access:**
   - Uncheck the "Block all public access" option to allow public access to your static website.

3. **Enable Static Web Hosting:**
   - In the bucket properties, enable static website hosting.

4. **Set Default Page:**
   - Set the default page to `index.html`.

5. **Add Bucket Policy:**
   - In the permissions tab, add the bucket policy code provided in the repository.

6. **Change Bucket ARN:**
   - Make sure to change the bucket ARN in the provided policy if necessary.

![WhatsApp Image 2024-11-25 at 16 55 24_377200a9](https://github.com/user-attachments/assets/5eff844f-defa-4454-b3d4-2bc342644a90)


## Step 3: Setting Up CodePipeline
1. **Navigate to CodePipeline:**
   - Open the CodePipeline service in the AWS Management Console.

2. **Create Pipeline:**
   - Click on "Create pipeline."
  
![WhatsApp Image 2024-11-25 at 16 55 23_4d49a1f3](https://github.com/user-attachments/assets/7711e4f5-b8c9-4efd-93f7-aa033103712a)

3. **Add Source Provider:**
   - Select GitHub as the source provider.

4. **Connect to GitHub:**
   - Authorize CodePipeline to access your GitHub account.

5. **Select Repositories:**
   - Choose the repository you forked in Step 1.

6. **Click on Repository Name:**
   - Select the branch you want to use for deployment.

7. **Deploy Provider - S3:**
   - Choose S3 as the deploy provider.

8. **Review Everything and Create:**
   - Review your settings and create the pipeline.

## Conclusion
Once the setup is complete, any changes you make to the code in your GitHub repository and commit will trigger the pipeline, automatically updating your static website hosted on S3.
