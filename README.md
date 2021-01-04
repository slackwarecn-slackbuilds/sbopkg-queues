# sbopkg-queues

常用软件的 slackbuilds 队列 (sbopkg queue)。

## Alternative

如果没有特殊需要，仅仅是想安装一个 slackbuilds.org 上的软件包与所有相关依赖，
建议使用 `sqg` 工具。

`sqg` 脚本随 `sbopkg` 一同提供，你可以用命令 `sqg -p <pkg>` 来快速生成一个包的安装队列。

例如安装 `neovim`，可以用命令 `sudo sqg -p neovim `产生 `/var/lib/sbopkg/queue/neovim.sqf`，
然后使用 `sudo sbopkg -i neovim.sqf` 安装。

## Usage

```
git clone https://github.com/slackwarecn/sbopkg-queues/
cd sbopkg-queues
cp -r *.sqf /var/lib/sbopkg/queue/
```

完成后即可使用 `sbopkg` 命令安装相关软件包队列。例如安装 `neovim`:

```
sudo sbopkg -i neovim.sqf
```

