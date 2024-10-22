# Key Features

## 1. Flexible Data Management with Git Annex 

packageR integrates the `git annex addurl` feature to register external data sources, creating lightweight pointers to data stored externally. These pointers are resolved when a user runs `git annex get`.

- Utilize packageR’s convenient tools (UI, API) for simplifying external data registration, but you can always revert to using Git Annex’s `addurl` directly.
- Requests are routed through a secure packageR API endpoint, which checks user permissions, allowing pointer files to be shared in Git while authorization is determined later during resolution.

## 2. No Proprietary Infrastructure

One of packageR's main advantages is its operation without proprietary infrastructure for data packages, relying on standard Git repositories and commodity object storage solutions like Amazon S3.

- There’s no need for a specialized Git hosting provider; data packages consist of Git Annex pointer files for all registered external data. These remain regular files, resolved on the client side via the Git Annex tool.
- You can organize your data package structure and include additional reference data or metadata files (e.g., `README.md`) as desired since it functions as a standard Git repository.

## 3. Simple and Secure Data Sharing via Git

Leverage the native authentication mechanisms of GitHub or GitLab.

- Sharing data with packageR is as straightforward as granting access to a Git repository. The decision to make it public or private lies entirely with your team.
- You can make a repository public while restricting data resolution (via Git Annex `get`) to certain users. Only those with at least read permissions can resolve the Git Annex pointer files using packageR endpoints.

## 4. Scalable, Flexible, and Secure Data Storage

packageR provides scalable and secure data storage by utilizing cloud-based object storage solutions, simplifying the management of large datasets.

- Data is stored in scalable, secure cloud storage like Amazon S3, minimizing the load on the Git repository when handling large datasets.
- packageR’s presigned URL mechanism ensures secure access, with only the Data Curator needing access to the storage credentials and packageR's backend methods for generating presigned URLs.
