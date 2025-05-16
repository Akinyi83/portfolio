#  DevOps CI/CD Pipeline for Node.js Web App with AWS CodePipeline

This project applies a full DevOps CI/CD pipeline setup using **AWS CodePipeline**, **CodeCommit**, **GitHub**, **Elastic Beanstalk**, and **Amazon ECR** to deploy a sample Node.js web application.
It demonstrates
Building and deploying Dockerized applications using Elastic Beanstalk.

Triggering deployments using AWS CodePipeline with GitHub and CodeCommit.

Automating infrastructure permissions using Python and Boto3.

##  Project Structure

├── Dockerrun.aws.json # Docker image deployment definition for Elastic Beanstalk
├── front_end_website/
│ ├── README.md # Placeholder README
│ └── test.html # Sample HTML for frontend showcase
├── python_3/
│ └── permissions.py # Script to apply an S3 bucket policy


##  Technologies Used

- **AWS CodePipeline** – Orchestrates the CI/CD process
- **AWS CodeCommit & GitHub** – Source control
- **Amazon ECR** – Hosts the Docker image for the Node.js app
- **Elastic Beanstalk** – Deploys and manages the app environment
- **Amazon S3** – Used for storing security policy (referenced in permissions script)
- **Python & Boto3** – For automating S3 bucket permissions

##  Sample Frontend Page

The `test.html` file includes a simple webpage used during an interview technical demo with Melita Ltd:

```html
<h1>This is a sample HTML page for my DevOps Interview with Melita Ltd, one of the best Telecommunication Companies.</h1>

bucket_name = "<FMI>"  # Replace with your actual bucket name

##Dockerrun.aws.json (Elastic Beanstalk)
{
  "AWSEBDockerrunVersion": "1",
  "Image": {
    "Name": "*****.dkr.ecr.us-east-1.amazonaws.com/cafe/node-web-app",
    "Update": "true"
  },
  "Ports": [
    { "ContainerPort": 3000 }
  ]
}
