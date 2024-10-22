# Key Features

`packageR` incorporates the following capabilities:

## 1. Flexible Data Management with `git annex` 

`packageR` integrates the `git annex addurl` feature to register external data sources for published data, creating lightweight pointers to externally stored data. These pointers are resolved when a consumer runs `git annex get`.

- `packageR`’s tools (UI, API) simplify external data registration, but producers can revert to `git annex addurl` directly.
- Data consumption routes through a secure `packageR` API endpoint, checking user permissions, allowing pointer files to be shared without exchanging storage credentials.

**Benefit**: Full reproducibility and provenance with common `git`flows ensure audit trails for better data governance and reliability.

## 2. No Proprietary Infrastructure

`packageR` operates without proprietary infrastructure, using standard Git-Repositories and commodity object storage like Amazon S3.

- No need for a specialized `git`hosting provider; data packages include `git annex` pointer files resolved client-side.
- Organize data package structures with additional reference or metadata files in a standard Git-Repository.

**Benefit**: Teams can work in familiar environments like GitHub and GitLab, providing transparency and utilizing well-established tools and principles.

## 3. Simple and Secure Data Sharing via Git

`packageR` leverages the native authentication mechanisms of GitHub or GitLab.

- Data sharing is as simple as granting access to a Git-Repository, with your team deciding on public or private access.
- Public repositories can restrict data resolution (via `git annex get`) to specific users.

**Benefit**: Granular permissions can be finely tuned, allowing users with read access to pull and resolve files, while others can contribute by managing or editing the repository.

## 4. Flexible Data Storage

`packageR` supports scalable and secure data storage through cloud-based object storage solutions.

- Data is stored in scalable cloud storage like S3, reducing load on Git-Repositories when handling large datasets.
- `packageR`’s presigned URL mechanism ensures secure access, with only the Data Curator needing storage credentials.

**Benefit**: `git`hosting and data storage are separated, allowing for independent scaling. Data consumers can resolve only the files they need, optimizing storage and bandwidth usage.
