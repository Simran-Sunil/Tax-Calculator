# Tax Calculator Project

## 📋 Overview

This project demonstrates the implementation of a Tax Calculator application using modern cloud-native practices and DevOps principles. The application has been containerized, tested, and deployed using a CI/CD pipeline on IBM Cloud Code Engine.

<img width="854" alt="Calculator" src="https://github.com/user-attachments/assets/2540ea4b-4d9f-4c9a-a5fe-e5cd9d695451" />

## 🚀 Features

- **Containerized Application**: Packaged with Docker for consistent deployment
- **Automated Testing**: Unit tests using Jasmine framework
- **CI/CD Pipeline**: Continuous Integration and Deployment using Tekton
- **Cloud Deployment**: Deployed on IBM Cloud Code Engine

## 🔧 Technologies Used

- Frontend: HTML, CSS, JavaScript
- Testing: Jasmine
- Containerization: Docker, Nginx
- CI/CD: Tekton Pipeline
- Cloud Platform: IBM Cloud Code Engine

## 📝 Project Implementation

### 1. Running Unit Tests

The application uses Jasmine to ensure code quality through unit tests. All seven tests pass successfully, validating the core functionality of the tax calculator.

### 2. Containerization with Docker

Created a Dockerfile to containerize the application using Nginx as the base image. The Docker image was built, tagged as 'tax-calculator', and tested locally to ensure proper functionality.

### 3. Deployment to IBM Cloud

The Docker image was pushed to IBM Container Registry (ICR) and deployed on IBM Cloud Code Engine, making the application accessible through a public URL.

### 4. CI/CD Pipeline Setup

Implemented a Tekton pipeline with tasks for npm installation, Jasmine testing, and container image building using Buildah. The pipeline automates the entire workflow from code to deployment.

### 5. Final Deployment

Successfully deployed the application from a different branch (v2) to showcase dynamic updates and the effectiveness of the CI/CD pipeline.

## 🛠️ Project Structure

```
tax-calculator/
├── index.html
├── scripts/
│   ├── main.js
│   └── tax-calculator.js
├── styles/
│   └── styles.css
├── spec/
│   └── tax-calculator.spec.js
├── Dockerfile
├── package.json
└── README.md
```

## 📊 Pipeline Architecture

The Tekton pipeline follows this sequence:
1. Clone repository
2. Install NPM dependencies
3. Run Jasmine tests
4. Build Docker image with Buildah
5. Push to container registry
6. Deploy to Code Engine

## 🚀 How to Run Locally

1. Clone the repository:
```bash
git clone https://github.com/Simran-Sunil/Tax-Calculator.git
cd zntwk-tax_calculator
```

2. Install dependencies:
```bash
npm install
```

3. Run tests:
```bash
npx jasmine
```

4. Start the server:
```bash
python3 -m http.server
```

5. Open in browser: http://localhost:8000

## 🔄 Building and Running with Docker

```bash
# Build the Docker image
docker build -t tax-calculator .

# Run the container
docker run -d -p 8080:80 tax-calculator

# Access at http://localhost:8080
```

## 🌐 Cloud Deployment

The application is deployed on IBM Cloud Code Engine and can be accessed at the URL provided in the deployment output.

## 📚 Lessons Learned

Through this project, I gained experience with:

- Creating a proper Dockerfile for web applications
- Setting up and running JavaScript unit tests
- Working with Kubernetes secrets for secure deployment
- Implementing a full CI/CD pipeline with Tekton
- Deploying containerized applications to the cloud

## 🔗 References

- [IBM Cloud Code Engine Documentation](https://cloud.ibm.com/docs/codeengine)
- [Tekton Pipelines](https://tekton.dev/)
- [Docker Documentation](https://docs.docker.com/)
- [Jasmine Testing Framework](https://jasmine.github.io/)

## ✅ Assessment Completion

This project successfully implements all the required objectives:
- [x] Containerized the application
- [x] Ran unit tests as part of the pipeline
- [x] Deployed the application when all tests passed
- [x] Replaced hard-coded configuration
- [x] Re-deployed the application with passing tests

---

Developed as part of the Cloud Native, DevOps, Agile, and NoSQL course.
