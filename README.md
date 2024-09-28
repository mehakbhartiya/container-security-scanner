# Container Security Scanner

![Trivy logo](https://img.shields.io/badge/Trivy-Security%20Scanner-green?style=for-the-badge&logo=trivy)

## Overview
The **Container Security Scanner** project automates the scanning of Docker images for vulnerabilities using **Trivy**. It integrates with **GitHub Actions** for continuous security checks within CI/CD pipelines, ensuring that only secure images are deployed.

## Key Features
- **Automated Docker Image Scanning**: Vulnerability scanning during CI/CD workflows.
- **Multi-Image Support**: Can scan multiple images (e.g., nginx, redis).
- **Vulnerability Reports**: Provides detailed JSON reports.
- **Lightweight**: Designed to run on low-resource environments like AWS t2.micro.

## Tools & Technologies
- **Trivy**: A popular open-source vulnerability scanner.
- **GitHub Actions**: Automates the CI/CD process.
- **Docker**: For managing and running containerized applications.

---

## How It Works

This project uses **GitHub Actions** to automate vulnerability scans for Docker images. Each time code is pushed, Trivy runs and scans the images. Reports are generated in JSON format for analysis.

---

## Enhancements

- **Resource Optimization**: Run containers with limited resources for better performance on t2.micro:
  ```bash
  docker run --cpus=".5" --memory="512m" nginx 
