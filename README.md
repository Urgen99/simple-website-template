# 🚀 CI/CD Pipeline with Jenkins, GitHub, SonarQube & Docker on AWS

## 📌 Overview
Designed and implemented a robust Continuous Integration and Continuous Deployment (CI/CD) pipeline to automate the build, test, and deployment of a Dockerized web application using:

- **Jenkins** for orchestration
- **GitHub** for version control
- **SonarQube** for static code analysis
- **Docker** for containerization
- **AWS EC2** instances for cloud hosting

## 🔁 Pipeline Workflow

1. **📥 GitHub Integration**
   - Source code is maintained in a GitHub repository.
   - Webhooks trigger Jenkins jobs automatically on every commit.
   - ![GitHub Webhook Setup](screenshots/githubwebhook.png)

2. **🛠 Jenkins Automation**
   - Jenkins pulls the latest code and orchestrates the pipeline.
   - Freestyle or scripted jobs define build/test/deploy stages.
   - ![Jenkins Pipeline Job](screenshots/jenkins-job.png)

3. **🧪 SonarQube Code Quality Analysis**
   - Jenkins runs SonarQube scanner to analyze code quality.
   - Fails the build if code doesn't meet quality gates.
   - ![SonarQube Analysis](screenshots/sonarqube-results.png)

4. **🐳 Docker Containerization**
   - Jenkins builds Docker images from the source.
   - Pushes the image and runs it on a Docker server (EC2).
   - ![Docker Container Running](screenshots/docker-container.png)

5. **☁️ Deployment on AWS EC2**
   - Separate EC2 instances for Jenkins/SonarQube and Docker.
   - Nginx used to serve the application on the target EC2.
   - ![AWS EC2 Setup](screenshots/aws-ec2.png)


