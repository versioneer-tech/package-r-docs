# Workflows

`packageR` supports several personas, each with tailored workflows to suit their roles.

## 1. Data Curator
As a **Data Curator**, you manage and organize datasets by referencing external files stored in cloud platforms. Using `git annex`’s `addurl`, you build a structured hierarchy of data pointers and include essential documentation like a `README.md`. Once assembled, you can sync these data packages with a standard Git-Repository, ensuring broad accessibility without needing proprietary infrastructure.

### Key Responsibilities:
- Organize and reference cloud-stored data.
- Add metadata and documentation to data packages.
- Sync and manage data in Git-Repositories (e.g., GitHub, GitLab).

---

## 2. Data Governance
In the role of **Data Governance**, you manage access to both cloud storage and Git-Repositories, ensuring data security and appropriate permissions. You determine repository visibility (public or private) and enforce access policies. For public repositories, only metadata is visible, while actual data is restricted to authorized users with `git annex` installed.

### Key Responsibilities:
- Manage data connection and access within object storage.
- Set repository permissions and visibility.
- Control data access via GitHub/GitLab permissions and `git annex` resolution.

---

## 3. Data Scientist & Collaborator
As a **Data Scientist** or **Collaborator**, you engage with curated datasets, utilizing `git annex` to selectively download the data you need. With the appropriate permissions, you can also contribute new files, data references, or documentation to the repository, collaborating seamlessly within the GitHub or GitLab environment.

### Key Responsibilities:
- Clone repositories and download specific data using `git annex`.
- Contribute new data or documentation to the repository.
- Collaborate within GitHub/GitLab using familiar tools and workflows.
