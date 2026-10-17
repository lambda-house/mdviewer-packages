# MDViewer packages

Signed apt and dnf repository for [MDViewer](https://github.com/lambda-house/mdviewer-mj), served at https://lambda-house.github.io/mdviewer-packages/. The MDViewer release workflow adds each release here (`packaging/linux-repo/build.sh`); don't edit the package directories by hand.

Signing key fingerprint: `CF6514F8FF85FCB383F24C14D7A16159C913520B`

## Debian, Ubuntu

```sh
curl -fsSL https://lambda-house.github.io/mdviewer-packages/mdviewer.gpg | sudo tee /usr/share/keyrings/mdviewer.gpg > /dev/null
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/mdviewer.gpg] https://lambda-house.github.io/mdviewer-packages/deb stable main" | sudo tee /etc/apt/sources.list.d/mdviewer.list
sudo apt update && sudo apt install md-viewer
```

## Fedora, RHEL

```sh
sudo curl -fsSL -o /etc/yum.repos.d/mdviewer.repo https://lambda-house.github.io/mdviewer-packages/mdviewer.repo
sudo dnf install md-viewer
```
