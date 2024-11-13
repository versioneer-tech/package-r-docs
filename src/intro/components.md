# Architecture

The architecture of `packageR` is organized into three key components, each designed to provide a seamless and secure data management experience.

### 1. `packageR` UI
The `packageR` UI features a file-browser interface, making it intuitive for users to manage and curate data packages. Users can navigate connected storage sources (e.g., object storage buckets), select individual data assets or folders (prefixes), and register them within packages. Once data is registered, it can be shared with selected audiences. The shared data can then be either downloaded directly or staged to a repository, allowing tools like `dvc` or `git annex` to provide robust version control and audit capabilities, ensuring reproducibility and data integrity.

### 2. `packageR` API
The `packageR` API provides the necessary file-system abstraction functionality, including registering external data as pointer files and managing secure data access. When a data consumer requests access, the API verifies their permissions and then generates a presigned URL, either redirecting or providing direct access. This setup ensures that data remains securely accessible without requiring users to handle storage credentials. Additionally, the API supports connecting and browsing various storage sources, making it a central point for secure data operations.

### 3. Source Management
`packageR` offers a unified view of all data assets across connected storage sources (e.g., object storage buckets) by utilizing file system mounts. Mounting methods are flexible, supporting widely-used options like FUSE with `s3fs`. For operation deployment scenarios using Kubernetes, the open-source tool [sourceD](https://github.com/versioneer-tech/source-d) can streamline the mounting process, which is also utilized by [Versioneer](https://versioneer.at) in operational management. For each mounted source, `packageR` requires necessary credentials to generate presigned URLs. This can be configured with direct secret mounts or through integrated `sourceD` tools, ensuring secure and efficient data access.
