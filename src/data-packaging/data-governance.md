# Data Governance

As a **Data Governance** professional, your role is to control and manage access to the data package repositories. You determine whether the repository should be public or private and ensure that the correct permissions are in place for collaborators to access the data.

### Tasks and Responsibilities:
- **Manage Repository Access**: Control access to the Git repository by managing user permissions on platforms like GitHub or GitLab.
- **Decide on Public or Private Repositories**: Determine whether the repository should be public (visible to everyone) or private (restricted access).
- **Control Data Access via Permissions**: Ensure that users can only resolve actual data files if they have the correct permissions while still allowing access to metadata.

### Workflow:
1. **Repository Visibility**:
   - Set the repository to either public or private based on the data governance strategy.
   - **Public Repository**: Only metadata (folder structure and URLs) is visible to everyone. The actual data (external URLs) cannot be resolved unless users are granted explicit permissions.
   - **Private Repository**: Both metadata and file resolution are restricted to authorized users only.

2. **Manage Permissions**:
   - Utilize GitHub/GitLab’s built-in permission system to control who can access the repository.
   - Add users with at least **read permissions** if they need to resolve the data URLs (via Git Annex).
   - Users with **write permissions** can contribute to the repository by adding files, updating metadata, or referencing new data.

3. **Allow Selective Data Access**:
   - Users added to the repository can resolve URLs using `git annex get`, but they must have Git Annex installed to selectively download files, subfolders, or entire datasets.
   - Only those with proper permissions will be able to access the actual content behind the URLs.

### Benefits:
- Complete control over access to both the metadata and the actual data, utilizing existing GitHub/GitLab permission mechanisms.
- Enables fine-grained permissions: a public repository can display metadata while restricting access to the actual data files.
- No need for proprietary access control systems—everything is managed via GitHub/GitLab’s standard infrastructure.
