# eiko

A (cute) modular music bot powered by [Rawon](https://github.com/stegripe/rawon).

## 📃 About

eiko is a fork of [Rawon](https://github.com/stegripe/rawon), a simple and modular Discord bot project.

This repository is used to control updates and features for customized instances.

## 🌠 Deployment

You can find full deployment instructions in the [official repository](https://github.com/stegripe/rawon).

### Prerequisites

eiko recommends [Node.js](https://nodejs.org) version `20.0.0` or later.

You can install the latest LTS version using [NodeSource](https://github.com/nodesource/distributions):

```sh
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
```

### Building

Clone this GitHub Repository:

```sh
git clone https://github.com/is-cute/eiko eiko && cd eiko
```

> [!NOTE]
> Command modules can be optionally removed under `src/commands`. *Modules that you wish to remove must be done prior to building.*

Create a [`.env`](./.env_example) file in your working directory. Build Rawon using your config:

```sh
npm install && npm run build && npm prune --production
```

### Usage

Enter your working directory and start eiko using `npm`:

```sh
npm start
```

### Scripts

Sample scripts are available in eiko's root directory:

- [`setup_eiko.sh`](./setup_eiko.sh_example) - Update and build script
- [`start_eiko.sh`](./start_eiko.sh_example) - Start script using `screen`

### Developer

> [!IMPORTANT]
> `eval` requires debug mode to be turned on by setting `DEBUG_MODE` in your [`dev.env`](./dev.env_example).

#### Cleaning Slash Commands

Erase cached slash commands by running the following with `eval`:

```java
client.application.commands.set([]);
```
