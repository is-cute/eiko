# eiko

A (cute) modular music bot built on [Rawon](https://github.com/Clytage/rawon).

## 📃 About
Eiko is a fork of [Rawon](https://github.com/Clytage/rawon), a simple and modular Discord bot.

## 🌠 Deployment
> **Note**  
> You can find full deployment instructions in the [official repository](https://github.com/Clytage/rawon).

### Dependencies
Eiko requires [Node.js](https://nodejs.org) version `16.6.0` or higher.

Install the latest version using `curl`:
```
sudo apt install -y curl
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
```

### Building the Bot
Clone this GitHub Repository:
```
git clone https://github.com/is-cute/eiko eiko && cd eiko
```

Create a [`.env`](./.env_example) file in your working directory.
```
nano .env
```

> **Note**  
> Command modules can be removed under `src/commands`.

Build Eiko using your config:
```
npm install && npm run build && npm prune --production
```

### Starting the Bot
> **Note**  
> A sample `screen` script can be found in [start_eiko.sh](./start_eiko.sh).

To start the bot, run `npm start`.
