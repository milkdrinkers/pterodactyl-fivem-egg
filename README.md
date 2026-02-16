<div align="center">
  <h1>FiveM/RedM Server Egg</h1>

  *A Pterodactyl egg for [FiveM](https://fivem.net/) & [RedM](https://redm.net/) which includes features like updating server artifacts and cloning/pulling server files from git.*

<br>
<div>
<a href="https://github.com/milkdrinkers/pterodactyl-fivem-egg/issues">
    <img alt="GitHub Issues" src="https://img.shields.io/github/issues/milkdrinkers/pterodactyl-fivem-egg?style=for-the-badge&labelColor=141417">
</a>
<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/milkdrinkers/pterodactyl-fivem-egg?style=for-the-badge&labelColor=141417">
<a href="https://discord.milkdrinkers.dev">
    <img alt="Discord Server" src="https://img.shields.io/badge/-DISCORD-5865F2?style=for-the-badge&logo=discord&logoColor=ffffff&color=%235865F2">
</a>
</div>
</div>

---

## 🌟 Features

- Easy server updating by using the reinstall button.
- Git support, clone and fetch your server files from a Git repository.
- TxAdmin support.

---

## ❓ FAQ

> Why create this, what is it for?

This is simply a fork/edit of [parkervcp](https://github.com/parkervcp)'s FiveM egg found [here](https://github.com/pelican-eggs/games-standalone/blob/main/gta/fivem), which I use for my FiveM servers.

> Why should I use this over other FiveM eggs?

This fork includes an easy way of updating server artifacts, automatic pulls from private git repositories on server startup into the `resources` folder, and lots of pre-defined convars that can be changed on your servers `Startup` page. I needed this for my servers and figured I'd share it.

> I have a question/could you help me set this up?

Will I help you set this up? No. However if you have any questions I'm usually available in my friends FiveM oriented [discord server](https://discord.milkdrinkers.dev), and would be happy to answer any question you may have.

---

## 📦 Guides

### Updating Server Artifact

If you want to update your servers artifact I've provided an easy way for doing so. (*This will delete the existing `/alpine/` directory and replace it with the newly downloaded one.*)

1. On your servers `Startup` page, set the `FXServer Version` to the version you want to update to.

    The valid versions are:
    - `latest` - (*Default*) *Downloads the latest available artifact.*
    - `recommended` - *Downloads the recommended artifact.*
    - any version number like `25770` or `1383-e5ea040353ce1b8bc86e37982bf5d888938e3096` - *Downloads the specific artifact.*
1. On your servers `Settings` page, click `Reinstall Server` and confirm. Then simply wait for it to download the new server artifact.

### Auto Updating Server from Git

Listed below is the behavior of Git when it's enabled.

#### Startup Scenarios (On server start)

- If the `resources` folder is empty. The specified repository will be cloned into `resources` on startup.
- If the `resources` folder has a git repository inside it. It will run a git pull in `resources` on startup.

#### Reinstall Scenarios (If the `Reinstall Server` button is pressed)

- If the `resources` folder does not exist. The folder will be created and the specified repository will be cloned into `resources` on startup.

---

## 🛠️ Server Ports

Ports required to run the server in a table format. You only need the TxAdmin port if you plan to enable TxAdmin.

| Type | Port |
| - | - |
| Game | 30120 |
| txAdmin | 40120 (*Optional*) |

## ❤️ Acknowledgments

- **[Parkervcp](https://github.com/parkervcp)** - *For creating the original [egg](https://github.com/pelican-eggs/games-standalone/blob/main/gta/fivem).*
- **[Parkervcp](https://github.com/parkervcp)** - *[Git Clone & Pull Script](https://github.com/parkervcp/eggs/blob/master/scripts/git_cloner.sh).*
- **[Pterodactyl](https://pterodactyl.io/)** - *Creators and maintainers of the Pterodactyl panel.*
- **[Cfx.re](https://fivem.net/)** - *Creators and maintainers of FiveM & RedM.*
