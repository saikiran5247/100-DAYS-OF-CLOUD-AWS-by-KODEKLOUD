# DAY 1: Create Key Pair
## TASK
The Nautilus DevOps team is strategizing the migration of a portion of their infrastructure to the AWS cloud. Recognizing the scale of this undertaking, they have opted to approach the migration in incremental steps rather than as a single massive transition. To achieve this, they have segmented large tasks into smaller, more manageable units. This granular approach enables the team to execute the migration in gradual phases, ensuring smoother implementation and minimizing disruption to ongoing operations. By breaking down the migration into smaller tasks, the Nautilus DevOps team can systematically progress through each stage, allowing for better control, risk mitigation, and optimization of resources throughout the migration process.  

For this task, create a key pair with the following requirements:  
•	Name of the **key pair** should be **devops-kp**  
•	Key pair **type** must be **rsa**


Notes:  
•	Create the resources only in us-east-1 region.  

## Theory  
### What is a Key Pair?  
An AWS key pair is a set of cryptographic credentials used to securely authenticate users when connecting to an EC2 instance. It consists of two components:  
•  Public Key - Stored by AWS and associated with the EC2 instance.  
•  Private Key - Downloaded by the user at creation time and used to authenticate access. This file must be kept secure.  
AWS uses asymmetric cryptography, where the public and private keys work together to establish a secure connection.

### Why is a Key Pair Required?  
•  Key pairs are primarily used for secure, password-less authentication to EC2 instances.  
For Linux-based EC2 instances:  
•  SSH access requires a private key (.pem file)  
•  Password-based login is disabled by default for security reasons  
Without a valid key pair, it is not possible to access the instance after launch.  

### Key Pair Types in AWS  
AWS supports multiple key pair types. In this task, the RSA key type was used.  
•  RSA  
  Widely supported and compatible with OpenSSH  
  Commonly used for Linux EC2 instances  

### Key Pair Use Cases  
•  Secure SSH access to EC2 instances  
•  Initial authentication during instance launch  
•  Used by automation tools like Ansible, Terraform, and CI/CD pipelines  
•  Access control in multi-user cloud environments  

### Security Best Practices  
•  Never commit private key files (.pem) to GitHub or any public repository  
•  Store private keys securely with restricted file permissions  
•  Rotate key pairs if a private key is exposed or compromised  

### Outcome of This Task  
By completing this task, I created an RSA-based EC2 key pair in the us-east-1 region, enabling secure access to future EC2 instances as part of the AWS migration process.  

## Steps Performed:  
1. Click on the CONSOLE URL and enter the AWS credentials and sign in. This will open up the AWS console. Ensure we are in us-east-1 region.  
2. Search for Key Pairs in the search tab and click on Key pairs(EC2 feature). Key pairs section will open up now.  
3. Click on create key pair and enter  
name: devops-kp  
Key pair type: RSA  
Private key file format: .pem (For use with OpenSSH)
4. Click on Create key pair. Now we have successfully created the key pair.
5. Check if the keypair is successfully created from aws-client host in kodekloud by entering: **aws ec2 describe-key-pairs**. This command confirms that the devops-kp key pair exists in the us-east-1 region.

<img width="941" height="292" alt="image" src="https://github.com/user-attachments/assets/40506d85-7599-46ad-bc86-d97f16e771d8" />  

6. Click on **Check** and close the task.
