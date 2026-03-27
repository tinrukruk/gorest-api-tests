# GoRest API Testing - QA Automation Exam

## Project Overview
This project contains automated API tests for the GoRest API (https://gorest.co.in). The tests cover CRUD operations for user management including create, read, update, and delete functionality.

### Test Coverage
| Endpoint | Method | Description |
|----------|--------|-------------|
| `/users` | POST | Create a new user |
| `/users/{id}` | GET | Fetch user details by ID |
| `/users?status=active` | GET | List all active users |
| `/users/{id}` | PUT | Update existing user |
| `/users/{id}` | DELETE | Delete user |

## Prerequisites

### Software Requirements
- **Node.js** (v14 or higher) - [Download](https://nodejs.org/)
- **npm** (comes with Node.js)
- **Newman** (Postman CLI tool)
- **Newman HTML Reporter** (for detailed test reports)

### Installation

#### 1. Install Node.js
Download and install Node.js from: https://nodejs.org/

Verify installation:
node --version
npm --version

#### 2. Install Newman and HTML ReporterInstall Newman and HTML Reporter
npm install -g newman
npm install -g newman-reporter-htmlextra

Verify installation:
newman --version

### Running Tests using CMD
Basic Command:
newman run QA_EXAM.postman_collection.json -e TEST_ENV.postman_environment.json

With HTML Report:
newman run QA_EXAM.postman_collection.json -e TEST_ENV.postman_environment.json -n 1 --reporters htmlextra --reporter-htmlextra-export reports/html-report.html --reporter-htmlextra-logs --reporter-htmlextra-testPaging
