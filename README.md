# Home Lab v1 - Docker Configurations

Welcome to my first ever home lab project! This repository contains the configuration files and setup notes for my home lab, which is designed to be a reference for myself primarily, but also for others looking to build a similar setup. **Note:** This is a public reference and not an exact copy of my running configuration, for security reasons.

## Hardware
- **Device:** Microsoft Surface Laptop 2
- **OS:** Debian 13 (Trixie)
- **CPU:** 8th Gen Intel (4 cores)
- **RAM:** 8GB
- **Storage:** 250GB SSD + 1TB External SSD
- **Form Factor:** Sits closed in a drawer, running 24/7

## Management
- **Containerization:** Docker
- **Container Management:** Portainer

## Current Apps/Services
- **[Meet Homepage](https://gethomepage.dev/):** A dashboard for managing and monitoring your home lab services.

## Planned/Upcoming Services
- **Pi-hole:** Network-wide ad blocking + DDNS
- **Tailscale Exit Node:** Even though Tailscale is already in use, I may set up an exit node as a container
- **More apps/services to come!**

## Repository Structure
This repo contains the Docker Compose file(s) and configuration files for the services running in the home lab. All services are run as Docker containers.
```
/
└── docker_volumes/
  └── homepage/
    ├── docker-compose.yaml
    └── config/
      ├── bookmarks.yaml
      ├── docker.yaml
      ├── proxmox.yaml
      ├── services.yaml
      ├── settings.yaml
      └── widgets.yaml
```

- `docker-compose.yaml`: Main Docker Compose file for orchestrating containers
- `config/`: Configuration files for the "Meet Homepage" dashboard and other services

## Usage
This repository is intended as a reference for myself as I build out and up my home-lab, but for others as well looking to bootstrap their own environment at home. **Do not use these configs as-is for production or sensitive environments.**

1. Clone the repository
2. Review and modify the configuration files as needed for your environment
3. Deploy using Docker Compose:
   ```fish
   docker compose up -d
   ```

## Security Notice
Sensitive information (such as passwords, API keys, and internal network details) has been omitted. Always review and secure your own configurations before deploying.

## Contributing
Feel free to open issues or pull requests with suggestions for new services, improvements, or corrections!

## License
This project is open source and available under the MIT License.
