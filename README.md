# About

This project is build to install WordPress with NGINX and PhpMyAdmin using docker-compose.

# How to start the project

1. Register a new hostname entry in the hosts file (`/etc/hosts`)

```sh
local.wp.com	 127.0.0.1
```

2. Create a copy of the example env file:

```sh
cp .env.example .env
```

3. Start containers
   Start containers with the `-d` flag to run all containers in the background:

```sh
docker-compose up -d
```

In your web browser, navigate to `http://local.wp.com` to set up a WordPress page. You can also reach the PhpMyAdmin interface at `http://local.wp.com/pma/`

# Stop all containers

```sh
docker-compose down
```

To remove all named volumes and completely all containers including orphaned docker containers of the docker-compose file you can run the following command:

```sh
docker-compose down --volumes --remove-orphans
```
