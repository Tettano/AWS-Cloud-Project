# AWS S3 Bucket Webhost

We are creating AWS static website using S3 Bucket make sure you already have a website on HTML, CSS and JavaScript in this project and AWS free tier account.

![image](https://github.com/user-attachments/assets/9dd42788-1806-4f82-bc1c-103e97828f97)

You'll be using Amazon S3 (which stands for Amazon Simple Storage Service) to host a website.

---

# Step#1 -Create a bucket in Amazon S3

![image](https://github.com/user-attachments/assets/f36d0b6d-8764-470f-a18e-bec777bdc41d)

- On the general purpose buckets click (Create Bucket)
- Create your bucket name 
  * An S3 bucket name is globally unique. After you create a bucket, no other AWS account in the entire world can use your bucket's name (unless you delete the bucket).
    This also means that when you create your bucket, you need to make sure the bucket's name is unique too.

![image](https://github.com/user-attachments/assets/120e4dcd-ffe4-459b-908f-8b8b19224f6a)

- For Object Ownership, choose ACLs enabled.

![image](https://github.com/user-attachments/assets/20905b01-882d-440f-95a0-bcf195d78a4c)

what are ACLs (Access Control Lists)?

An ACL = a set of rules that decides who can get access to a resource.
Enabling ACLs in this S3 setup lets you control who can access and do things with the objects (i.e. website files) you upload into your bucket.
With ACLs, different AWS accounts can own and control different files in your bucket.
- Choose Bucket owner preferred.

---

- For Block Public Access settings for this bucket, clear the check box for Block all public access.
  * This banner is telling us that the bucket and its objects might become public if we untick the checkbox. This is what we want to host a public website.
  * Check the box that says “I acknowledge that the current settings might result in this bucket and the objects within becoming public.”
![image](https://github.com/user-attachments/assets/f48291fb-baf3-4fc7-9785-1ad737e2a064)

- For Bucket Versioning, choose Enable.
- Choose Create bucket.

---

# Step#2 -Upload website content to your bucket

- In the Buckets section, choose the name of your new bucket.
- Download these files to your computer so we can add them into your bucket (right click on each link, and select Save link as...):
  * index.html
![image](https://github.com/user-attachments/assets/6642873f-4c76-4381-930b-0051daae2922)

- Choose Close underneath the green Upload succeeded banner.

![image](https://github.com/user-attachments/assets/225d9659-92ca-4e15-a4b4-397d4ac227bc)

---

# Step#3 -Configure a static website on Amazon S3

  Next up, let's make your website available on the internet by setting up static website hosting.

- Make sure you're back in your bucket's page. If you're not sure, choose General purpose buckets on the left hand side navigation bar, and then choose the bucket you created for this project.
- Choose the Properties tab.
- Scroll all the way down to the Static website hosting panel.
- Choose Edit.

![image](https://github.com/user-attachments/assets/428b7abd-b232-4da1-90b4-28f9c9531657)

![image](https://github.com/user-attachments/assets/0af9f89a-fc86-4dc2-a598-6caeba81fb9d)

- Choose Enable.

![image](https://github.com/user-attachments/assets/9f991845-d85a-4910-9d7b-71efe0fd7c95)

- Also insert the HTML file that you uploaded earlier.

- Choose Save changes.

---

# Step#4 -Make objects in your S3 bucket public
  In this step, we gonna setup our bucket into the public so the html we uploaded will be accessible online.
- Go back to the Bucket Object tab.
![image](https://github.com/user-attachments/assets/f7364a09-96dc-4a41-a1c9-ab330fe6898a)
- Choose *Permission* .

- We're gonna go edit the bucket policy

An AWS Bucket policy is a JSON document that defines the permissions and access controls for an Amazon S3 bucket. It determines who can access the bucket, what actions they can perform (e.g., read, write, delete), and under what conditions.

![image](https://github.com/user-attachments/assets/407d5886-2e55-4aab-94f9-e2bbd9ca3adb)
- Copy the policy code and paste it into your bucket policy.
 * I made the JSON code for our bucket policy Kindly check the uploaded JSON file here.
![image](https://github.com/user-attachments/assets/928b84a6-4708-42e9-8971-535fd7402592)
- Replace the name of bucket resouce with your own resource.

Where can I find my own Bucket ARN Resouce?
- Go back to Bucket Object tab.
![image](https://github.com/user-attachments/assets/9eb3f6d7-335f-4fb3-a6f6-d8fa311161f4)
- Choose *Properties*
Copy your ARN Souce.
![image](https://github.com/user-attachments/assets/2a363634-b135-4eb8-b0ce-e2b6bcd0c425)

- Back to your *Permission* Tab
- Edit your *Bucket Policy*.
- Replace the Source with your ARN Bucket Source

![image](https://github.com/user-attachments/assets/b5d4f0c7-7042-4619-b164-e9521778c4a1)

- And also update the file name that you uploaded earlier, in this it will automatically read
Your HTML with the bucket policy.

![image](https://github.com/user-attachments/assets/05561291-7778-4ca4-a89b-2c5acfd61ba8)

- Save Changes.

---

# Step#5 -Run your Static Website

Go to your *Properties* settings of your bucket tab.
- Scroll all the way down to the Static website hosting panel.

![image](https://github.com/user-attachments/assets/94b3e2a5-cd3a-4f5b-b7f5-a4c0f7b71421)

Go to your direct URL of your website and check, this already accessible for anyone worldwide.






















