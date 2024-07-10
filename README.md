# AWS-Llama-ChatBot

## Description
This project is a solo endeavor to develop a Llama-powered chat bot where the model is hosted on a private server to ensure the security of all user prompts. The project leverages various AWS services and modern technologies to create a secure, scalable, and efficient cloud-based application.
## What is AWS and Cloud Computing?

Amazon Web Services (AWS) is a comprehensive and widely adopted cloud platform offering over 200 fully-featured services from data centers globally. Cloud computing, in general, provides on-demand delivery of IT resources via the internet with pay-as-you-go pricing.

[AWS Console](https://aws.amazon.com/free/?gclid=Cj0KCQjwv7O0BhDwARIsAC0sjWP4e1vIF3IO7_L68FxUuy6DJ1qtGi1KusgFEt6o5Zy2q0ConJ7LWa4aAmxkEALw_wcB&trk=fce796e8-4ceb-48e0-9767-89f7873fac3d&sc_channel=ps&ef_id=Cj0KCQjwv7O0BhDwARIsAC0sjWP4e1vIF3IO7_L68FxUuy6DJ1qtGi1KusgFEt6o5Zy2q0ConJ7LWa4aAmxkEALw_wcB:G:s&s_kwcid=AL!4422!3!432339156150!e!!g!!aws!1644045032!68366401852&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)


### Benefits of Cloud Computing in the Tech Industry:
- **Scalability**: Easily scale resources up or down based on demand.
- **Cost Efficiency**: Pay only for the resources you use.
- **Flexibility**: Access a wide range of services and tools to innovate faster.
- **Global Reach**: Deploy applications in multiple regions worldwide.
- **Security**: Benefit from a data center and network architecture built to meet the requirements of the most security-sensitive organizations.

## Technologies and Services Used
This project utilizes the following technologies and AWS services:

- AWS EC2: Virtual servers to host the Flask-API and Streamlit app.
- AWS RDS: Managed relational database service (MySQL) to store user information and prompts.
- AWS S3: Scalable storage service for images and icons.
- AWS Bedrock: Hosting the chat bot model.
- Flask-API: Framework for building REST APIs.
- Gunicorn: WSGI HTTP server for running the Flask application.
- Streamlit: Framework for building interactive web applications.

## Service and Technology Breakdown
- AWS EC2: Provides resizable compute capacity in the cloud. Two instances are used; one runs the Flask-API on Gunicorn, and the other hosts the Streamlit app.
- AWS RDS: Manages MySQL databases, ensuring high availability, security, and automated backups.
- AWS S3: Offers object storage with a simple web service interface to store and retrieve any amount of data.
- AWS Bedrock: Securely hosts the chat bot model, ensuring user prompts remain private.
- Flask-API: A lightweight framework to create RESTful APIs in Python.
- Gunicorn: A Python WSGI HTTP Server for UNIX to serve the Flask application.
- Streamlit: An open-source app framework to create custom web apps for machine learning and data science.

## Communication Between Services at Runtime
- User Interaction: Users interact with the chat bot via the Streamlit app hosted on one EC2 instance.
- API Requests: The Streamlit app sends API requests to the Flask-API hosted on the second EC2 instance.
- Data Storage: User information and prompts are stored and retrieved from AWS RDS.
- Media Storage: Images and icons are stored and retrieved from AWS S3.
- Model Hosting: The chat bot model hosted on AWS Bedrock processes user prompts and returns responses securely.
