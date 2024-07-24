# Project Overview
This project is currently under development. Its aim is to create a semi-automatic pipeline for assessing the impact of mutations on protein structures using free tools available on GitHub. The impact description will be generated using GPT. A bioinformatician can monitor each stage of the process and make adjustments or corrections as needed.
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
3.	Satisfaction survey email.<br>
    Satisfaction Survey https://script.google.com/macros/s/AKfycbwVYsaQv1J2pv5DT426ByFoM24giHrlOUgDumQkNrGCQx7WRtM76YMuxwxY_dGhaITL/exec?name=8888<br>
4.  Results:<br>
Delivered as a ZIP file containing a folder with the results and an HTML file with a sidebar menu for easy navigation.<br>
Currently, the folder is empty, and the HTML file contains only the details filled out in the form.<br>
### Tracking and Editing
•	Job Tracking: Track Submitted Jobs https://script.google.com/macros/s/AKfycbzEnoZlq0qPqaukgxtEkzFIBfj_ps-eGgEYHDbh0YPfSiVRf20e7flKpPzAcrfT06wRgQ/exec<br>
![image](https://github.com/user-attachments/assets/5208c262-14a8-4639-93c8-5a2945ce2e6b)

Requires appropriate permissions.<br>
•	Editing Results:<br>
The 'edit' column allows modifications to the HTML file in the results folder.<br>
Use the editor available at: HTML Editor- http://52.21.39.179:8502/ <br>
Results can be resubmitted only after making the necessary changes.<br>
![image](https://github.com/user-attachments/assets/af06e2e5-e2b8-4eb8-b4ec-3f48c3d13b36)

