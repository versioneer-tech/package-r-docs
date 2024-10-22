# Architecture

The architecture of `packageR` is organized into three key components that work together to provide a seamless data management experience.

### 1. `packageR` UI:
The `packageR` UI mimics a file-browser interface, making it easy for users to manage and curate data packages. Users can browse connected object storage buckets, select external data, and register it within packages. Once the data is registered, the package can be directly published to a Git-Repository. While users can share data via presigned URLs, the preferred method for reproducibility is using the `git annex` workflow, which offers more robust version control and auditing.

### 2. `packageR` API:
The `packageR` API underpins much of the system's functionality, particularly for registering external data as pointer files via `git annex`. The API also handles secure data access by generating presigned URLs for approved users. When a data consumer requests a file, the API checks their permissions and either returns or redirects them to the presigned URL. This ensures data is securely accessible without requiring users to directly manage storage credentials.

### 3. `git annex` Workflow with `git`:
`packageR` integrates with any Git-compatible hosting service, such as GitHub or GitLab, to store and manage pointer files and other supplementary content like metadata or README files. The permissions model of `git`hosting services ensures that only authorized users can access or modify these files. By leveraging `git annex`, `packageR` provides a scalable and secure way to manage large datasets, allowing users to browse rep
