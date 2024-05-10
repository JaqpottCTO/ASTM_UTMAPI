Main Branch of ASTM UTM APIs
Overview
Welcome to the central repository for the development of standalone APIs that form the backbone of NASA's Unmanned Traffic Management (UTM) system. These APIs are designed to operate independently and integrate seamlessly within the broader UTM architecture, adhering to the modular X5 approach. The main branch contains the most stable and up-to-date version of the code that is ready for deployment.

Purpose
This repository serves multiple key purposes:

It acts as the primary hub for all developmental activities related to the UTM APIs, ensuring that all components are aligned with the latest approach of the UTM API Specifications Focus Group and broader Working Group.

1. Operational Intent Services - Demand Capacity Balancing (OIS-DCB)
  Team Members:
  David
  Hugo
  Tony
  Aryaman
  Michael

Purpose: Manages the dynamic balancing of airspace capacity based on operational intents.
Functionality: This API interfaces with both the Resource Status Information Service (RSIS) and the Discovery Synchronization Service (DSS) to provide real-time balancing of airspace demands with available capacities. It allows for the submission of operational intents and dynamically adjusts them according to changing airspace capacity constraints.
Key Endpoints:
POST /ois-dcb/intents: Submit operational intents for capacity validation.
GET /ois-dcb/capacity: Retrieve current and forecasted airspace capacity constraints.

2. Operational Intent Services - Discovery Synchronization Service (OIS-DSS)
  Team Members:
  David
  Hugo
  Tony
  Aryaman
  Michael

Purpose: Ensures synchronization and consistent status of operational intents across the UTM network.
Functionality: This API facilitates the discovery and synchronization of operational intents, maintaining consistency across the UTM ecosystem. It supports efficient data sharing and status updates among various UTM components to enhance overall system responsiveness and reliability.
Key Endpoints:
PUT /ois-dss/sync: Synchronize operational intents across different services.
GET /ois-dss/discover: Discover operational intents within the network.

3. Discovery Synchronization Service - Resource Capacity Information Service (DSS-RCIS)
  Team Members:
  Steven
  Jose
  Alexis
  Rafal
  (Tony?)   

Purpose: Manages information related to the capacities of UTM resources.
Functionality: This API focuses on providing access to resource capacity data which is critical for planning and demand management within the UTM system. It tracks and updates the status and capacities of various airspace resources, aiding in the strategic management of airspace utilization.
Key Endpoints:
GET /dss-rcis/resources: Fetch the capacity information for various UTM resources.
PATCH /dss-rcis/update: Update resource capacities based on operational data and forecasts.

4. Discovery Synchronization Service - Resource Status Information Service (DSS-RSIS)
  Team Members:
  Steven
  Jose
  Alexis
  Rafal
  (Tony?)

Purpose: Provides up-to-date status information on UTM resources.
Functionality: The API serves to communicate real-time status updates of UTM resources, ensuring that all components of the UTM system have the latest data regarding resource availability and operational status.
Key Endpoints:
GET /dss-rsis/status: Retrieve the current status of resources.
POST /dss-rsis/update: Post updates to the resource status as they occur.

5. Operator Intent Management - Operator (OIM-Operator)
  Team Members:
  Aryaman (still to verify)

Purpose: Handles the management of operator intents for UTM operations.
Functionality: This API is responsible for processing and managing the intents submitted by operators, including the creation, update, and cancellation of flight plans. It ensures that operational intents align with available resources and regulatory constraints.
Key Endpoints:
PUT /oim-operator/intents: Manage operator flight plans and intents.
GET /oim-operator/details: Retrieve details on the managed intents.

Getting Started
To begin working with the code in this repository:

Clone the Repository: Clone this repository to your local machine using the appropriate Git command to ensure you have the latest version of the main branch.

Contribution Guidelines
Contributors are encouraged to participate in the development of the APIs by following these guidelines:

Code Contributions: Always pull the latest changes from the main or specific API branch before starting your work. Ensure that your contributions are well-documented and adhere to the coding standards outlined in our contributing guidelines.

Testing: Implement and run tests to confirm that your code works as expected without breaking existing functionalities.

Pull Requests: Use pull requests for merging changes. Ensure your code is reviewed by at least one other developer before it can be merged into the main branch.
Testing

Documentation
When possible, APIs should be accompanied by comprehensive documentation, which should include:

API Usage Instructions: Clear, step-by-step instructions on how to use the API endpoints.
Configuration Guides: Information on necessary configurations and setup.
Examples: Practical examples demonstrating the API in action.

Reference Library:
Google Drive Intial APIs https://drive.google.com/drive/folders/1unXdjbiw2UCOq_QOvmIV5xMJ9PY59V3L

Reference Index and Updates:
Google Drive API Main Folder https://drive.google.com/drive/folders/1Aa22MGK9s4SZ45HN8sEOccscvUB6RA1d

Contact Information
For more information or to report issues, please contact the project team:
Steven C. Philpott Sr. steven.philpott@evertisky.com 
Antony Evans tony.evans@airbus-sv.com
David Murphy dmurphy@flyanra.com

Ongoing feedback from the community is encouraged to help improve the development of these APIs.
