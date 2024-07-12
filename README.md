# d17 OpenResty

## Description

Web server for personal use

## How to Run

1. Open `terminal` and `cd` to project root path

2. Run `docker-compose` commands
```
docker-compose build

docker-compose up -d
```

## Useful Commands

```
# Stop the service
docker-compose down

# Reload settings
docker-compose exec openresty openresty -s reload

# Browse server directories
docker-compose exec openresty sh

# Tail access/error logs of nginx
docker logs -f openresty
```

## Project Structure
```
openresty
├── env
│   └── settings.env                  # Contains setting values
├── nginx
│   ├── conf.d
│   │   ├── locations
│   │   └── servers
│   │       └── default.conf          # Default server and upstream setting
│   ├── lua
│   └── nginx.conf                    # Root setting of the server
├── .gitignore
├── docker-compose.yaml
├── Dockerfile.openresty
└── README.md
```
