# DAY 1: Create Key Pair
## TASK
The Nautilus DevOps team is strategizing the migration of a portion of their infrastructure to the AWS cloud. Recognizing the scale of this undertaking, they have opted to approach the migration in incremental steps rather than as a single massive transition. To achieve this, they have segmented large tasks into smaller, more manageable units. This granular approach enables the team to execute the migration in gradual phases, ensuring smoother implementation and minimizing disruption to ongoing operations. By breaking down the migration into smaller tasks, the Nautilus DevOps team can systematically progress through each stage, allowing for better control, risk mitigation, and optimization of resources throughout the migration process.  

For this task, create a key pair with the following requirements:  
•	Name of the **key pair** should be **devops-kp**  
•	Key pair **type** must be **rsa**

Use below given **AWS Credentials**:  
(You can run the **showcreds** command on **aws-client** host to retrieve these credentials)  
Console URL	https://420483306794.signin.aws.amazon.com/console?region=us-east-1  
Username:	kk_labs_user_654078  
Password:	y5gqF1i^xheC  
Start Time:	Fri Dec 26 03:05:15 UTC 2025  
End Time:	Fri Dec 26 04:05:15 UTC 2025  

Notes:  
•	Create the resources only in us-east-1 region.  
•	To display or hide the terminal of the AWS client machine, you can use the expand toggle button as shown below:  
<img width="868" height="226" alt="image" src="https://github.com/user-attachments/assets/f4d3ec30-a91d-4399-bd71-c40c0c209088" />  

## STEPS:  
1. Click on the CONSOLE URL and enter the AWS credentials and sign in. This will open up the AWS console. Ensure we are in us-east-1 region.  
2. Search for Key Pairs in the search tab and click on Key pairs(EC2 feature). Key pairs section will open up now.  
3. Click on create key pair and enter  
name: devops-kp  
Key pair type: RSA  
Private key file format: .pem (For use with OpenSSH)
4. Click on Create key pair. Now we have successfully created the key pair.
5. Check if the keypair is successfully created from aws-client host in kodekloud

<img width="941" height="292" alt="image" src="https://github.com/user-attachments/assets/40506d85-7599-46ad-bc86-d97f16e771d8" />  

6. Click on **Check** and close the task.
