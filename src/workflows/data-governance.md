# Data Governance

As a **Data Governance** professional, your main role is to manage and regulate access to both cloud storage and data package repositories. You decide if a repository should be public or private, ensuring the necessary permissions are in place for secure collaborator access. Furthermore, you oversee which object storage solutions are connected to the `packageR` UI for data package curation.

### Tasks and Responsibilities:
- **Manage Connected Object Storage**: Select which cloud object storage services integrate with the `packageR` UI for data curation.
- **Manage Repository Access**: Control access to the Git-Repository by managing user permissions on platforms like GitHub or GitLab.
- **Decide on Repository Visibility**: Determine whether the repository is public (accessible to everyone) or private (restricted access).
- **Control Data Access via Permissions**: Ensure users can only resolve actual data files if they have the appropriate permissions while allowing access to metadata.

### Workflow:
1. **Object Storage Access**:
     - Configure access to specific object storage buckets to be integrated with `packageR` tools.

2. **Repository Visibility**:
     - Set the repository as public or private based on your data governance strategy.
     - **Public Repository**: Only metadata (folder structure and URLs) and supplementary files are visible to all users, while actual data (external URLs) cannot be accessed unless explicit permissions are granted.
     - **Private Repository**: Both metadata and data resolution are restricted to authorized users only.

3. **Manage Repository Permissions**:
     - Utilize the built-in permission system of GitHub/GitLab to control repository access.
     - Provide users with at least **read permissions** to allow them to resolve pointer files (via `git annex`) and access the underlying content behind the URLs.
     - Users with **write permissions** can contribute to the repository by adding files, updating metadata, or referencing new data.

### Benefits:
- Removes the need for proprietary access control systems, as everything is managed through standard infrastructure.
- Complete control over access to both metadata and actual data, leveraging GitHub/GitLab's existing permission systems.
- Enables fine-grained permissions: public repositories can display metadata while restricting access to the actual data files.
