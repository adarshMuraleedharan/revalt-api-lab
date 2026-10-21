# revalt-api-testbench
Experimental development and testing environment for REVALT REST APIs, Postman collections, HTTP fundamentals, automated API testing, and future backend and IoT integrations.

# REVALT API Lab

**API Development | REST API Testing | Postman | Backend Integration | IoT Connectivity**

A structured development and testing repository for exploring, implementing, validating and documenting HTTP-based APIs and backend integrations within the REVALT technical ecosystem.

## 1. Project Overview

**REVALT API Lab** serves as an experimental development workspace for learning API fundamentals, building reusable API test collections and evaluating integration workflows.

The repository initially focuses on HTTP and REST API testing using **Postman integrated with Visual Studio Code**.

As development progresses, it is intended to support more advanced capabilities, including automated API validation, authentication testing, error handling, backend service integration and IoT-related data exchange.

This repository is intended for development, experimentation and testing purposes. It is not a production API service.

## 2. Project Objectives

The primary objectives are to:

- Establish a foundational understanding of HTTP and REST API operations.
- Develop and organise reusable Postman collections.
- Practise API requests using GET, POST, PUT, PATCH and DELETE methods.
- Understand JSON request and response structures.
- Explore authentication, request headers, query parameters and HTTP status codes.
- Develop structured API validation and debugging techniques.
- Introduce automated API testing and regression testing.
- Build a scalable framework for future backend and IoT API integration.
- Maintain version-controlled API tests and technical documentation.

## 3. Technology Stack

| Technology | Purpose |
|---|---|
| Visual Studio Code | Primary development environment |
| Postman | API development, testing and debugging |
| HTTP/HTTPS | Application-layer communication |
| REST API | Resource-oriented API interaction |
| JSON | Request and response data representation |
| Git | Source and version control |
| GitHub | Repository hosting and collaboration |
| JavaScript | API test scripting and automation |
| Python | Potential future integration testing |
| Notion | Project management and Kanban task tracking |

Additional tools and frameworks may be introduced as project requirements evolve.

## 4. Repository Structure

```text
revalt-api-lab/
│
├── postman/
│   ├── collections/
│   └── environments/
│
├── api-tests/
│
├── examples/
│   ├── get/
│   ├── post/
│   ├── put-patch/
│   └── delete/
│
├── docs/
│
├── .gitignore
└── README.md
```

### Directory Descriptions

| Directory | Description |
|---|---|
| `postman/collections/` | Exported Postman collections containing reusable API requests and tests |
| `postman/environments/` | Sanitised environment templates and non-sensitive configuration examples |
| `api-tests/` | Automated test scripts, assertions and regression testing resources |
| `examples/get/` | GET request examples for retrieving API resources |
| `examples/post/` | POST request examples for submitting data and creating resources |
| `examples/put-patch/` | PUT and PATCH examples for updating API resources |
| `examples/delete/` | DELETE request examples and deletion-response validation |
| `docs/` | API specifications, integration notes, debugging procedures and technical references |
| `.gitignore` | Excludes local configuration, credentials and generated files from version control |
| `README.md` | Project overview, setup instructions and development guidelines |

## 5. Development Roadmap

### Phase 1 — HTTP and REST API Fundamentals

**Goal:** Establish practical proficiency in HTTP requests and REST API interactions.

- [ ] Configure Postman within Visual Studio Code.
- [ ] Execute GET requests and inspect JSON responses.
- [ ] Create resources using POST requests.
- [ ] Update resources using PUT and PATCH requests.
- [ ] Perform DELETE operations.
- [ ] Understand HTTP headers and query parameters.
- [ ] Interpret HTTP response status codes.
- [ ] Document common API errors and troubleshooting methods.

**Expected outcome:** Ability to independently construct, execute and troubleshoot basic REST API requests.

### Phase 2 — API Collections and Environment Management

**Goal:** Establish structured and reusable API testing workflows.

- [ ] Create and organise Postman collections.
- [ ] Configure development and testing environments.
- [ ] Implement reusable environment and collection variables.
- [ ] Explore API key and Bearer token authentication.
- [ ] Configure request chaining.
- [ ] Document API endpoints and their parameters.

**Expected outcome:** A reusable API test workspace with organised requests and controlled configurations.

### Phase 3 — API Test Automation

**Goal:** Introduce repeatable API validation procedures.

- [ ] Write JavaScript-based response assertions.
- [ ] Validate HTTP status codes.
- [ ] Validate response body fields and JSON structures.
- [ ] Test invalid parameters and error responses.
- [ ] Execute collections through the Postman Collection Runner.
- [ ] Explore command-line API testing.
- [ ] Investigate integration with CI/CD workflows.

**Expected outcome:** Repeatable automated API tests capable of detecting unexpected response behaviour.

### Phase 4 — Backend and IoT API Integration

**Goal:** Extend testing capabilities toward application and connected-device integration.

Potential development areas include:

