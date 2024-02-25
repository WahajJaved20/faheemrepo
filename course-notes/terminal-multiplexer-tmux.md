---
description: >-
  --Tshark is terminal based wireshark--Ngrep is just grep for packet
  capture--capinfo just gives information about pcapng files--
---

# Terminal Multiplexer (TMUX)

tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal.

Installation Line:

```bash
sudo apt-get update
sudo apt install tmux
```

## Create a new session

```bash
tmux new -s session_name
```

## View ongoing sessions

```bash
tmux ls
```

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## Reattaching to the session

```bash
tmux attach-session -t session_name
```
