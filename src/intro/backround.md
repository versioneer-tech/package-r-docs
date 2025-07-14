# Backround

`packageR` arose from the idea of simplifying work with different data and, above all, large data sets, whether you’re working alone or as part of a team. In real-world data workflows, teams face challenges not just from file sizes, but from the diversity of data formats, fragmented storage systems, and lack of user-friendly tools for secure sharing and collaboration.

If you work with any of the following types of data, `packageR` may be the solution you’ve been looking for:

### Text-Based Data Formats

- **Markdown** (.md)**:** Lightweight and human-readable, often used for documentation or notes.
- **JSON / YAML:** Common for structured data and configurations.
- **CSV / TSV:** Tabular data used across data science, statistics, and web tools.

`packageR` provides a built-in browser editor for quick viewing and editing of these formats.

### Binary, Office & Scientific Data

- **Excel** (.xlsx)**:** Widely used for reports, spreadsheets, and collaborative editing.
- **PDF, Word Documents:** Supplementary documentation and static exports.
- **RO-Crate Archives:** Machine-readable scientific data bundles with rich metadata.
- **High-Resolution Imagery & TIFFs:** Used in earth observation, geospatial analysis, and medical imaging.

Files can be previewed where supported or downloaded securely via presigned URLs. Metadata (e.g., metadata.json, manifests) is surfaced when available—without requiring a full download.

### Pointer Files & Packaged Archives

- **Pointer files** like .dvc, git-annex, or custom manifests enable lightweight local repositories while referencing remote data.  
  These pointers can be resolved into full datasets using familiar tools like wget, curl, dvc, or git annex.
- **RO-Crate, BagIt, Frictionless Data Packages:** Include structured metadata and are often FAIR-aligned.
- **ZIP, TAR, GZ:** Generic archive formats used for static sharing and reproducibility.

`packageR` tries to surface available metadata (like metadata.json, manifest files, or folder previews) directly in the browser. If full access is needed, it offers direct download paths from the underlying storage, without routing data through a server.

### Cloud-Native Formats at Scale

Cloud-native formats are purpose-built for scalable storage and efficient access. They support HTTP-based access, partial reads, and are designed to decouple compute from storage.

- **Parquet:** A columnar format ideal for large-scale analytics and integrated with Apache Arrow.
- **Cloud-Optimized GeoTIFF (COG):** Rearranged TIFF structure for range-based reads over HTTP, perfect for geospatial maps and tiles.
- **Zarr:** A protocol for chunked N-dimensional arrays using JSON metadata and binary chunks. Works with many storage backends (e.g., S3, GCS).

`packageR` integrates modern in-browser viewers that allow you to preview Parquet-backed tables, COG-based map tiles, and Zarr array slices directly, without downloading entire datasets. Wherever supported, previews are rendered seamlessly in the browser using lightweight, state-of-the-art libraries.

## What `packageR` Delivers

`packageR` helps teams work more efficiently with diverse and distributed datasets — without forcing major changes to infrastructure or workflows. It brings clarity, security, and performance to data management by:

- **Enabling secure access** via presigned URLs, without exposing storage credentials
- **Previewing and organizing data** across a wide range of formats and structures
- **Working with modern, cloud-native formats** through integrated viewers
- **Resolving pointer files and structured archives** without duplication or manual repackaging

Whether you're publishing open data, distributing scientific products, or managing internal cloud workflows, `packageR` is built to reduce friction and unlock the full potential of your data.