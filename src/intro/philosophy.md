# Philosophy

packageR emphasizes the significance of sharing and collaboration to enhance efficiency, quality, and data reuse within Earth Observation (EO) platform ecosystems.

## 1. No Vendor Lock-In—Complete Flexibility

With packageR, you are not confined to any specific platform or proprietary solution for managing your data packages. By leveraging standard Git repositories, teams can operate within familiar environments like GitHub and GitLab. This flexibility grants teams full control over data storage and access.

## 2. Collaborative and Open Data Management

packageR fosters a collaborative environment where teams can work together seamlessly, utilizing the same tools they use for software development. Since the data package is stored in a Git repository:

- Teams can easily add supplementary files, such as README files, project documentation, or analysis scripts, directly to the repository.
- This enhances transparency and collaboration by providing context for the data while keeping the data package structure clear and organized.
- Contributors can engage with the repository in familiar ways, whether through GitHub's web interface, command-line tools, or integrated development environments (IDEs).

## 3. Access Control via GitHub/GitLab Permissions

By relying on GitHub or GitLab for access control, packageR enables effective user permission management at the repository level, offering several advantages:

- Public or private access: Teams can opt for public repositories to allow broad visibility while maintaining control over who can resolve actual data files by managing read, write, or admin permissions.
- Granular permissions: Permissions can be finely tuned for each repository. A user with read access can pull the repository and resolve referenced files, while users with higher permissions can contribute by adding files, making edits, or managing the repository itself.

## 4. Reproducibility and Version Control

By utilizing Git's native version control features, packageR ensures that every data package is versioned and easily traceable. This supports:

- Reproducibility: Data scientists can replicate experiments by accessing the exact version of a dataset used in previous analyses, ensuring consistent results.
- Data integrity: The version control system logs every change made to the repository, providing a complete audit trail of additions, updates, or removals, thereby enhancing data governance and reliability.

## 5. Scalable Data Access and Storage

packageR's architecture allows teams to scale without limitations:

- Object storage for large data: Actual data is stored externally in cloud-based object storage solutions, making it suitable for projects dealing with terabytes of data or more.
- Selective data access: With Git Annex, users can download only the specific files they need at any given time, optimizing both storage and bandwidth usage.
