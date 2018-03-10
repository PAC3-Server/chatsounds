# What is chatsounds?
It's an addon for garrysmod and goluwa that plays sounds based on what players in the chat are saying. This repository contains the actual sounds. The source for chatsounds can be found here https://gitlab.com/CapsAdmin/goluwa/tree/master/game/lua/libraries/audio/chatsounds

# How does chatsounds read from this repository?
Sounds are read from `sounds/chatsounds/*`
The structure is `sounds/chatsounds/*CATEGORY*/*TRIGGER*`
If you say `geee it's kinda dark` in the chat, it will play the following sounds in order.
```
sounds/chatsounds/cdihm_mario/geee.ogg
sounds/chatsounds/cdihm_mario/its kinda.ogg
sounds/chatsounds/cdihm_mario/dark.ogg
```
The first sound `gee` is found in the directory/category `cdihm_mario` which will influence the next sounds to be found in the same category. If not they are searched for in other directories.

All punctation is stripped and space is normalized. `gEEE it's KINDA DarK?` will become `geee its kinda dark` internally before it's looked up.

A trigger can also be a directory. When it's a directory, its content will be randomly chosen. The file names inside a directory doesn't matter, but I recommend naming them like so.

```
sounds/chatsounds/cdihm_mario/foo/1.ogg
sounds/chatsounds/cdihm_mario/foo/2.ogg
sounds/chatsounds/cdihm_mario/foo/3.ogg
```

# How can I easily add sounds?

1. Click fork in the top right corner of this page. 
2. Drag drop sounds or directories into your forked repository. 
3. Click commit changes
4. Click new pull request
5. Click Create pull request
6. Change the title "Add files via upload" to something more descriptive.
7. Click Create pull request and wait for your change to be merged by someone
