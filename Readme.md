# Devcontainer Templates and Dockerfiles

This repository contains Dockerfiles and Devcontainer templates for setting up development environments.

## Repository Structure

```
Devcontainer_Templates/
    C_Dev/
        .devcontainer/
            .env
            compose.yaml
            devcontainer.json
    Py_Dev/
Dockerfiles/
    C_Dev_Dockerfile
    Py_Dev_Dockerfile
Readme.md
```

### Devcontainer_Templates

This directory contains templates for setting up development environments using Visual Studio Code's Devcontainer feature.

#### C_Dev

- **.devcontainer/**: Contains the configuration files for the C/C++ development environment.
  - **.env**: Environment variables for the Docker container.
  - **compose.yaml**: Docker Compose file to define and run multi-container Docker applications.
  - **devcontainer.json**: Configuration file for the Devcontainer.

#### Py_Dev

- Placeholder for Python development environment configuration.

### Dockerfiles

This directory contains Dockerfiles for building custom Docker images.

- **C_Dev_Dockerfile**: Dockerfile for the C/C++ development environment.
- **Py_Dev_Dockerfile**: Dockerfile for the Python development environment.

## Usage

### Setting Up the C/C++ Development Environment
1. Manually build the Docker image:
   ```sh
   cd Dockerfiles
   docker build -f C_Dev_Dockerfile -t cdev:latest .
   ```
2. Open Visual Studio Code.
3. Install the `Remote - Containers` extension.
4. Clone this repository.
5. Open the `Devcontainer_Templates/C_Dev` folder in Visual Studio Code.
6. When prompted, reopen the folder in the container.
7. User can move the .devcontainer folder to the root of any other project and reopen the VSCode in devcontainer.

### Customizing the Environment

You can customize the development environment by modifying the files in the `.devcontainer` directory.

- **compose.yaml**: Modify the services, volumes, and ports as needed.
- **devcontainer.json**: Add or remove extensions, change settings, and configure the remote user.

## Contributing

Feel free to submit issues and pull requests for new features, bug fixes, or improvements.

## License

This project is licensed under the MIT License.
