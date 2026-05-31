# DevOps Workshop Game

The DevOps Workshop Game is a full-stack, cloud-native Rock Paper Scissors application designed to demonstrate infrastructure as code (IaC) and CI/CD pipelines. This project features a React/Vite frontend and an AWS CDK-powered backend that fully automates the provisioning of S3 buckets, CloudFront CDN, and a CodePipeline for continuous deployment.

## Requirements & Installation

To deploy and work with this project, you will need the following tools:
- **Node.js** (v20 or higher recommended)
- **AWS CLI** (configured with your AWS account credentials)
- **AWS CDK** (`npm install -g aws-cdk`)
- **Git**

To set up the project locally:

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd devops-workshop-game
   ```
2. Install the AWS CDK dependencies:
   ```bash
   npm install
   ```
3. Update `bin/devops-workshop-game.js` with your AWS Account ID and preferred Region.
4. Update the GitHub Source Action in `lib/devops-workshop-game-stack.js` with your GitHub username and configure your GitHub token in AWS Secrets Manager as `workshop/github`.

## Usage Guide

To synthesize the CloudFormation template and verify your CDK stack:
```bash
npx cdk synth
```

To deploy the infrastructure and the CodePipeline to your AWS account:
```bash
npx cdk deploy
```

Once deployed, any commits pushed to the `main` branch of your configured repository will automatically trigger the CodePipeline to build the Vite frontend and deploy the updated static assets to your S3 website bucket and CloudFront distribution.
