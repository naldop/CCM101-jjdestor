
# MinIO Deployment Documentation

## Docker Command Used

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  quay.io/minio/minio server /data --console-address ":9001"
```

We used the MinIO image from **Quay.io** instead of Docker Hub because the Docker Hub download showed an **"access denied"** error.

## Deployment Details

| Item             | Value         |
| ---------------- | ------------- |
| Web Console Port | 9001          |
| API Port         | 9000          |
| Container Name   | minio-server  |
| Bucket Name      | client-photos |

## Steps Taken

1. Opened a **KillerCoda Ubuntu Playground**.
2. Ran the Docker command to download and start MinIO.
3. Used `docker ps` to check if the MinIO container was running.
4. Opened **port 9001** using the **Traffic / Ports** tab.
5. Logged in to the MinIO web console using the username and password from the Docker command.
6. Created a bucket named **client-photos**.
7. Uploaded a sample file to the bucket.

## Environment Variables (`-e`)

* **`MINIO_ROOT_USER=cloudadmin`** – Sets the username for the MinIO administrator account.
* **`MINIO_ROOT_PASSWORD=CloudNova2026!`** – Sets the password for the administrator account.

The **`-e`** option is used to add settings to the MinIO container. MinIO uses these settings when it starts, so we do not need to create the administrator account manually.

These usernames and passwords are only for the lab. **They should not be used in a real production system.**

## Troubleshooting

* The first attempt failed because Docker Hub could not download `minio/minio` and showed an **"access denied"** error. We solved this by using `quay.io/minio/minio`.
* Another attempt failed because a container named **`minio-server`** already existed. We removed the old container using `docker rm -f minio-server` and ran the command again.

## Screenshots

* **`screenshots/minio-deployed.png`** – Shows the MinIO container running.
* **`screenshots/minio-bucket-upload.png`** – Shows the `client-photos` bucket with an uploaded file.
