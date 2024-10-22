# Data Sharing

Data sharing in **packageR** is designed to be intuitive and efficient, enabling users to seamlessly share curated datasets with others. The sharing mechanism is facilitated directly through the **packageR UI**, allowing users to generate presigned URLs for specific data files or entire datasets. This process enhances accessibility while maintaining security and control over the data.

### How It Works

1. **Access the UI**:
   - Users can navigate to the **packageR UI** to manage their curated datasets. The interface provides options to view the data package structure and access metadata associated with the datasets.

2. **Generate Presigned URLs**:
   - Instead of directly browsing and downloading content, users can opt to generate presigned URLs for the data files they wish to share. This allows others to access the data securely without exposing the actual storage locations.
   - Users can select the specific files or folders they want to share and initiate the URL generation process.

3. **Share for Offline Download**:
   - The generated presigned URLs can be used for offline downloading of files. These URLs can be accessed via command-line tools like `curl` or `wget`, making it easy to retrieve data without needing to log into the UI.
   - Each presigned URL is temporary and grants access only to the designated files, ensuring that data remains secure and controlled.

### Benefits:
- **Secure Access Control**: Presigned URLs provide a secure way to share data without exposing the underlying object storage details.
- **Convenient Offline Access**: Users can easily download datasets using familiar command-line tools, streamlining the workflow for data retrieval.
- **Flexibility**: The ability to generate URLs on-demand allows for tailored sharing, giving users control over what data is shared and with whom.

This mechanism not only enhances data accessibility but also ensures that data governance principles are upheld, allowing for effective collaboration while safeguarding sensitive information.
