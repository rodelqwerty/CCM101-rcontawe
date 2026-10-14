# Checkpoint 5 - Technical Documentation

## 1. Docker Command Used to Deploy the MinIO Server

The following Docker command was used to download and deploy the MinIO server in the KillerCoda Ubuntu environment.

```bash
docker pull pgsty/minio

docker run -d -p 9000:9000 -p 9001:9001 --name minio-server -e "MINIO_ROOT_USER=cloudadmin" -e "MINIO_ROOT_PASSWORD=CloudNova2026!" pgsty/minio server /data --console-address ":9001"
```

The `docker pull` command downloads the MinIO image, while the `docker run` command creates and starts the container. Port 9000 is used for the S3 API, and port 9001 is used for the web console.

## 2. Port Number Used to Access the Web Console

The MinIO web console uses **port 9001**.

To access it, I opened the Traffic / Ports section in KillerCoda and forwarded port `9001`. I then accessed the MinIO web console through the generated URL and logged in using the configured credentials.

- **Web Console Port:** `9001`
- **S3 API Port:** `9000`

## 3. Bucket Created

I created a bucket named **`client-photos`** using the MinIO web console.

The bucket is configured as private and is intended to store photos and other media files for the client's photo-sharing application.

The following sample files were uploaded to verify that the bucket was working:

- `App Instructions.txt`
- `Reflection.webp`

## 4. Explanation of the -e Flags (Environment Variables)

The `-e` flags in the Docker command set environment variables inside the MinIO container. These variables configure the root account credentials when the server starts.

- **`-e "MINIO_ROOT_USER=cloudadmin"`** sets the MinIO administrator username to `cloudadmin`.
- **`-e "MINIO_ROOT_PASSWORD=CloudNova2026!"`** sets the password for the MinIO root account.

These environment variables allow me to configure the login credentials directly in the Docker command instead of manually editing configuration files inside the container.

## Conclusion

I successfully deployed the MinIO object storage server using Docker in KillerCoda. I used port 9001 to access the web console, created the private `client-photos` bucket, and uploaded sample files. The environment variables configured the administrative username and password required to access and manage the MinIO server.
