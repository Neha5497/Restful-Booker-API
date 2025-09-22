# Restful Booker API Testing Project

A comprehensive testing suite for the Restful Booker API, including functional, security, and integration testing with automated test execution capabilities.

## 📋 Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Test Execution](#test-execution)
- [Test Documentation](#test-documentation)
- [Bug Reports & Tracking](#bug-reports--tracking)
- [Contributing](#contributing)
- [API Endpoints](#api-endpoints)
- [Test Coverage](#test-coverage)
- [Known Issues](#known-issues)
- [Contact](#contact)

## 🎯 Overview

This project contains a complete testing framework for the **Restful Booker API** - a RESTful web service for managing hotel bookings. The testing suite covers:

- ✅ **Authentication & Authorization**
- ✅ **Booking Management (CRUD Operations)**
- ✅ **Data Validation & Error Handling**
- ✅ **Security Testing**
- ✅ **Integration Testing**

### Key Features

- **25 Comprehensive Test Cases** covering all API endpoints
- **Automated Test Execution** using Postman
- **Detailed Bug Reporting** with CSV tracking
- **Requirements Traceability Matrix (RTM)**
- **CI/CD Integration Ready**

```

## 🔧 Prerequisites

Before running the tests, ensure you have:

- **Postman** (latest version) - [Download here](https://www.postman.com/downloads/)
- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **Internet Connection** - API is hosted on Heroku
- **Git** (for version control)

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd Restful-Booker-API-Testing
```

### 3. Import Postman Collection
1. Open Postman
2. Click **Import**
3. Select `Restful Booker API Project.postman_collection.json`
4. Collection will be imported with all test cases

### 4. Verify API Accessibility
Test the base URL: `https://restful-booker.herokuapp.com/ping`

Expected Response: `Created`

## 🚀 Test Execution

### Postman GUI
1. Open Postman
2. Select the imported collection
3. Click **Run Collection**
4. Configure test settings and execute
```

## 📚 Test Documentation

### Test Cases Overview

| Module | Test Cases | Coverage |
|--------|------------|----------|
| Authentication | TC001-TC005 | Login, Invalid credentials, Missing fields |
| Booking Creation | TC006-TC012 | Valid/Invalid data, Business logic |
| Booking Retrieval | TC013-TC016 | Get bookings, Invalid IDs |
| Booking Filtering | TC017-TC018 | Name/Date filtering |
| Booking Updates | TC019-TC023 | PUT/PATCH operations |
| Booking Deletion | TC024-TC025 | Delete with/without auth |

### Key Test Scenarios

#### ✅ Positive Test Cases
- Valid user authentication
- Complete booking creation
- Successful booking retrieval
- Proper filtering functionality

#### ❌ Negative Test Cases
- Invalid authentication attempts
- Malformed booking data
- Non-existent resource access
- Unauthorized operations

#### 🔒 Security Test Cases
- Authentication bypass attempts
- Authorization validation
- Unauthorized deletion prevention

## 🐛 Bug Reports & Tracking

### Critical Issues Identified

| Bug ID | Severity | Description | Status |
|--------|----------|-------------|--------|
| BUG-018 | Critical | Unauthorized deletion allowed | Open |
| BUG-005 | High | Invalid data types cause 500 errors | Open |
| BUG-007 | High | Business logic validation missing | Open |
| BUG-011 | High | Date filtering causes server errors | Open |

## 🤝 Contributing

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-tests`)
3. Add your test cases or improvements
4. Commit changes (`git commit -m 'Add new security tests'`)
5. Push to branch (`git push origin feature/new-tests`)
6. Create a Pull Request

### Contribution Guidelines
- Follow existing test case naming conventions
- Include detailed test descriptions
- Add appropriate assertions and validations
- Update documentation for new features
- Ensure all tests pass before submitting

## 🌐 API Endpoints

### Base URL
```
https://restful-booker.herokuapp.com
```

### Available Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| GET | `/ping` | Health check | No |
| POST | `/auth` | Create authentication token | No |
| GET | `/booking` | Get all booking IDs | No |
| GET | `/booking/{id}` | Get specific booking | No |
| POST | `/booking` | Create new booking | No |
| PUT | `/booking/{id}` | Update booking (full) | Yes |
| PATCH | `/booking/{id}` | Update booking (partial) | Yes |
| DELETE | `/booking/{id}` | Delete booking | Yes |

### Authentication
- **Basic Auth:** Username: `admin`, Password: `password123`
- **Token Auth:** Use `/auth` endpoint to generate token

## 📊 Test Coverage

### Current Coverage Statistics
- **Total Test Cases:** 25
- **Passed:** 13 (52%)
- **Failed:** 12 (48%)
- **Critical Issues:** 4
- **High Priority Issues:** 8
- **Medium Priority Issues:** 4
- **Low Priority Issues:** 2

### Coverage by Module
- **Authentication:** 60% (3/5 passing)
- **Booking Creation:** 57% (4/7 passing)
- **Booking Retrieval:** 75% (3/4 passing)
- **Booking Filtering:** 50% (1/2 passing)
- **Booking Updates:** 20% (1/5 passing)
- **Booking Deletion:** 0% (0/2 passing)

## ⚠️ Known Issues

### High Priority Issues
1. **Security Vulnerability:** Unauthorized deletion allowed (TC025)
2. **Authentication Issues:** Wrong HTTP status codes for invalid credentials
3. **Update Operations:** All PUT/PATCH operations returning 403 errors
4. **Date Filtering:** Server errors when filtering by date range

### Workarounds
- Use GET operations for read-only testing
- Manual verification required for update operations
- Alternative authentication methods may be needed
---

**Happy Testing! 🎉**


For questions or support, please create an issue or contact the testing team.
