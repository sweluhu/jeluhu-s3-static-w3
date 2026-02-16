# Personal Website (junioreluhu.com)

Source code for the personal static website **junioreluhu.com**, hosted on AWS S3.

## Overview

This project is a static website serving as a personal portfolio and gallery. It's built with vanilla HTML, CSS, and JavaScript, and leverages various AWS services for hosting, content delivery, security, and authentication. The site features a dynamic "E-Mobility" section that showcases various electric vehicles through a responsive image mosaic and video gallery.

## Live Site

You can visit the live site at: [https://www.junioreluhu.com/](https://www.junioreluhu.com/)

## Features

- **Dynamic S3 Integration**: For public galleries, JavaScript fetches and parses XML listings from a public S3 bucket to dynamically populate image and video galleries.
- **Responsive Mosaic Grid**: A custom CSS Grid implementation that arranges images based on their aspect ratio (landscape vs. portrait) to create a visually appealing and responsive layout.
- **Custom Lightbox**: A lightweight, vanilla JavaScript lightbox for viewing images and videos, with features like:
  - Previous/Next navigation.
  - Keyboard support (Arrow keys for navigation, Escape to close).
  - Touch-friendly controls for mobile devices.
- **Secure User Authentication**: Leverages [Amazon Cognito](https://aws.amazon.com/cognito/) User Pools for user sign-up/sign-in, and Identity Pools to provide temporary AWS credentials for both authenticated and unauthenticated users.
- **Video Gallery**: Includes video thumbnails that autoplay on hover for a more interactive experience.
- **Neon Theme**: A distinct dark mode aesthetic with neon green accents and a minimalist "Made in..." footer for a modern look and feel.

## Pages

- **Home**: Landing page.
- **E-Mobility**: The main gallery page featuring vehicles like:
  - 2017 BMW i3 Rex Terra
  - 2020 Onyx RCR
  - 2021 Cowboy C4
  - 2024 BMW CE-04
  - 2024 Cake Makka
  - 2025 Tesla Model Y
- **NFT**: An NFT Gallery.
- **Fam Bam**: A family photo gallery.
- **Random**: Random image generator.
- **Resume**: Professional resume.

## Tech Stack & Infrastructure

This project leverages the following technologies and services:

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Hosting & Content Delivery**:
  - [AWS S3](https://aws.amazon.com/s3/) for static website hosting and media assets.
  - [Amazon CloudFront](https://aws.amazon.com/cloudfront/) for global content delivery and HTTPS.
- **Authentication & Authorization**:
  - [Amazon Cognito](https://aws.amazon.com/cognito/) (User Pools and Identity Pools) for user authentication and providing credentials for unauthenticated access.
  - [AWS Identity and Access Management (IAM)](https://aws.amazon.com/iam/) for managing access to AWS services and resources.
- **Security & Encryption**:
  - [AWS Certificate Manager (ACM)](https://aws.amazon.com/certificate-manager/) for provisioning and managing SSL/TLS certificates.
  - [AWS Key Management Service (KMS)](https://aws.amazon.com/kms/) for encrypting data at rest in S3.
- **Serverless Compute**:
  - [AWS Lambda](https://aws.amazon.com/lambda/) (Python 3) for backend processing tasks.
- **Infrastructure as Code**:
  - The AWS infrastructure is defined and managed using [Terraform](https://www.terraform.io/).

## Local Development

To run this project locally:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/jeluhu/jeluhu-s3-static-w3.git
    cd jeluhu-s3-static-w3
    ```

2.  **Serve the files:**
    You can use any simple local web server. If you have Python installed, you can run one of the following commands from the project root:

    *For Python 3:*
    ```bash
    python -m http.server 8000
    ```

    *For Python 2:*
    ```bash
    python -m SimpleHTTPServer 8000
    ```

3.  **View the site:**
    Open your web browser and navigate to `http://localhost:8000`.

## Deployment

The website is deployed to an AWS S3 bucket and served globally via Amazon CloudFront. The deployment process involves:

1.  Provisioning the necessary AWS resources (S3 bucket, CloudFront distribution, ACM certificate, IAM policies, etc.) using Terraform.
2.  Uploading the static website files (HTML, CSS, JavaScript, images) to the S3 bucket. This can be done manually via the AWS Console or automated using the AWS CLI.