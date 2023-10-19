---
title : 'Customer Onboarding'
date : 2023-10-06T15:28:27+05:30
draft : false
---






## Customer Onboarding

Customer onboarding is a fundamental process for integrating new customers into your organization and ensuring a smooth and positive experience with your products and services. It plays a crucial role in establishing enduring relationships with your customers. This documentation outlines the steps and key considerations in the customer onboarding process.
 
We categorize users into two types: internal users and external users. Internal users possess the capabilities to manage customer bookings and access various applications owned by Maersk. External users, on the other hand, are individuals or entities seeking to do business with us on behalf of their companies. The process we employ for external users is referred to as "basic soft user" registration. Basic soft users have limited access rights, primarily enabling them to request upgrades, change their passwords, and perform other basic functions.
 
To expand their access and capabilities, soft users must embark on an "upgradation journey." The customer onboarding process involves three key steps: creating a customer, establishing a contact, and ultimately upgrading the user. It's important to note that the Customer Master Data (CMD) serves as the primary source of truth, owning and managing customer and contact data.
It has it’s benefits like product adaptation , Account setup , Support and communication, Cross selling and upselling etc.

Some benefits are:-

Enhanced Customer Experience: A well-designed onboarding process ensures that new customers have a positive and seamless experience when interacting with a business. It sets the tone for a long-lasting relationship and fosters a sense of trust and confidence.

Reduced Churn: Effective onboarding can reduce customer churn, as it helps customers understand the value and benefits of a product or service. When customers see the value early on, they are more likely to stay engaged and continue using the offering.

Increased Customer Loyalty: Onboarding can foster customer loyalty by demonstrating a commitment to meeting the customer's needs and expectations. Satisfied customers are more likely to become repeat customers and brand advocates.

Compliance and Security: In some industries, onboarding is critical for compliance and security reasons. It ensures that customers meet necessary regulatory requirements and understand security protocols.

Competitive Advantage: A smooth onboarding process can set a business apart from competitors. It demonstrates a commitment to customer success and can be a key differentiator.

<b>Customer Onboarding Flow</b>:-

![Alt Image](CustomerOn.png)

Three distinct upgradation journeys are available to grant users full access to our systems. Soft users must undergo one of these journeys to become upgraded users:
 
1. Auto Upgrade (Based on Exact Email): This process syncs customer data from CMD to our systems Postgres and IDM when a new customer is created. If the email matches an existing contact, the user is provided with different customers the user contact is associated with. After Customer matching and selection the user is upgraded within 10 minutes.
 
2. Schedule Upgrade (Based on Email Domain): If the exact email isn't found, we consider the email domain of the user and provide a list of relevant customers to choose from. The user can select one and proceed with a scheduled upgrade, which typically takes 30 minutes.
 
3. Manual Upgrade: In cases where soft users don't find relevant customers in the schedule upgrade list, they can create a customer manually by  entering the required fields . The LiveHelp team manages this process, contacting the user for additional details and documents to verify their relationship with the customer. If all requirements are met, the LiveHelp team creates a customer, establishes a contact, and upgrades the user within 48 hours.




1. Initiate the proces by registering on Maersk.

![Alt text](image-1.png)

2. Verify the email. 

![Alt text](image-2.png)
<br>
<b>Transportation services</b>:-

User is a soft user and has already completed the email verification and now desires to go through transportation services will to go through one of the workflows .

Listed below are some of the workflows:

It supports 3 kinds of workflows:-

1. Auto Upgrade Flow
1. Schedule Upgrade flow
1. Manual Upgrade Flows

### Auto Upgrade Flow:-

In this workflow a user when a soft user has already goes through email and domain matching .

<b>Flow</b>:

![Alt text](AutoUp.png)
1. After searching and identification of matched contact with active status the soft user is displayed the customers it has links to. <br><br>
The user will be reach this page:-
![Alt text](autoBVD.png)
2. Upon customer selection the user lands at confirm customer details page . After submit request the user is assigned upto 10 min within which his request will be approved by the LiveHelp team in cmd.

![alt image](AutoUPConfirm.png)



### Scheduled Upgrade 

