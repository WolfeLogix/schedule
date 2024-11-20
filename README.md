# Schedule

## Overview
This repository contains the configuration and workflows for an enterprise scheduler. The primary purpose of this scheduler is to automate various tasks and processes, ensuring they run at specified times or can be triggered manually as needed.

## Workflows
### Nightly Tax Classification
This workflow sets the tax classification for unclassified products. It runs nightly on weekdays at midnight EST (5 AM UTC) and can also be triggered manually.

#### Configuration
- **Schedule**: Runs at midnight EST (5 AM UTC) on weekdays.
- **Manual Trigger**: Can be triggered manually via the GitHub Actions interface.

#### Job Details
- **Job Name**: `send_request`
- **Runs On**: `ubuntu-latest`
- **Steps**:
  - **Send request to URL**: Sends a POST request to the specified URL with the necessary authorization token.

## Environment Variables
The following environment variables are required for the workflows to function correctly:
- `TAX_CLASSIFICATION_URL`: The URL to which the tax classification request is sent.
- `API_TOKEN`: The authorization token used to authenticate the request.

## Usage
To use this scheduler, ensure that the necessary environment variables are set up in your repository's secrets. You can then monitor and manage the workflows via the GitHub Actions interface.

## Contributing
Contributions to improve the scheduler or add new workflows are welcome. Please ensure that any new workflows are well-documented and tested.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.