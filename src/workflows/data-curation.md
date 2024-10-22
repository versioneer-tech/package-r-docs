# Data Curator

As a **Data Curator**, you play a vital role in assembling and organizing datasets. With `packageR`, you can efficiently curate data by referencing external files (objects stored in cloud storage like S3, GCS, etc.) and arranging them into meaningful folder hierarchies within a Git-Repository. Here’s a step-by-step guide on how to leverage `packageR` for your curation tasks:

### Tasks and Responsibilities:
- **Curate Data**: Organize data from multiple external sources, including various cloud storage buckets or URLs.
- **Reference External Data**: Register external data files (URLs pointing to objects in different clouds) without storing the files themselves in the Git-Repository.
- **Add Additional Documentation**: Include metadata or supporting files, such as `README.md`, to describe the dataset and its usage.
- **Sync with Git-Repositories**: Sync your curated folder structure, metadata, and URLs as data package to a Git-Repository (e.g., GitHub or GitLab).

### Workflow:
1. **Reference External Data**: 

     - Use the `packageR` UI (or run `git annex addurl <url>`) to link data objects from various cloud storage services.
     - Assemble the referenced URLs into a clear folder hierarchy to organize your data package.

2. **Add Metadata**:

     - Incorporate additional files like `README.md` or other documentation to provide context and describe the data package for collaborators.

3. **Sync with Git**:

     - Use the `packageR` UI (or run corrsponding `git` commands) to push your changes to a Git-Repository, ensuring that all metadata and URL references are included.

### Benefits:
- No proprietary infrastructure is required for storing or hosting data packages—everything is managed through your Git-Repository.
- Full control over the organization of external data sources.
- The ability to add non-data files like documentation to enhance understanding and collaboration.
