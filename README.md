# YouCube


YouCube streams media from services like YouTube to [ComputerCraft: Tweaked](https://github.com/cc-tweaked/CC-Tweaked). \
**Project Status: Proof of concept**

## Installation

To Install the client use the following:

or

```shell
wget run https://raw.githubusercontent.com/Mcjevsta1234/installer/main/src/installer.lua
```

### Starting the Client

```text
youcube
```

### Libraries

All libraries that are used by the [client](https://github.com/Commandcracker/YouCube/blob/main/client/youcube.lua).

| Library                                                                                               |
|-------------------------------------------------------------------------------------------------------|
| [argparse](https://github.com/Commandcracker/cc-argparse)                                             |
| [numberformatter](https://github.com/Commandcracker/YouCube/blob/main/client/lib/numberformatter.lua) |
| [semver](https://github.com/kikito/semver.lua)                                                        |
| [youcubeapi](https://github.com/Commandcracker/YouCube/blob/main/client/lib/youcubeapi.lua)           |
| [string_pack](https://gist.github.com/MCJack123/d5973e4d8b7e46991c5f99ac4b076aec)                     |

### UnicornPKG (Experimental)

YouCube can be installed with [unicornpkg](https://unicornpkg.madefor.cc/). \
Just run `hoof install youcube` to install it.

### LevelOS / lStore

[![lStore Package](https://img.shields.io/github/actions/workflow/status/CC-YouCube/client/lstore-put.yml?branch=main&label=lStore%20Package&logo=github&style=for-the-badge)](https://github.com/CC-YouCube/client/actions/workflows/lstore-put.yml)

On [LevelOS](https://discord.com/invite/vBsjGqy99U) YouCube can be installed by running `lStore get YouCube <path>` or `lStore get bpBYV1aG <path>` or by Using the StoreUI.

![preview](.README/levelos.png)

## Settings

Settings that can be set with the CC: Tweaked [settings module](https://tweaked.cc/module/settings.html#v:get)

| Name                   | Default | Description                                       |
|------------------------|---------|---------------------------------------------------|
| `youcube.server`       |         | First server that should be used                  |
| `youcube.keys.skip`    | 32 (d)  | Key code to skip song                             |
| `youcube.keys.back`    | 30 (a)  | Key code to head to previous song                 |
| `youcube.keys.restart` | 19 (r)  | Restarts the current song                         |
| `youcube.max_back`     | 32      | Maximum ammount of songs that can be gone back to |

## Events

List of events that are [queued](https://tweaked.cc/module/os.html#v:queueEvent) by youcube

| Name                     | Arguments | Description                                     |
|--------------------------|-----------|-------------------------------------------------|
| `youcube:vid_eof`        | `data`    | Called, when Video playback has ended           |
| `youcube:audio_eof`      | `data`    | Called, when Audio playback has ended           |
| `youcube:fill_buffers`   |           | Internal event (called when buffers are filled) |
| `youcube:status`         | `data`    | Status of the serversided media download        |
| `youcube:playback_ended` |           | Called, when all playback has ended             |
| `youcube:vid_playing`    | `data`    | Called, when Video playback has started         |
| `youcube:audio_playing`  | `data`    | Called, when Audio playback has started         |
| `youcube:playing`        |           | Called, when playback has started               |
