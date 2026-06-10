# SecurePortal

A three-page authenticated portal with admin and employee dashboards, served via Docker + Nginx.

## Files

| File | Purpose |
|------|---------|
| `login.html` | Login page — authenticates users and redirects to the correct dashboard |
| `admin_dashboard.html` | Admin-only dashboard — blocked if accessed without admin session |
| `employee_dashboard.html` | Employee-only dashboard — blocked if accessed without employee session |
| `Dockerfile` | Builds a lightweight nginx:alpine image |
| `docker-compose.yml` | Runs the container on port 8080 |
| `nginx.conf` | Custom nginx server block |

## Credentials

| Role | Username | Password |
|------|----------|----------|
| Admin | `admin` | `admin123` |
| Employee | `employee` | `emp123` |

## Run with Docker Compose (recommended)

```bash
# Build and start
docker compose up --build -d

# Open in browser
open http://localhost:8080

# Stop
docker compose down
```

## Run with plain Docker

```bash
# Build
docker build -t secureportal .

# Run
docker run -d -p 8080:80 --name secureportal secureportal

# Stop
docker stop secureportal && docker rm secureportal
```

## Access Control

- **Login page** → redirects already-logged-in users to their dashboard automatically.
- **Admin dashboard** → if session role is not `admin`, user is immediately sent back to login.
- **Employee dashboard** → if session role is not `employee`, user is immediately sent back to login.
- **URL tampering** → navigating directly to a dashboard without a valid session redirects to login.
- Sessions are stored in `sessionStorage` (cleared automatically when the browser tab is closed).

## Development (live reload)

The `docker-compose.yml` mounts the HTML files as read-only volumes, so editing a file on your machine updates it instantly — no rebuild needed.
