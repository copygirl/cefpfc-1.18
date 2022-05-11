# copy's Extraordinary Fabric Pack for Cuties

.. or "cefpfc" for short, is a Minecraft 1.18.2 Fabric modpack. It aims to provide an optimized, expanded, yet solid Minecraft experience. For a list of mods and short descriptions on each check out [MODS.md](docs/MODS.md). You might also want to take a quick look at [CONTROLS.md](docs/CONTROLS.md).

## Download / Installation

We use [packwiz] to create an auto-updating [PolyMC] / [MultiMC] modpack. If you're unsure which launcher to get, I personally recommend PolyMC. It's more actively developed. MultiMC should work perfectly fine, however. Installation is simple:

- In PolyMC / MultiMC, click "Add Instance", then "Import from zip".
- Go to the [Releases] page and right click the latest .zip release file and click "Copy Link".
- Paste the link into the box titled "Local file or link to a direct download".
- Press OK to create the instance, then launch it.
- Select any optional mods you'd like to play with.

Please note that your instance will automatically update when new versions are released. If you would like to avoid this, you can go to the instances "Settings", then "Custom commands", and disable the check box.

[packwiz]: https://github.com/packwiz/packwiz
[PolyMC]: https://polymc.org/
[MultiMC]: https://multimc.org/
[Releases]: https://github.com/copygirl/cefpfc-1.18/releases

## Server Setup

```sh
# Download the packwiz bootstrapper and Fabric server launcher.
curl -LOJ https://github.com/packwiz/packwiz-installer-bootstrap/releases/download/v0.0.3/packwiz-installer-bootstrap.jar
curl -LOJ https://meta.fabricmc.net/v2/versions/loader/1.18.2/0.14.4/0.10.2/server/jar

# Download modpack files. Also run this to update.
java -jar packwiz-installer-bootstrap.jar -g -s server https://raw.githubusercontent.com/copygirl/cefpfc-1.18/main/pack.toml

# Start up the server with 4GB RAM. Or use your usual server launch script.
java -Xms4G -Xmx4G -jar fabric-server-mc.1.18.2-loader.0.14.4-launcher.0.10.2.jar nogui
# Do the usual: Accept the EULA, modify the server.properties, ...
```
