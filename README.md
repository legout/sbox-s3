# SBOX-S3

SBOX-S3 is a self-hosted S3 object storage solution built using the S3 API from [SeasweedFS](https://seaweedfs.github.io/) 
and can be run on an inexpensive VPS like from [netcup](https://www.netcup.de/?ref=223843), 
[Hetzner](https://www.hetzner.com/cloud) or [contabo.com](https://contabo.com/en/vps/).

For storage space, any mountable remote storage can be used. I am using a [Hetzner Storagebox](https://www.hetzner.com/storage/storage-box).
The remote storage is mounted into the VPS using [Rclone](rclone.org). 
Thanks to Seaweedfs and Rclones clever caching, you get very fast S3 object storage that allows
you to store and retrieve data/objects in a scalable and cost-effective manner. 

## Prerequisites

To run SBOX-S3, you'll need the following:

- A VPS with at least 2 cores and 2GB of RAM. A VPS with a fast NVME SSD is recommended.
- A Hetzner Storagebox for storage or any remote storage supported by rclone. 
  
## Deployment

To deploy SBOX-S3, follow these steps:

1. Clone the SBOX-S3 repository.
2. Modify the `rclone.conf`file to configure your remote storage.
3. Modify the `s3.conf` file to configure your s3 credentials.
4. Modify the mount point in the `docker-compose.yml` file (`/data/s3:/data/s3`, `/data/cache:/data/cache`) and adjust them accordingly.


## Configuration

SBOX-S3 can be configured with the files `rclone.conf`  and `s3.conf`.



## Usage

Once SBOX-S3 is deployed, you can use the S3 API to interact with the object storage. Refer to the documentation for the seasweedfs S3 API for more information on how to use it.

## Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
