# Repository Management Toolkit

The Repository Management Toolkit is a collection of scripts designed to simplify repository management tasks using the GitHub API. These scripts automate the process of checking dependencies, fetching repository names, cloning repositories, and executing all the scripts sequentially.

## Features

- **Dependency Check**: The `check_dependencies.sh` script verifies the presence of necessary dependencies (`git`, `curl`, `jq`) on the system and installs them if missing.

- **Repository Fetching**: The `fetch_repositories.sh` script interacts with the GitHub API to fetch the names of repositories associated with your GitHub account. It requires providing the necessary credentials in a `credentials.txt` file.

- **Repository Cloning**: The `clone_repositories.sh` script allows you to select repositories to clone from the fetched repository names. It clones the selected repositories, configures email and username for each repository, and sets the personal access token as the remote URL.

- **Sequential Execution**: The `run_all_scripts.sh` script runs all the scripts sequentially, ensuring that dependencies are checked, repository names are fetched, and repositories are cloned. If any of the scripts encounter an error, the execution stops.

# Requirements

The Repository Management Toolkit has the following requirements to run successfully:

## Operating System

 - **Linux**
 - **macOS**

## Dependencies

The following dependencies need to be installed on your system:

- **git**: Version 2.0 or above
- **curl**: Version 7.0 or above
- **jq**: Version 1.6 or above

## Supported Package Managers

The script utilizes the following package managers for installing dependencies:

- **apt-get**: For Debian-based Linux distributions
- **yum**: For Red Hat-based Linux distributions
- **brew**: For macOS

If you're using a different package manager or operating system, you may need to modify the script to install the required dependencies manually.

## GitHub Credentials

To interact with the GitHub API, you need to provide the following credentials **interactively** or in a `credentials.txt` file:

- **github_username**: Your GitHub username
- **github_token**: Your GitHub personal access token
- **email**: Your email address
- **username**: Your desired username for the repository configuration

Ensure that the `credentials.txt` file is present in the repository directory and contains the correct information. Otherwise it will prompt you for GitHub credentials interactively and save them to the `credentials.txt` file.

## Getting Started

1. Clone the Repository Management Toolkit repository:
   ```bash
   git clone https://github.com/your-username/repo-management-toolkit.git
2. Navigate to the repository directory:
   ```bash
   cd repo-management-toolkit

3. Provide credentials:
**Optional**
Create a credentials.txt file in the repository directory.
Add the following information to the file:
   ```bash
   github_username="your-github-username"
   github_token="your-github-personal-access-token"
   email="your-email"
   username="your-username"

**NB:** If you skipp this step, you will be prompted for this info interactively.

4. Make the scripts executable:
   ```bash
   chmod +x check_dependencies.sh fetch_repositories.sh clone_repositories.sh run_all_scripts.sh

5. Run the desired script(s) individually or execute them sequentially using run_all_scripts.sh.
   ```bash
   ./run_all_scripts.sh

## License

