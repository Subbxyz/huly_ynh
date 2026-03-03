# ⚠️ Very Heavy Application

Before you install Huly, please read the following:

- **14 Docker Containers:** Huly deploys 14 interlinked microservices to work.
- **High Resource Usage:** The architecture includes CockroachDB, Redpanda, ElasticSearch, and Minio. It requires a significant amount of RAM (absolute minimum 4GB, recommended 8GB-16GB+).
- **Downtime on Backup:** Since this package backs up databases using filesystem snapshots, all Huly containers must be gracefully stopped during the backup procedure. This will result in a couple minutes of downtime during `ynh_backup`.
- **User Management:** This package does not hook into YunoHost LDAP or SSO.
- **Docker Wrapper:** Huly is not installed bare-metal; you will see it occupy disk-space via Docker volumes inside your `data_dirs`.

Proceed only if you understand and have checked your system's `free -m`.
