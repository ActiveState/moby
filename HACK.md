# Compression Level Hack

To build a `dockerd.exe` with compression level hardcoded to 0:

- `make win`
- `aws s3 cp bundles/binary/dockerd.exe s3://your/s3/bucket`
- Launch a Windows ECS-Optimized EC2 server
- Stop and remove the existing `dockerd.exe`
- Replace it with your `dockerd.exe` and restart the service

Alternatively, you can install the binaries following this document: https://docs.docker.com/engine/install/binaries/#install-server-and-client-binaries-on-windows
