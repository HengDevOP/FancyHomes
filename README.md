# FancyHomes

https://imgur.com/a/9UL8Ume

Set personal homes, teleport to them, and manage your homes with simple commands.

## ✨ Features

* 🏠 Set personal homes
* 📍 Teleport to your homes
* 🗑️ Delete homes
* 📋 List all your homes
* 🔢 Configurable maximum homes
* 💾 Persistent home data
* ⚡ Lightweight and fast
* 🔐 Permission-based controls
* ⚙️ Fully configurable messages
* 🌍 Supports multiple worlds

## 📦 Requirements

* **Minecraft:** 1.21.x
* **Server:** Paper / Spigot
* **Java:** 21+

## 🛠️ Commands

| Command           | Description        |
| ----------------- | ------------------ |
| `/sethome <name>` | Set a new home     |
| `/home <name>`    | Teleport to a home |
| `/homes`          | List your homes    |
| `/delhome <name>` | Delete a home      |
| `/home help`      | Show home commands |

### Examples

```text
/sethome base
/home base
/homes
/delhome base
```

## 🔑 Permissions

| Permission      | Description           | Default |
| --------------- | --------------------- | ------- |
| `home.use`      | Use the home system   | `true`  |
| `home.sethome`  | Set homes             | `true`  |
| `home.teleport` | Teleport to homes     | `true`  |
| `home.delete`   | Delete homes          | `true`  |
| `home.list`     | List homes            | `true`  |
| `home.admin`    | Access admin features | `op`    |

## ⚙️ Configuration

Example `config.yml`:

```yaml
homes:
  default-limit: 3

teleport:
  delay: 3
  cancel-on-move: true

messages:
  prefix: "&8[&bHome&8] "
  sethome: "&aHome &f{name} &ahas been set."
  teleport: "&aTeleporting to &f{name}&a..."
  delete: "&cHome &f{name} &chas been deleted."
  not-found: "&cThat home does not exist."
  limit: "&cYou have reached your home limit."
  no-permission: "&cYou don't have permission to do that."
```

## 💾 Data Storage

Home locations are stored persistently so they remain available after:

* Server restarts
* Player disconnects
* Plugin reloads

Example data:

```yaml
homes:
  uuid:
    base:
      world: world
      x: 100.5
      y: 65.0
      z: -42.5
      yaw: 90.0
      pitch: 0.0
```

## 📁 Project Structure

```text
Home/
├── src/
│   └── main/
│       ├── java/
│       │   └── net/
│       │       └── khmc/
│       │           └── home/
│       │               ├── HomePlugin.java
│       │               ├── command/
│       │               ├── manager/
│       │               ├── storage/
│       │               └── listener/
│       │
│       └── resources/
│           ├── plugin.yml
│           └── config.yml
│
├── pom.xml
└── README.md
```

## 🚀 Installation

1. Download the latest `Home.jar`.
2. Place it inside your server's `plugins` folder.
3. Restart your server.
4. Configure the plugin in:

```text
plugins/Home/config.yml
```

5. Start using:

```text
/sethome base
/home base
```

## 🔮 Planned Features

* [ ] `/home` GUI
* [ ] Home teleport warmup
* [ ] Teleport cooldown
* [ ] Per-world home limits
* [ ] Permission-based home limits
* [ ] Home rename command
* [ ] Home icons
* [ ] Admin home management
* [ ] PlaceholderAPI support
* [ ] Database storage
* [ ] MySQL support
* [ ] MongoDB support

## 🤝 Contributing

Contributions, suggestions and bug reports are welcome.

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature/my-feature
```

3. Make your changes
4. Commit your changes

```bash
git commit -m "Add my feature"
```

5. Push your branch

```bash
git push origin feature/my-feature
```

6. Open a Pull Request

## 🐛 Bug Reports

If you find a bug, please open an issue and include:

* Minecraft version
* Server software and version
* Home plugin version
* Error message / console log
* Steps to reproduce the issue

## 📜 License

This project is licensed under the MIT License.

See [`LICENSE`](LICENSE) for more information.

---

Made with ❤️ for Minecraft servers.

**KHMC.NET**
