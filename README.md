# kctyler.github.io

AWS Architect Adventures
Welcome to the repository for AWS Architect Adventures! This project is designed to grow my personal brand as an AWS evangelist, featuring a blog, podcast, and more. The website is hosted on AWS as a serverless static website.

Table of Contents
Project Overview
Tech Stack
Folder Structure
Getting Started
Deployment
Contributing
License
Project Overview
AWS Architect Adventures is a personal website that includes:

Home Page: An overview of the latest blog posts and podcast episodes.
Podcast Page: A list of podcast episodes with descriptions and links.
Blog Page: A collection of blog posts with summaries and links.
AWS Utah Page: Information about the AWS Utah user group.
Resume Page: My professional resume and career highlights.
The website is designed to be fully serverless, leveraging various AWS services for hosting, content delivery, and more.

Tech Stack
Frontend: HTML, CSS, JavaScript
Backend: AWS Lambda (for content processing)
Hosting: Amazon S3, Amazon CloudFront
CI/CD: AWS Amplify, AWS CodePipeline, AWS CodeBuild
Others: AWS Route 53 (DNS), AWS Certificate Manager (SSL/TLS)
Folder Structure
awsarchitectadventures/ │ ├── src/ │ ├── assets/ │ │ ├── images/ │ │ ├── css/ │ │ │ └── styles.css │ │ ├── js/ │ │ │ └── scripts.js │ │ └── fonts/ │ ├── content/ │ │ ├── blog/ │ │ ├── podcast/ │ │ └── aws-utah/ │ ├── templates/ │ │ ├── partials/ │ │ │ ├── header.html │ │ │ ├── footer.html │ │ │ └── nav.html │ │ ├── index.html │ │ ├── blog.html │ │ ├── podcast.html │ │ ├── aws-utah.html │ │ └── resume.html │ └── scripts/ │ └── markdown_to_html.py │ ├── build/ │ ├── assets/ │ │ ├── images/ │ │ ├── css/ │ │ │ └── styles.css │ │ ├── js/ │ │ │ └── scripts.js │ │ └── fonts/ │ ├── blog/ │ │ └── index.html │ ├── podcast/ │ │ └── index.html │ ├── aws-utah/ │ │ └── index.html │ ├── index.html │ ├── blog.html │ ├── podcast.html │ ├── aws-utah.html │ └── resume.html │ ├── amplify/ │ ├── .config/ │ ├── backend/ │ ├── team-provider-info.json │ ├── .gitignore ├── amplify.yml ├── package.json ├── README.md

Getting Started
Prerequisites
Node.js and npm installed
AWS CLI installed and configured
Amplify CLI installed and configured
Installation
Clone the repository:

git clone https://github.com/your-username/awsarchitectadventures.git
cd awsarchitectadventures
Install dependencies:

npm install
Initialize Amplify:

amplify init
Add hosting:

amplify add hosting
amplify publish
Deployment
Build Process
Build the project:

Use a build tool to process the source files in src/ and output the final files into the build/ directory.

Example using a custom script:

npm run build
Deploy to S3:

Use the AWS CLI to sync the contents of the build/ directory to the S3 bucket.

aws s3 sync build/ s3://awsarchitectadventures.com/ --delete
Invalidate CloudFront Cache:

Invalidate the CloudFront cache to ensure the latest changes are reflected.

aws cloudfront create-invalidation --distribution-id YOUR_DISTRIBUTION_ID --paths "/*"
Contributing
Contributions are welcome! Please read the CONTRIBUTING.md file for details on how to contribute.

