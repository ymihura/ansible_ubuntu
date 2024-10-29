# Static Server Setup with Ansible and Docker

## Requirements

### System Requirements
- **Docker:** Installed and running (version 20.10 or later).
- **Docker Compose:** Installed (version 1.29 or later).
- **Ansible:** Installed on the host machine (version 2.9 or later).

### Required Packages
The following packages should be installed on the system:
- **git**

---

## Installation Steps

1. Clone this repository.
2. Run `export USER_PASSWORD=${UBUNTU_USER_PASSWORD}; docker-compose up -d --build` from ubuntu directory to set up the test environment.
3. Apply the Ansible playbook from ansible folder using the created password:
`ansible-playbook -i hosts_ubuntu ubuntu.yml --ask-pass` 
4. You can access the static images at [http://localhost:80/images](http://localhost:80/images).

For additional configuration details, refer to the playbook and roles provided in the project.
