# Automated investigation of genetic mutations on protein structure and automatic generation of explanatory text and images
# Project Overview
This project is currently under development. Its aim is to create a automatic pipeline for assessing the impact of mutations on protein structures using free tools available on GitHub. <br>

Automated Investigation: Utilizing a pipeline of existing bioinformatics tools available on GitHub. <br>
Automatic Text Generation: Using GPT-API <br>
Automatic Image Generation: Using MOL* (https://molstar.org/) or Jsmol <br>

Additionally, making adaptations to enable ranking of results obtained from next-generation sequencing technologies, focusing solely on mutations in protein-coding regions. The ranking will also be performed by GPT.<br>

A bioinformatician will be able to monitor each stage of the process and will make adjustments or corrections as needed.<br>

### Website and Forms
•	Website: GetReprot https://www.getreprot.com/ <br>
Built using Google Sites.<br>
•	Multi-Step Form: GetReprot Form https://www.getreprot.com/getreprot <br>
Created using Google Forms and designed with HTML, CSS, and JavaScript.<br>
Integrated with the Payable add-on to enable payments via PayPal, with automatic fee calculation at each form step.<br>
•	Contact Form: Contact Us https://www.getreprot.com/contact-us<br>
Created similarly to the multi-step form but without the payment add-on.<br>
### Pipeline and Cloud Infrastructure
•	Cloud Platform: AWS <br>
Computation is handled by EC2 instances, and the results are stored in S3 buckets.<br>
A cron job on EC2 checks the Google Sheets file linked to the Google Form every X hours. If a new entry is found, the EC2 instance with the pipeline is started.<br>
•	Currently, the check is performed on a Google Sheet connected to a form created in Streamlit: Streamlit Form. https://app.getreprot.com/ <br>
### Email Notifications and Result Delivery
•	Email Sequence:<br>
1.	Confirmation email after form submission.<br>
2.	Email with results.<br>
    The results delivered as a ZIP file containing a folder with the results and an HTML file with a sidebar menu for easy navigation.<br>
   Currently, the folder that is delivered after form submission is empty, and the HTML file contains only the details filled out in the form. However,The HTML file should look like this:<br>
    ![image](https://github.com/user-attachments/assets/05680d27-23ea-4c7e-84c4-602f6f6a9479)
  	![image](https://github.com/user-attachments/assets/deb8946e-375a-49b9-baab-66640f5e4330)


4.	Satisfaction survey email.<br>
    Satisfaction Survey https://script.google.com/macros/s/AKfycbwVYsaQv1J2pv5DT426ByFoM24giHrlOUgDumQkNrGCQx7WRtM76YMuxwxY_dGhaITL/exec?name=8888<br>
    Createted using Google App Scripts. <br>

### Tracking and Editing
•	Job Tracking: Track Submitted Jobs https://script.google.com/macros/s/AKfycbzEnoZlq0qPqaukgxtEkzFIBfj_ps-eGgEYHDbh0YPfSiVRf20e7flKpPzAcrfT06wRgQ/exec<br>
    Requires appropriate permissions.<br>
    ![image](https://github.com/user-attachments/assets/5208c262-14a8-4639-93c8-5a2945ce2e6b)
    Createted using Google App Scripts. <br>

•	Editing Results:<br>
The 'edit' column allows modifications to the HTML file in the results folder.<br>
Use the editor available at: HTML Editor- http://52.21.39.179:8502/ <br>
Results can be resubmitted only after making the necessary changes.<br>
![image](https://github.com/user-attachments/assets/af06e2e5-e2b8-4eb8-b4ec-3f48c3d13b36)

