# Ansible Role: jeffhung.docker

Ansible playbook to use Docker CE on CentOS/Ubuntu Linux.

Install this playbook:

	ansible-galaxy install jeffhung.docker


## Role Variables

### `docker_variant` (optional)

Select the Docker variant from one of the following:

- `enterprise` (n/a)
- `stable`
- `edge` (n/a)
- `cloud` (n/a)

Default: `stable`

Docker is available in multiple variants:

- Docker Enterprise Edition (Docker EE) is designed for enterprise
  development and IT teams who build, ship, and run business critical
  applications in production at scale. Docker EE is integrated, certified,
  and supported to provide enterprises with the most secure container
  platform in the industry to modernize all applications.

- Docker Community Edition (Docker CE) is ideal for developers and small
  teams looking to get started with Docker and experimenting with
  container-based apps. Docker CE is available on many platforms, from
  desktop to cloud to server. Docker CE is available for macOS and Windows
  and provides a native experience to help you focus on learning Docker. You
  can build and share containers and automate the development pipeline all
  from a single environment.

  Docker CE gives you the option to run stable or edge builds.

  - Stable builds are released once per quarter.
  - Edge builds are released once per month.

- Docker Cloud is a platform run by Docker which allows you to deploy your
  application using multiple cloud providers such as Digital Ocean, Packet,
  SoftLink, or to bring your own device.

See: https://docs.docker.com/engine/installation/#docker-variants

### `docker_manage_as_nonroot` (optional)

Manage Docker as a non-root user?

Default: `true`

Warning: The docker group grants privileges equivalent to the root user. For
         details on how this impacts security in your system.
    See: https://docs.docker.com/engine/security/security/#docker-daemon-attack-surface


### `docker_install_method` (optional)

Select the method for installing docker. Could be:

- `repository`
- `package` (n/a)

Default: `repository`

## License

BSD

