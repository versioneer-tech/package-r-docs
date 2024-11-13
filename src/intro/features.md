# Key Features

`packageR` builds on established practices and integrates seamlessly with popular open-source tools, enabling data package management and sharing without specialized infrastructure. This flexibility enhances standard workflows with functionality that:

- **Unifies the creation of presigned URLs** for diverse object storage platforms, such as AWS S3, MinIO, and Ceph RadosGW. It supports both private link URLs or explicit identity-based access grants through your chosen Identity Provider, delivering secure and adaptable access control.

- **Simplifies data packaging** by offering a unified view of all data assets, even when spread across multiple storage locations. Through symbolic link-like “pointer” files, `packageR` streamlines data dissemination and staging, automatically translating these pointers for client tools as needed. This allows for efficient bulk (fully resolved) or selective (streamed) data access.

## How `packageR` Helps

`packageR` incorporates the following capabilities:

### 1. Streamlined Data Package Generation

`packageR` allows you to easily connect storage sources (like object storage buckets) to gain a comprehensive overview of your data assets. By mimicking simple copy operations, `packageR` creates symbolic link-like “pointer” files to build organized data package hierarchies that can then be shared.

**Benefit**: No actual data is duplicated; instead, it’s a pure metadata operation using familiar file system operations.

### 2. Operates without Proprietary Infrastructure

`packageR` works on top of standard commodity object storage, compatible with a wide array of OpenID Connect Identity Providers. This allows you to work where storage is most cost-effective, without the need to transfer data, and you retain control over data sharing.

**Benefit**: Continue using established storage solutions like AWS S3 or MinIO and share data seamlessly with external providers like GitHub or internal users via your enterprise SSO system.

### 3. Simple and Secure Data Sharing via Git

`packageR` supports sharing data packages through private link URLs or by selecting specific users or teams within your connected security realm, following familiar Git-based workflows. Shared folders can contain static data packages with any number of assets or dynamic, live sources, with consumption managed through presigned URLs.

**Benefit**: Apply granular permissions to share exactly what you want, without complex IAM policies or compromising security.

### 4. Transparent Data Resolution for Pointer Files

`packageR` enables clients to download pointer files for bulk resolution with tools like `wget` or `curl` and can stage data into repositories through integrations with `dvc` and `git annex`. Data is securely accessed via presigned URLs for authorized users, meaning repositories with pointer files can be shared without exposing underlying storage credentials.

**Benefit**: Automatically resolve pointer files securely using preferred client tools without compromising data security.

## How `packageR` Compares to Other Data Management Tools

`packageR` doesn’t replace existing tools but instead complements them for enhanced data collaboration. By integrating with `git annex`, `packageR` streamlines the data-sharing process and can be extended to work with `dvc`. This approach maintains the scalability of external storage solutions, unlike `git lfs`, which may face challenges with large file volumes, making `git annex` a more scalable choice.

## Only One Piece of the Larger Data Management Puzzle

`packageR` focuses on data sharing and distribution, while for end-to-end data product creation, we recommend exploring other solutions from [Versioneer](https://versioneer.at), which integrate seamlessly with commodity storage and provide:

- Stable snapshots to preserve data states for consistent access.
- Time-travel capabilities for navigating data versions.
- Data deduplication to optimize storage by removing redundancies.
- Automated data expiration to efficiently manage data lifecycles.

These capabilities integrate well with `git` workflows extended by `git annex` or `dvc`, enhancing your overall data management strategy.

## The Data Management Shared Responsibility Model

At `packageR`, we advocate for solid engineering practices as the foundation of successful data management. Adopting effective engineering methodologies allows operators to introduce the right tools to support large-scale, high-volume data management—a shared responsibility for achieving collaborative success and improved outcomes.

By embracing these principles, teams can leverage `packageR` alongside other tools to enhance their data management capabilities, driving greater collaborative success and better results.
