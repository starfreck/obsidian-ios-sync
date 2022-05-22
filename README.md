# obsidian ios sync

## Setup

1. Install [iSH](https://apps.apple.com/us/app/ish-shell/id1436902243) on your ios device

2. Run this in iSH

```shell
apk update

apk upgrade

apk add git

git clone https://github.com/starfreck/obsidian-ios-sync.git

mv obsidian-ios-sync/* .

rm -rf obsidian-ios-sync

chmod 777 -R .

./install.sh
```
3. Once you are done setting up 'rclone' run sync.sh

## Referance
- https://rclone.org
- https://rclone.org/drive/
- https://rclone.org/mega/
- https://github.com/ish-app/ish/wiki
- https://github.com/Jwink3101/syncrclone
