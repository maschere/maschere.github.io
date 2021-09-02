---
title: "Epic MegaJam 2021: Day 1 #UnrealJam"
---
## Epic MegaJam 2021: Day 1

First ideas, story concept, DLSS and more

![2021 Epic MegaJam](https://img.itch.zone/aW1nLzY2NjA3NTUucG5n/original/dg2jZN.png "2021 Epic MegaJam #UnrealJam")
---


### Day 1:

**Running out of Space**. SO I got my first ideas for a story concept written down and started working on some basics need for the game. This includes a nice first person character, interaction system, main menu and of course the map for the first scene.


Then I was pleasantly surprised how easy and well-documented the setup for [NVIDIA's DLSS plugin](https://developer.nvidia.com/dlss-getting-started) for UE5 is. One minor caveat though: I was using UGameInstanceSubsystem's Initialize to enable DLSS, but this seems to fire before the graphics hook is complete and hence does not work. So you should set DLSS a little later (BeginPlay somewhere or a delayed FTimer).