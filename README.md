# Securing-Cloud-Applications

## Objective

This project aims to use Microsoft Azure to host my own cyber blog web application, and to protect it with a SSL certificate and Azure's security features. 


### Skills Learned

-A better understanding of cloud networking fundamentals
-Developed and designed a cyber-blog web application using Azure’s Cloud services and Docker
-Created and stored SSL certificates in Azure’s Key Vault, and bound them to secure the web application.
-Protected the web application by utilizing Azure’s Security features, such as the Azure WAF, and Security Center.


### Tools Used

-Azure: {Keyvaults, App Services, WAF}
-GoDaddy domain managment
-PHP 8.2 (backend)
-HTML/CSS (frontend) 
-Docker
-OpenSSL


## Steps
Web Application Homepage
<img width="551" alt="project 1- domain" src="https://github.com/user-attachments/assets/825ceda2-46d7-47ef-a100-c46168df2d5a" />
Blogpost
<img width="552" alt="Project 1- blogpost1" src="https://github.com/user-attachments/assets/8219605d-ca0e-4729-adb7-a306abc25124" />


### 1. Create a Wep Application on Azure 
- Navigate to [Azure Portal](https://portal.azure.com)
- Go to **App Services** → Click **+ Add**
- Choose your subscription, resource group, and region
- Select **Runtime Stack**: PHP 8.2
- Create a new App Service Plan or use an existing one
- Deploy the web app

### 2. Connect a Custom Domain
- Purchase or use existing domain ( I used GoDaddy)
- In Azure → App Services → Custom Domains
- Add your domain name (e.g., `caseycyber.blog`)
- Verify domain ownership via DNS records (CNAME or TXT)

### 3. Deploy Web Files
- Customize these elements of the webpage: name, LinkedIn profile link, introductions, and picture
- To customize you first need to SSH into the right container

### 4. Secure the Web App with SSL/TLS
- Enable HTTPS in Azure App Settings
- In Azure: create a key vault and self-signed certificate
- Certificates must be created in PFX format, remember to encrypt the certifiacte
- Test certificate validity in browser

### 5. Enable Azure Web Application Firewall (WAF)
- Create a WAF Policy
- Enable OWASP rule sets (e.g., SQL Injection, XSS, Directory Traversal)
- Assign WAF policy to your App Gateway or Front Door

Custom Rules
<img width="553" alt="Project 1- custom rules" src="https://github.com/user-attachments/assets/e22197ec-f21e-4dee-9791-28b10908443f" />


### 6. Configure Custom WAF Rules
- Create a rule to block traffic (e.g., from specific regions or IPs)
- In this project I customized the rules to only accept traffic from locations where the business parters reside: the US, Canada, and Australia
  

### 7. Analyze Azure Security Center Recommendations
- Go to **Microsoft Defender for Cloud**
- Review and remediate high-priority recommendations:
  - Enable MFA
  - Restrict public access
  - Enable encryption and monitoring

### Clean Up Resources
- Delete unused Azure resources to avoid charges

### Reflection
I truly enjoyed this project - it marked the beginning of my interest in cloud security. It was fascinating to see how the front end and back end of a web application work together, especially when it comes to implementing security features. THis experience sparked my curiosity and gave me a strong foundation to build on as I continue to learn and growing in cybersecurity. 


