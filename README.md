# Purpose
This CLI allows the user to update files in a remote Github repository from the command line. This can be particularly useful when automating a process that requires editing the same file across many repositories, such as updating microservices in a large scale application.

# Implementation
This is a Flask application that utilizes the PyGithub library (a library to allow access to the Github API through Python code) to clone files, create branches, create pull requests, and commit file changes to the remote.

# Parameters for Command
* Global Parameters
  1. Personal Access Token
  2. Github Server Address (e.g. "github.{company_name}.com"
  3. Source Branch (e.g. "main")
  4. Local File Location to Clone File
* Parameters Specific to Request
  1. Repository Name
  2. File to Update
  3. Branch Name
  4. Open Pull Request? (True/False)
      - Pull Request Title
      - Pull Request Body
  5. Script to Run for File Update

Sample command: 
`set PERSONAL_ACCESS_TOKEN = your_token_here`
`set GITHUB_SERVER_ADDRESS = your_github_server_address_here`
`set SOURCE_BRANCH = your_source_branch_here`
`set LOCAL_FILE_CLONE_LOCATION = "C:\Users\user\Documents"`
`code-publish^ 
--open-pull-request=True --pr_title="Your PR Title" --pr_body="Your PR Body" 
^--branch_name="your_branch_name" 
^--file_to_update="file.py" 
^--file_edit_scripts="C:\users\documents\edit.py`
