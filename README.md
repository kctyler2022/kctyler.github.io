# thewizardofaws.github.io

The Wizard of AWS
Welcome to the repository for The Wizard of AWS! This project is designed to grow my personal brand as an AWS evangelist, featuring a blog, podcast, and more. The website is hosted on AWS as a serverless static website.

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
thewizardofaws.github.io/
│
├── _config.yml
├── index.md
├── about.md
├── projects.md
├── blog.md
├── resources.md
├── podcast.md
├── contact.md
│
├── _posts/
│   ├── 2024-12-12-welcome-to-my-blog.md
│   └── 2024-12-13-aws-certification-tips.md
│
├── _drafts/
│   └── future-post-ideas.md
│
├── assets/
│   ├── css/
│   │   └── main.css
│   ├── images/
│   │   ├── profile-picture.jpg
│   │   └── aws-cert-badges/
│   └── js/
│       └── main.js
│
├── _includes/
│   ├── header.html
│   ├── footer.html
│   ├── social-links.html
│   └── youtube-embed.html
│
├── _layouts/
│   ├── default.html
│   ├── post.html
│   └── page.html
│
└── _data/
    ├── navigation.yml
    └── projects.yml


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

