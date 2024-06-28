# Home Keycloak


This project provides an identity server for use in a home network. 

## Quickstart

Copy `.env.example` to `.env` and set the desired values:

```bash
cp -n .env.example .env
````

Build the containers:

```bash
docker compose build --no-cache
```

Visit the site at `http://localhost:8080` and login with the credentials you defined in `.env`.

## Configuring a Systemd Service

A service template is provided that you can install on a server. This will define a service named `keyclock` that will start automatically when the system boots:

```bash
./bin/install-keyclock-service.sh
```

Start, stop, reload and service status can be managed with:

```bash
sudo systemctl start keyclock
sudo systemctl stop keyclock
sudo systemctl reload keyclock
sudo systemctl status keyclock
```
