# 🚀 Docker Databases Setup for Local Development

A ready-to-use Docker Compose configuration to spin up multiple databases locally for development purposes.  
No need to install database engines directly on your machine!

## 📦 Included Databases

- **Microsoft SQL Server** (2022)
- **MySQL** (8.0)
- **PostgreSQL** (16)
- **MongoDB** (7)

Easily run and manage multiple databases in isolated containers.

---

## 🧩 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/jeison-araya/docker databases.git
cd docker databases

## 🧩 Running Specific Services

You don’t have to run all databases at once!
You can start individual services or a selection of them

### Run a single database:

```bash
docker compose up -d postgres
```

Example for MySQL:

```bash
docker compose up -d mysql
```

### Run multiple specific databases

```bash
docker compose up -d mysql mongo
```

###  Run all databases

```bash
docker compose up -d
```

### Stop a specific database

```bash
docker compose stop postgres
```

### View logs for a specific database

```bash
docker compose logs -f mongo
```

Use `docker compose ps`to see the status of all running containers.

---

## ⚙️ Services & Access

| Service    | Host      | Port  | Username | Password            | Notes                         |
| ---------- | --------- | ----- | -------- | ------------------- | ----------------------------- |
| MSSQL      | localhost | 1433  | sa       | YourStrong!Passw0rd | Connect using SSMS or DBeaver |
| MySQL      | localhost | 3306  | user     | userpassword        |                               |
| PostgreSQL | localhost | 5432  | user     | userpassword        |                               |
| MongoDB    | localhost | 27017 | user     | userpassword        |                               |

---

## 📝 Environment Variables

You can customize the database credentials by editing the `docker-compose.yml` file or by using environment files.  
It's recommended to copy `.env.example` and create your own `.env`.

```bash
cp .env.example .env
```

---

## 🛠️ Requirements

- Docker
- Docker Compose

Make sure Docker is installed and running on your machine.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
