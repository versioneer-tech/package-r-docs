# Personas

## 1. Data Curator
The **Data Curator** is responsible for organizing and assembling datasets by referencing external files stored across various cloud platforms. Utilizing Git Annex’s `addurl`, they create a structured folder hierarchy of data links while also including relevant metadata and documentation (e.g., `README.md`). The curated data package is then synced with any standard Git repository (e.g., GitHub or GitLab), eliminating the need for specialized infrastructure.

### Key Responsibilities:
- Organize and curate data by referencing external cloud objects.
- Add additional documentation (e.g., `README.md`).
- Sync and manage data in standard Git repositories (GitHub, GitLab, etc.).

---

## 2. Data Governance
The **Data Governance** professional oversees repository access, ensuring data security and appropriate permissions. They determine whether the repository is public or private and control who can resolve the actual data. In public repositories, only metadata is visible to everyone, while actual data is accessible solely to users with read permissions and Git Annex installed.

### Key Responsibilities:
- Manage Git repository visibility (public or private).
- Control access through GitHub/GitLab permissions.
- Ensure only authorized users can resolve the data via Git Annex.

---

## 3. Data Scientist/Collaborator
The **Data Scientist** or **Collaborator** engages with the curated datasets, utilizing Git Annex to selectively download the data they require. They can also contribute additional files, data references, or documentation to the repository if they possess the appropriate permissions.

### Key Responsibilities:
- Clone repositories and selectively download data using Git Annex.
- Add contributions (new data, documentation) to the repository.
- Collaborate within the existing GitHub/GitLab ecosystem using standard tools and permissions.
