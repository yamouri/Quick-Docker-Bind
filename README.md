# Quick Docker Bind9

This repository provides a simple setup for a recursive DNS server using Bind9, already configured and ready to use. Just run `sudo docker-compose up -d` and you will have a fully operational DNS server.

## What is Bind9?

Bind9 is one of the most widely used DNS (Domain Name System) server software. It can act as a recursive DNS server, resolving domain names by querying other DNS servers on behalf of clients. In this setup, Bind9 is configured to be a recursive resolver, which means it will follow the chain of DNS servers to resolve domain names from the root servers down to the authoritative server.

## Running the Bind9 Server

To get the server up and running, you simply need to use Docker Compose. This setup makes it incredibly easy to deploy and manage your DNS server without having to configure everything manually.

### Steps to Run:

1. Clone this repository:
    ```bash
    git clone https://github.com/yamouri/Quick-Docker-Bind-.git
    ```

2. Navigate into the repository directory:
    ```bash
    cd Quick-Docker-Bind-
    ```

3. Start the DNS server using Docker Compose:
    ```bash
    docker-compose up -d
    ```

That's it! Your Bind9 recursive DNS server is now running.

### Port Information

- **Port 53 (UDP/TCP)**: This is the default port for DNS traffic. Bind9 will listen on this port, both for UDP and TCP connections. Ensure that port 53 is open in your firewall settings for the server to function properly.

## Requirements

- Docker
- Docker Compose

## Additional Notes

- The configuration provided here is meant for a quick setup of a recursive DNS server, and it does not include advanced DNS features, it's just a project on my side.
- If you need to modify the deployment and DNS settings, feel free to edit the files under the bind-dns folder

