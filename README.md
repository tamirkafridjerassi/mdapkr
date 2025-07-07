mdapkr – Emergency Crew and Mission Management Service
mdapkr is a backend microservice for managing emergency response personnel and missions. Built with FastAPI, MongoDB, and fully containerized using Docker, the service provides a structured API for adding, retrieving, and managing crew members and mission data.

The repository also includes infrastructure provisioning scripts using Terraform and deployment templates via Helm, enabling seamless deployment to cloud environments or Kubernetes clusters.

Overview
This service is part of a modular architecture designed to support real-time coordination, assignment, and resource management for emergency response teams.

Key components include:

RESTful API for personnel and mission records

Schema validation and automatic documentation with FastAPI

Containerized development and deployment with Docker

Testing support via docker-compose.test.yml

Infrastructure and Helm chart templates for production deployment

Features
Crew Management (/person): Create, update, retrieve personnel records

Mission Management (/mission): Register, update, and view active missions

Interactive API Docs: FastAPI’s auto-generated documentation is available at /docs

Extensibility: Easily integrated with external services and front-end clients

Getting Started
Prerequisites
Docker and Docker Compose installed

Git CLI (optional: Python 3.11+ for local development without Docker)

Clone the Repository
bash
Copy
Edit
git clone https://github.com/tamirkafridjerassi/mdapkr.git
cd mdapkr/fastapi-app
Running the Service with Docker
bash
Copy
Edit
docker-compose up --build
Access the API documentation at:
http://localhost:8000/docs

Running Tests
To execute the test suite in an isolated environment:

bash
Copy
Edit
docker-compose -f docker-compose.test.yml up --build
Project Structure
bash
Copy
Edit
mdapkr/
├── fastapi-app/               # Core FastAPI application
│   ├── main.py                # Entry point
│   ├── routes/                # API route definitions
│   ├── models/                # Data schemas and validation
│   └── ...                    # Additional business logic
├── tests/                     # Unit and integration tests
├── docker-compose.yml         # Development environment
├── docker-compose.test.yml    # Testing environment
├── terraform/                 # Infrastructure-as-Code (IaC) configuration
├── helm/                      # Kubernetes Helm charts for deployment
└── README.md
Deployment
Terraform
Infrastructure provisioning can be done using the scripts in the terraform/ directory. This can be adapted for providers such as AWS, GCP, or Azure.

Helm
The Helm chart in the helm/ directory provides configuration templates for Kubernetes deployment. Custom values can be applied for staging, production, or development environments.

Contributing
Contributions, bug reports, and feature requests are welcome. Please open an issue or submit a pull request with relevant details.

License
This repository is licensed under the MIT License. See the LICENSE file for details.

Maintainer
Tamir Kafri Djerassi
GitHub: @tamirkafridjerassi
