# Valkey Docker Setup Guide

Getting Valkey running in Docker is very similar to working with Redis. Here are the commands to get your environment set up and start playing with the CLI.

---

## 1. Install and Run Valkey

Pull the official image and start a container with the command below. It's named `my-valkey` with the default port `6379` mapped so you can access it from your host machine if needed.

```bash
docker run -d --name my-valkey -p 6379:6379 valkey/valkey:latest
```

---

## 2. Check Version

To verify the installation and see the version info without entering the console, use the following `exec` command:

```bash
docker exec -it my-valkey valkey-server --version
```

Alternatively, get a more detailed report (including the Valkey version and underlying Redis compatibility version) by running:

```bash
docker exec -it my-valkey valkey-cli info server | grep version
```

---

## 3. Enter the Valkey Console

To enter the interactive CLI and start running commands like `SET`, `GET`, or `PING`:

```bash
docker exec -it my-valkey valkey-cli
```

Once inside, you'll see a prompt like `127.0.0.1:6379>`. Test it with the following commands:

| Command             | Expected Output |
|---------------------|-----------------|
| `ping`              | `PONG`          |
| `set test "hello"`  | `OK`            |
| `get test`          | `"hello"`       |
