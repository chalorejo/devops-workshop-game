# Rock Paper Scissors - Frontend

The frontend for the DevOps Workshop Game is a sleek, modern, and interactive Rock Paper Scissors application built with React and Vite. It serves as the user-facing interface for the game, featuring dynamic animations and a responsive design tailored with TailwindCSS.

## Requirements & Installation

Before you begin, ensure you have the following installed:
- **Node.js** (v20 or higher recommended)
- **npm** (comes with Node.js)

To set up the frontend locally, follow these steps:

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install the required dependencies:
   ```bash
   npm install
   ```

## Usage Guide

To run the application locally in development mode:

1. Start the Vite development server:
   ```bash
   npm run dev
   ```
2. Open your browser and navigate to `http://localhost:5173` (or the URL provided in your terminal).

To build the application for production:
```bash
npm run build
```
This will generate optimized static assets in the `dist` directory, which can be deployed to AWS S3 and CloudFront (as configured in the root AWS CDK stack).
