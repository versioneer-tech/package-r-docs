# Data Curator

As a **Data Curator**, you play a vital role in assembling and organizing datasets. With **packageR**, you can efficiently curate data by referencing external files (objects stored in cloud storage like S3, GCS, etc.) and arranging them into meaningful folder hierarchies within a Git repository. Here’s a step-by-step guide on how to leverage **packageR** for your curation tasks:

### Tasks and Responsibilities:
- **Curate Data**: Organize data from multiple external sources, including various cloud storage buckets or URLs.
- **Reference External Data**: Use `git annex addurl` to register external data files (URLs pointing to objects in different clouds) without storing the files themselves in the Git repository.
- **Add Additional Documentation**: Include metadata or supporting files, such as `README.md`, to describe the dataset and its usage.
- **Sync with Git Repositories**: Push your curated folder structure, metadata, and URLs to any Git repository (e.g., GitHub or GitLab). These repositories do not need to support Git Annex—**packageR** works out of the box with standard Git repositories.

### Workflow:
1. **Reference External Data**: 
   - Run `git annex addurl <url>` to link data objects from various cloud storage services.
   - Assemble the referenced URLs into a clear folder hierarchy to organize your data package.

2. **Add Metadata**:
   - Incorporate additional files like `README.md` or other documentation to provide context and describe the data package for collaborators.

3. **Sync with Git**:
   - Push your changes to a Git repository, ensuring that all metadata and URL references are included.
   - This can be done with a standard `git push`, as no Git Annex-specific support is needed on the repository (GitHub, GitLab, etc., work seamlessly).

### Benefits:
- No proprietary infrastructure is required for storing or hosting data—everything is managed through your Git repository.
- Full control over the organization of external data sources, allowing for flexibility in data management.
- The ability to add non-data files like documentation to enhance understanding and collaboration.
