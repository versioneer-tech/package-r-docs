# Workflows

`packageR` supports various personas, each with specific workflows designed to fit their roles and responsibilities.

## 1. Data Curator
As a **Data Curator**, your responsibility is to manage and organize datasets by referencing external files stored in cloud platforms. You create a well-structured hierarchy of data assets and can include documentation such as a `README.md`. Once your data is organized, you share these data packages to ensure easy access without the need for proprietary infrastructure.

### Key Responsibilities:
- Organize and reference data stored in cloud platforms.
- Add metadata and documentation to the data packages.
- Share data packages with relevant stakeholders.

---

## 2. Data Governance
As part of the **Data Governance** team, you oversee access management for both cloud storage and the data packages shared with users. You ensure that appropriate permissions are granted and maintained to manage secure and compliant data access.

### Key Responsibilities:
- Manage connections to cloud storage.
- Set or oversee access controls for shared data packages.

---

## 3a. Customer
As a **Customer**, you download data for initial inspection and then integrate it into your operations. You begin by selectively downloading the data you need, and later leverage bulk download capabilities to acquire all necessary assets. You interact with curated datasets stored in repositories for more efficient consumption.

### Key Responsibilities:
- Download and inspect data.
- Integrate the data into your operational environment.

## 3b. Data Scientist & Collaborator
As a **Data Scientist** or **Collaborator**, you work with curated datasets in repositories, utilizing tools like `dvc` or `git annex` to selectively download the necessary data. With proper permissions, you can also contribute new data, files, or documentation to the repository, collaborating seamlessly within GitHub or GitLab.

### Key Responsibilities:
- Stage shared assets in Git repositories.
- Contribute new data, files, or documentation to the repository.
- Collaborate within GitHub/GitLab using familiar tools and workflows.
