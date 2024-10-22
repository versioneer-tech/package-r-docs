# Architecture

The architecture of **packageR** is organized into three main components:

- **packageR UI**:  
  The **packageR UI** serves as the primary entry point for users. This web portal is designed to simplify the discovery, browsing, reviewing, and downloading of services, code, AI models, and datasets. Users can interact with a user-friendly interface to select and explore large object storage buckets and utilize the "Register External Data" workflow to incorporate objects referenced in a package. Additionally, users can publish packages to a Git repository directly from the UI.

- **packageR API**:  
  The **packageR API** is the backbone that supports the functionalities of the portal. It provides the convenience of registering external data through Git Annex directly, streamlining the process for users. The API also includes the capability to presign URLs, which allows for secure access to data. If a user is authorized, the API will redirect them to the presigned URL, ensuring that access to the data is controlled and secure.

- **Git Hosting Instance**:  
  A **Git Hosting Instance**, which can refer to any Git-compatible hosting service (such as GitHub or GitLab), is essential for managing user permissions and data access. This instance allows users to browse and clone repositories, enabling access to metadata and non-annexed files, such as README documents. If authorization is granted, users can utilize Git Annex functionalities. The permissions in this instance are crucial for maintaining the security and accessibility of the packages while allowing users to explore available resources freely.
