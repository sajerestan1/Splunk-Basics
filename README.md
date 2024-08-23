# Splunk-Basics


## Project Report: Splunk Room Review and Data Analysis

![image](https://github.com/user-attachments/assets/13d53ca2-4a86-4e81-a4a1-c110f4e97bc2)

### 1. Overview

This project is a revisit of the Splunk rooms in the SOC Level 1 learning path on TryHackMe (THM). The goal was to reinforce my understanding of Splunk components, data ingestion, and querying by completing a series of tasks and documenting my approach, including any mistakes made during the process. This exercise serves as both a review and a learning opportunity to deepen my skills in using Splunk for security operations.

### 2. Task 3: Splunk Components

#### 2.1 Which component is used to collect and send data over the Splunk instance?

In this task, I identified the component responsible for collecting and sending data across the Splunk instance. The answer was found in the reading material provided in the room.

    Answer: Forwarder

### 3. Task 4: Navigating Splunk
#### 3.1 In the Add Data tab, which option is used to collect data from files and ports?

For this task, I connected my own virtual machine (VM) to the THM network instead of using the provided Attack Box. After establishing the connection, I navigated to the Add Data tab in Splunk. The required option was found at the bottom of the page.

![image](https://github.com/user-attachments/assets/1e5f23ca-0827-47eb-8a70-33af3fab20a4)

![image](https://github.com/user-attachments/assets/a2842c8f-1ed4-482c-89b6-f59bf645e5aa)


    Answer: Monitor

### 4. Task 5: Adding Data
#### 4.1 Upload the data attached to this task and create an index “VPN_Logs.” How many events are present in the log file?

To complete this task, I first downloaded the log file from my host machine and transferred it to my VM using file.io. Afterward, I uploaded the data to Splunk and created an index named “VPN_Logs.” I then searched the index to find the total number of events present in the log file.

![image](https://github.com/user-attachments/assets/98430243-d97b-4388-91a6-e3922758bcb7)


![image](https://github.com/user-attachments/assets/1ef5332b-4fe8-4985-8ad0-e1e2b2ca4d92)

![image](https://github.com/user-attachments/assets/7cc35d8f-0d46-4fbe-8ad2-2229b95917bd)

![image](https://github.com/user-attachments/assets/b54f9366-e17e-40b7-8062-20e6fda44463)


    Answer: 2862

### 4.2 How many log events by the user Maleena are captured?

In this step, I filtered the logs by the UserName field to identify how many events were associated with the user “Maleena.” This was done by typing index=vpn_logs UserName=”Maleena” in the search bar.

![image](https://github.com/user-attachments/assets/e501b70c-f344-4456-8748-04abfc10b998)

![image](https://github.com/user-attachments/assets/2c9c0c8f-d323-43a8-8d4a-70b956fef13b)


    Answer: 60

### 4.3 What is the name associated with IP 107.14.182.38?

I filtered the logs by the Source_ip field to find the name associated with the specified IP address. Adjusting the filter allowed me to identify the correct user.

   ![image](https://github.com/user-attachments/assets/9d93e2cc-f0ae-40ed-8183-2fa2f7c5f5cc)

   ![image](https://github.com/user-attachments/assets/4526d8ef-7a40-42c7-b926-414dd3ee3bfc)


    
    Answer: Smith

### 4.4 What is the number of events that originated from all countries except France?

To answer this question, I filtered the logs by the Source_Country field and excluded events originating from France. This was accomplished by using a boolean expression in the search query.

![image](https://github.com/user-attachments/assets/b2dfb7a8-e9c1-43ed-ad2f-490dad12fda7)

    Answer: 2814

### 4.5 How many VPN Events were observed by the IP 107.3.206.58?

Similar to the previous question, I used the Source_ip field to search for events associated with the specified IP address.

![image](https://github.com/user-attachments/assets/caeb2d95-0715-439d-8948-ae626be16a96)


    Answer: 14

### 5. Thoughts

While this exercise served as a valuable review, I found it to be relatively basic given my current level of knowledge. This room was an introductory exercise, so it’s understandable that the tasks were simpler. However, the review process helped reinforce my understanding of Splunk components and data querying. I look forward to tackling more advanced Splunk rooms to further enhance my querying skills. Moving forward, I plan to revisit other rooms, including those focused on phishing and Wireshark, to complete my SOC Level 1 path.
6. Conclusion

This project allowed me to solidify my foundational knowledge of Splunk by revisiting core components, navigating the interface, and performing data analysis. The hands-on experience of uploading and querying data provided valuable insights into how Splunk is used in a security operations context. As I continue to progress through the SOC Level 1 learning path, I aim to build on this knowledge and apply it to more complex scenarios in future exercises.