When contact retreival results as a failure we trigger a different workflow where the Soft user is displayed the customer based on the email domain of the user. The BVD search finds the customer that are linked with contacts that have similar domain as the user and prompts the user either to choose a customer or create a customer using a manual flow .<br><br>
![alt Text](ScheduledUpgrade.png)
<br><br>

<b>Flow</b>:
<br>
<br>

![alt Text](ScheduleUp.png)

#### Customer Selction 

<b>BVD Search (Found the Customer)</b>

After selecting a csutomer among the bvd search results the user is asked to verify the company address selected and fill the country and office region where the customer is located.

<br><br>

![alt Text](scheduleCustomerPage.png)
<br><br>

Upon clicking submit button the user triggers a contact api wrokflow  which creates a contact in our idm and upon approval updates the upgrade status of the  user to <b>S_UPGRADE</b>
<br><br>

![alt Text](ScheduleConfirmation.png)


## Manual Upgrade

When a user is not satisfied with the sarch results for customers , The user can manually search a customer using trading name and company .A customer search takes place where matching customer are shown to the user.
<br><br>

![Alt Text](manualUpTradingname.png)

<br><br>
Going forward with the search and selecting the customers within the BVD search results triggers a KYC workflow.
<br>

### Customer creation flow

Know Your Customer (KYC) is an essential process employed by us to validate our customers worldwide to mitigate risks associated with fraud and other financial crimes. KYC enables organizations to verify the identities of their customers, assess their suitability, understand their financial status and validate if they can do business with us. By conducting thorough KYC checks, we establish trust, ensure compliance with regulatory requirements, and protect ourselves from potential legal and reputational risks.
<b>Flow</b>:
<br>
<br>

![Alt image](ManualUPP.png)
<br>
<br>
### The Process

The KYC process at Maersk typically involves gathering and verifying customer information through various means, such as identity documents, proof of address, and financial statements. Initially, customers are required to provide personal details, including their full name, nationality, business contact information. This verifies their identity. 


1. Search for your company. This uses public domain API's to search for your company

![Alt text](image-4.png)

2. Validate ownership by provide additional details about your company. These will include a valid URL, taxid, and the email domain. Getting these details right will accelerate the KYC checks and grant access to the customers data faster

![Alt text](image-5.png)

3. The Customer details and shipping information are taken into consideration.This new feature introduces Maersk GO.

![Alt text](MaerskGOShippingpage.png)

4. Our KYC requirements can include additional documents based on the country the company is registered to. This is a new feature 

![Alt text](image-6.png)


 For non Europe customers the document verification should be done via ereg mail.
<br>

![Alt text](maerskUpgradePage.png)
They would then need to provide documents about the company to verify the validity of the company they operate with. This is the KYB process. 

5. The next step involves verifying the authenticity of these details by cross-checking them with reliable and official sources. Currently this is done through manual background checks, and verifying identification documents by manual inspection. 

![Alt text](image-7.png)

We believe that automating this through techniques like Optical Character Recognition (OCR) and machine learning will accelerate the onboarding journey and provide better ways of creating a risk profile for the user and customer and ensure ensuring that the customer's risk profile aligns with the organization's risk tolerance. 


The KYC process is an ongoing effort, with regular monitoring of customer activities to detect any suspicious transactions or changes in risk profiles.

## Onboarding Process for Small and Medium Business Customers

For onboarding small and medium business customers we use Maersk Go. Maersk Go is for small and medium businesses looking for simple and reliable global transportation solutions.

### The Process

https://github.com/Maersk-Global/ciam-tech-demo/assets/139266975/698973b7-3909-463f-b282-310999d858b7


## Challenges

Implementing KYC processes across the globe presents several challenges due to varying regulatory frameworks, cultural differences, and technological disparities. Different jurisdictions have their own unique KYC requirements, which can lead to complexities for multinational companies operating in multiple regions. Language barriers, diverse documentation standards, and inconsistent data formats further complicate the KYC process. Additionally, technology plays a critical role in KYC, but access to reliable internet connectivity and digital infrastructure varies across countries. Ensuring data privacy and security while sharing customer information across borders is also a challenge. We must navigate these challenges by developing scalable and adaptable KYC frameworks, utilizing advanced technologies like artificial intelligence and machine learning, and fostering collaboration with regulatory bodies and local partners to ensure compliance and efficiency in global KYC operations.
