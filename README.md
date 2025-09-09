# Flask Dockerized Web App with AWS Elastic Beanstalk Deployment

This is a beginner-friendly **Python Flask web application** that is:

- Containerized using **Docker**
- Deployed on **AWS Elastic Beanstalk** (Free Tier)
- Enhanced with basic **DevSecOps** security scanning tools
- Powered by **Gunicorn** for production-ready deployment

1. Run the App with Docker
    Build docker image
    Run the container 

Access the app:
    http://localhost:5000

2. Deploy to AWS Elastic Beanstalk (EB)
This app is ready for deployment to AWS EB using the Docker platform.

Steps:
    Install EB CLI 
    Initialize your EB project:
    Create and deploy the app:

3. DevSecOps: Security Scanning Pipeline

This project includes a GitHub Actions CI/CD pipeline that runs:

    Static Application Security Testing (SAST)
        Uses Semgrep to scan Python code for security issues

    Container Vulnerability Scanning
        Uses Trivy to scan Docker images for known CVEs

    Workflow Features
        On every push to main:
            App is built
            Security scans run
            Scan reports uploaded as CI artifacts

4. Gunicorn + WSGI Setup (Production-Ready)
Instead of using app.run(), the app uses a wsgi.py file to expose the Flask app via a WSGI interface.

This setup is:
    Safer for production
    Recommended for Elastic Beanstalk
    Complies with Flask deployment best practices
