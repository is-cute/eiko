# eiko

A (cute) modular music bot powered by [Rawon](https://github.com/Clytage/rawon).

## 📃 About

eiko is a fork of [Rawon](https://github.com/Clytage/rawon), a simple and modular Discord bot project.

This repository is used to control updates and features for customized instances.

## 🌠 Deployment

You can find full deployment instructions in the [official repository](https://github.com/Clytage/rawon).

### Dependencies

Rawon requires [Node.js](https://nodejs.org) version `16.6.0` or higher.

Install the latest version using `curl`:

```sh
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
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

A sample `screen` script can be found [here](./start_eiko.sh_example).

To start the bot, run `npm start` in your terminal.

### Developer

> [!IMPORTANT]
> `eval` requires debug mode to be turned on by setting `DEBUG_MODE` in your [`dev.env`](./dev.env_example).

Erase cached slash commands by running the following with `eval`:

```java
client.application.commands.set([]);
```
