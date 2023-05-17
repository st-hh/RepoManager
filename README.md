# Repository Management Toolkit

The Repository Management Toolkit is a collection of scripts designed to simplify repository management tasks using the GitHub API. These scripts automate the process of checking dependencies, fetching repository names, cloning repositories, and executing all the scripts sequentially.

## Features

- **Dependency Check**: The `check_dependencies.sh` script verifies the presence of necessary dependencies (`git`, `curl`, `jq`) on the system and installs them if missing.

- **Repository Fetching**: The `fetch_repositories.sh` script interacts with the GitHub API to fetch the names of repositories associated with your GitHub account. It requires providing the necessary credentials in a `credentials.txt` file.

- **Repository Cloning**: The `clone_repositories.sh` script allows you to select repositories to clone from the fetched repository names. It clones the selected repositories, configures email and username for each repository, and sets the personal access token as the remote URL.

- **Sequential Execution**: The `run_all_scripts.sh` script runs all the scripts sequentially, ensuring that dependencies are checked, repository names are fetched, and repositories are cloned. If any of the scripts encounter an error, the execution stops.

## Getting Started

1. Clone the Repository Management Toolkit repository:
   ```bash
   git clone https://github.com/your-username/repo-management-toolkit.git
2. Navigate to the repository directory:
   ```bash
   cd repo-management-toolkit
3. Provide credentials:
Create a credentials.txt file in the repository directory.
Add the following information to the file:
   ```bash
   github_username="your-github-username"
   github_token="your-github-personal-access-token"
   email="your-email"
   username="your-username"
4. Make the scripts executable:
   ```bash
   chmod +x check_dependencies.sh fetch_repositories.sh clone_repositories.sh run_all_scripts.sh
5. Run the desired script(s) individually or execute them sequentially using run_all_scripts.sh.
