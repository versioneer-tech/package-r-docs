# End-to-End Scenario: Curating and Sharing a Dataset

## 1. Data Curator

### Objective:
The Data Curator aims to assemble and organize a dataset by referencing external files and creating a structured data package.

### Steps:

- **Access the packageR UI**:
  - The Data Curator logs into the packageR UI and navigates to the section for curating datasets.

- **Reference External Data**:
  - The curator selects the option to register external data. 
  - They enter URLs pointing to data objects stored in cloud storage (e.g., Amazon S3, Google Cloud Storage) using the `git annex addurl <url>` command in the UI.
  - As they add URLs, they organize them into a meaningful folder hierarchy, making the dataset easy to navigate.

- **Add Documentation**:
  - The curator creates a `README.md` file directly within the UI to provide context for the dataset. This file includes details on the data's origin, structure, and any relevant metadata.
  
- **Sync with Git Repository**:
  - Once the data package is ready, the curator pushes the changes to a Git repository (e.g., GitHub or GitLab) using the UI's built-in sync functionality. 
  - Behind the scenes, this corresponds to executing a standard `git push` command:
    ```bash
    git push origin main
    ```

---

## 2. Data Governance

### Objective:
The Data Governance professional ensures that access to the data package is properly managed, maintaining security and compliance.

### Steps:

- **Set Repository Visibility**:
  - The Data Governance professional accesses the Git repository settings via GitHub/GitLab.
  - They decide to make the repository **private**, ensuring that only authorized users can access the actual data while metadata remains visible.

- **Manage Permissions**:
  - They add users who require access to the dataset, assigning at least **read permissions**. This enables those users to resolve data references using Git Annex.
  - For example, if a Data Scientist needs access, the governance professional would add them to the repository with the appropriate role.

- **Monitor Access Control**:
  - The Data Governance professional periodically reviews permissions and ensures compliance with data governance policies, adjusting access as needed.

---

## 3. Data Scientist/Collaborator

### Objective:
The Data Scientist or Collaborator works with the curated dataset, selectively downloading the necessary data for analysis and potentially contributing back to the repository.

### Steps:

- **Clone the Repository**:
  - The Data Scientist clones the Git repository to their local machine using the command:
    ```bash
    git clone https://github.com/username/repo.git
    ```
  - This action retrieves the folder hierarchy and metadata (including the `README.md`).

- **Resolve Data**:
  - After reviewing the contents, the Data Scientist identifies specific files they need for their analysis.
  - They run the command to download a specific file or folder using Git Annex:
    ```bash
    git annex get <file_or_folder_name>
    ```
  - This retrieves the required data files without needing to download the entire dataset.

- **Add Contributions** (if permissions allow):
  - If the Data Scientist has write permissions, they can add new data references or documentation.
  - For example, they might create a new analysis report and add it to the repository:
    ```bash
    echo "Analysis report" > analysis_report.md
    git add analysis_report.md
    git commit -m "Added analysis report"
    git push origin main
    ```

---

## Summary

Through this end-to-end scenario, each persona interacts with **packageR** at different stages of the data lifecycle:

- The **Data Curator** focuses on organizing and structuring datasets by referencing external data and adding necessary documentation.
- The **Data Governance** professional manages repository visibility and permissions, ensuring secure access to sensitive data.
- The **Data Scientist** utilizes the curated data for analysis, downloading only the required files and contributing back to the repository when necessary.

This collaborative workflow illustrates the power of **packageR** in enabling efficient data management, sharing, and analysis across different user roles while maintaining security and flexibility.
