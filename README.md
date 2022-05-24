# [obsidian](https://obsidian.md) ios sync

## Note
- [The iSH will ask for the location permisson to run in background. It does not log or monitor anyone's location](https://github.com/ish-app/ish/wiki/Running-in-background)
- To be more secure please try to use your own Google Drive API keys
- Create a pull request to contribute
 
## TODO
- [ ] Add sync.sh in to [OpenRC](https://wiki.alpinelinux.org/wiki/OpenRC) init system to run on start-up. [Read more](https://github.com/ish-app/ish/wiki/How-To-Enable-OpenRC-&-Start-Services-When-iSH-App-Starts).
- [ ] Fix the iSH app freeze issue after sometime ( it works but still sometimes freezes. I think it depends on the processor of your device. I only have an iPad. Please test and let me know your results)

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
3. Once you are done setting up 'rclone', We will update paths in config.py

4. python3 update_config.py "pathA" "pathB"

```shell
# Create a folder name 'Obsidian' in root of your Cloud Storage
# Replcae 'gdive' in below command with your given name i.e. 'mega' etc.
# Do not change '/root/Obsidian' because we have already mounted the right folder on that path via Script

python3 update_config.py "gdrive:Obsidian" "/root/Obsidian"

# if you mess up then just use "syncrclone --new config.py" to create new config.py
```

5. Run ./sync.sh and it will sync your Obsidian automatically. :)

## Referance
- https://rclone.org
- https://rclone.org/drive/
- https://rclone.org/mega/
- https://github.com/ish-app/ish/wiki
- https://github.com/Jwink3101/syncrclone
