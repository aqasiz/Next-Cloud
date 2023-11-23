# Nextcloud with MariaDB Docker Compose Configuration

## Overview

This Docker Compose configuration sets up a Nextcloud instance connected to a MariaDB database. It provides a convenient way to deploy and run Nextcloud with a database backend using Docker.

## Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Getting Started

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/aqasiz/Next-Cloud.git
    ```

2. Navigate to the project directory:

    ```bash
    cd Next-Cloud
    ```

3. Run the Docker Compose command to start the services:

    ```bash
    docker-compose -f next-cloud.yml up -d
    ```

    This will create and start the Nextcloud and MariaDB containers in the background.

4. Access Nextcloud by opening your browser and navigating to [http://localhost:8080](http://localhost:8080). Log in with the provided credentials.

## Configuration

### MariaDB Configuration

- **Root User**: `root`
- **Root Password**: `my-secret-pw`
- **Database Name**: `nextcloud`
- **Database User**: `nextcloud`
- **Database Password**: `my-secret-pw`

### Nextcloud Configuration

- **Web Address**: [http://localhost:8080](http://localhost:8080)
- **Database Host**: `db`
- **Database Name**: `nextcloud`
- **Database User**: `nextcloud`
- **Database Password**: `my-secret-pw`

## Volumes

- **db**: MariaDB data volume
- **nextcloud**: Nextcloud data volume

## Additional Information

- The containers will automatically restart in case of failure (`restart: always`).
- Ensure that the specified ports (8080 for Nextcloud) are not already in use on your system.
- **User**: `nextcloud`
- **Password**: `my-secret-pw`

