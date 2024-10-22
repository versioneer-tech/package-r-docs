# Data Scientist/Collaborator

As a **Data Scientist** or **Collaborator**, your role is to work with the data curated by the Data Curator, resolving specific datasets that you need for your analysis or research. You will utilize **Git Annex** to selectively download the data files referenced in the Git repository.

### Tasks and Responsibilities:
- **Clone the Repository**: Pull the metadata and structure of the data package from the Git repository.
- **Selectively Download Data**: Use `git annex get` to retrieve only the specific data files, folders, or entire datasets that you need for your analysis.
- **Interact with the Repository**: In addition to resolving data, you can contribute by adding new data references, documentation, or other files if you have the appropriate permissions.

### Workflow:
1. **Clone the Repository**:
   - Use the command `git clone <repository-url>` to clone the Git repository. This action provides you access to the folder hierarchy, metadata, and URL references in the data package.

2. **Resolve Data**:
   - If you have been granted **read permissions** in the repository, you can utilize Git Annex to selectively download the data files you require:
     - Run `git annex get <file>` to download a specific file.
     - Run `git annex get <folder>` to download all files in a folder.
     - Run `git annex get .` to download the entire dataset.

3. **Add Contributions** (if you have write permissions):
   - Contribute by adding new data references, files, or documentation (e.g., updated `README.md` files) to the repository. Push your changes back for others to utilize.

### Benefits:
- **Selective Data Retrieval**: Download only the data you need, optimizing storage and bandwidth usage.
- **Full Collaboration Support**: Contribute additional files or updates to the repository, enhancing the dataset with more context or metadata.
- **Leverage GitHub/GitLab Permissions**: Interact with the repository using standard GitHub/GitLab infrastructure, benefiting from familiar permission controls for secure access.
