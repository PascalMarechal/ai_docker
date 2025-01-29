# Local AI

## Requirements

Before proceeding, ensure the following dependencies are installed:

1. **Docker**: Make sure Docker is installed on your system.
2. **NVIDIA Drivers**: Install appropriate NVIDIA drivers for your GPU.
3. **NVIDIA Container Toolkit**: Follow the installation guide [here](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html).

## Installation Steps

### 1. Install NVIDIA Container Toolkit

Follow the instructions from the official documentation to install the NVIDIA Container Toolkit on your system.

### 2. Verify Installation

After installation, verify by running:

```bash
nvidia-smi
```

This command checks if the NVIDIA drivers are functioning correctly.

## Running the Containers

Once all dependencies are installed and verified, you can start the containers using Docker Compose.

Run the following command to start your containers in detached mode:

```bash
docker compose up -d
```

This will initiate the containers as per your `docker-compose.yml` configuration.

## Troubleshooting

- **Check Logs**: If a container fails to start, inspect it with:
  
  ```bash
  docker logs <container-name>
  ```

- **Permissions**: Ensure you have the necessary permissions. Adding your user to the `docker` group might be required:

  ```bash
  sudo usermod -aG docker $USER
  ```

  Log out and back in for changes to take effect.

## Conclusion

By following these steps, you should be able to successfully set up and run your containers with GPU support using Docker Compose.
