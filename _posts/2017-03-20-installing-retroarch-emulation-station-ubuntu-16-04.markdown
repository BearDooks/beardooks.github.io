---
title: Installing RetroArch and Emulation Station Ubuntu 16.04
date: 2017-03-20 11:08:42 -04:00
categories:
- Guides
tags:
- '16.04'
- Emulation
- EmulationStation
- N^$
- NES
- PSX
- RetroArch
- SNES
- Station
- Ubuntu
- Ubuntu 16.04
layout: post
author: Chuck Lindblom
---

Edit:
  
I wrote this and then I found this method is no good. There is so much that does not work. Adding to this seems impossible. If you really want to run this on ubuntu, then go to the official site and follow their directions.

sudo add-apt-repository ppa:emulationstation/ppa
  
sudo add-apt-repository ppa:libretro/stable
  
sudo apt update
  
sudo apt install emulationstation emulationstation-theme-simple
  
sudo apt install libretro-nestopia libretro-snes9x-next libretro-mupen64plus libretro-mednafen-psx