- [ ] Device registration and identification APIs.
- [ ] Authentication and access control validation.
- [ ] Device status and telemetry retrieval.
- [ ] API error handling and fault response validation.
- [ ] HTTP-based device management workflows.
- [ ] Backend data processing and validation.
- [ ] API integration testing with simulated IoT data.
- [ ] Evaluation of request latency, failures and retry behaviour.

**Expected outcome:** A structured API integration test environment supporting backend and IoT development activities.

*Note: Direct TCP socket communication and proprietary device protocols may require additional testing tools beyond Postman.*

## 6. Getting Started

### Prerequisites

Install or configure the following:

1. [Visual Studio Code](https://code.visualstudio.com/)
2. [Postman](https://www.postman.com/) or the Postman VS Code extension
3. [Git](https://git-scm.com/)
4. A GitHub account with authorised repository access

### Clone the Repository

```bash
git clone <repository-url>
cd revalt-api-lab
```

Replace `<repository-url>` with the actual GitHub repository URL.

### Configure Postman

1. Launch Visual Studio Code.
2. Open the Extensions panel.
3. Install the official Postman extension.
4. Sign in to your Postman account.
5. Open the REVALT API Lab workspace or create a new workspace.
6. Import existing collections from `postman/collections/`, if available.

Postman collections can be exported as JSON files and maintained under Git version control.

### First API Request

Use the public JSONPlaceholder API to test a GET request.

**Method:** `GET`

**Endpoint:**

```http
GET https://jsonplaceholder.typicode.com/posts/1
```

**Expected status:** `200 OK`

**Example response structure:**

```json
{
  "userId": 1,
  "id": 1,
  "title": "Example post title",
  "body": "Example post content"
}
```

The example above illustrates the response structure; the live service returns its own sample content.

### Recommended Testing Workflow

1. Create or select an API request.
2. Configure the HTTP method and endpoint.
3. Add required headers, parameters and request body.
4. Execute the request.
5. Inspect the HTTP response status, headers and body.
6. Validate the response against expected behaviour.
7. Record unexpected behaviour or errors.
8. Save and export the updated collection when appropriate.
9. Commit reviewed, non-sensitive changes to Git.

## 7. API Testing Conventions

The following conventions are recommended to maintain consistent test organisation.

### Request Naming

Use descriptive request names:

```text
GET    - Retrieve Resource
POST   - Create Resource
PUT    - Replace Resource
PATCH  - Update Resource Fields
DELETE - Delete Resource
```

### Test Case Documentation

Each test case should define:

| Field | Description |
|---|---|
| Test ID | Unique identifier |
| Test objective | Purpose of the test |
| HTTP method | GET, POST, PUT, PATCH or DELETE |
| Endpoint | API resource URL |
| Request data | Parameters, headers and body |
| Expected response | Expected status and response fields |
| Actual response | Observed response and behaviour |
| Test result | Pass, Fail or Blocked |
| Remarks | Debugging notes and references |

### Example Test Identifier

`API-GET-001`

Example description: Verify successful retrieval of an existing API resource.

## 8. Source Control and Development Practices

Git is used to maintain a record of project changes.

Recommended practices:

- Use descriptive commit messages.
- Keep API collections organised by purpose.
- Commit validated test cases and documentation.
- Avoid committing temporary testing outputs.
- Review changes before pushing to the remote repository.
- Use dedicated branches for substantial new features.
- Link development work to corresponding project-management tasks where applicable.

### Example Commit Messages

```text
docs: initialise REVALT API Lab README
test: add GET request collection
test: add POST request examples
feat: introduce API response validation
fix: correct request payload format
refactor: reorganise Postman collections
```

## 9. Security and Configuration Management

This repository may eventually be used to explore integration with commercial backend services.

To maintain security:

- Never commit passwords, API keys, authentication tokens or private certificates.
- Avoid storing production credentials in Postman collections.
- Use environment variables for configuration values.
- Commit example environment templates rather than credential-bearing environment exports.
- Do not publish proprietary API specifications without authorisation.
- Avoid including real customer, rider or device-identifying information in test datasets.
- Use mock data and non-production endpoints wherever possible.

**Important:** A private repository is not a substitute for secure credential management.

## 10. Documentation and Project Tracking

Development tasks may be managed through a Notion Kanban board.

Suggested workflow:

`Planned → In Progress → Review → Done`

Each development card should ideally include:

- Task description and objective.
- Related API endpoint or feature.
- Acceptance criteria.
- Relevant repository branch or commit.
- Testing results and observations.
- Supporting documentation.

Notion serves as the project-management layer, while Git remains the source-control system.

## 11. Project Status

**Status:** Initial development and learning phase

**Current focus:** HTTP and REST API fundamentals using Postman within Visual Studio Code.

**Planned direction:** API testing automation, backend integration validation and IoT-oriented API workflows.

Features listed in the roadmap represent planned capabilities and should not be interpreted as existing implementations.

## 12. Licence and Usage

This repository is currently intended for private development, learning, experimentation and authorised technical collaboration.

No open-source licence has been assigned.

All proprietary code, documentation and integration materials are subject to the applicable intellectual property ownership, confidentiality obligations and company agreements.

---

**REVALT API Lab**

*Building a structured foundation for reliable API development, testing and connected-system integration.*
