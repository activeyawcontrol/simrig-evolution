## What is this?

There isn't a lot of great data about ACC, triple screens, and graphics cards. This makes it hard to figure out how far you need to upgrade in order to play triple 1440 comfortably.

![numbers?](https://raw.githubusercontent.com/activeyawcontrol/simrig-evolution/main/acc-math-confused.gif)

I have been running an Asus 2060 Super for about 18 months. I recently bought an EVGA 3070 bundle from antonline. 
Later that day, I realized that I could enroll in the "step up" program through EVGA. 
Since I would have access to three relevant GPUs in a relatively short period of time, I figured I'd do my best to try some science (tm)

![science!](https://raw.githubusercontent.com/activeyawcontrol/simrig-evolution/main/acc-science.gif)

### My PC

* AMD Ryzen 5 3600 (before) 5600x (after)
* 16 GB RAM, XMP'd to 3200
* 512 GB NVME drive where ACC lives
* Various GPUs:
  * Asus 2060 Super Dual Evo (or something like that)
  * EVGA 3070 FTW3 (non Ti)
  * EVGA 3080 Ti FTW3 

## Some prior art

BonnyTech did some 3070 triple 1440 testing in ACC here
* https://www.youtube.com/watch?v=fAxWfbWf2to

This testing was of a single car, and it was before 1.8 with DLSS/FSR.

## Methodology

I captured a replay of a ~40 car grid from a SimRacing604 fun race. It was shortly after the ACC 1.8 update and so everyone was in the BMW M4 at Nurburgring.

Frameview documentation here
* https://www.nvidia.com/content/dam/en-zz/Solutions/GeForce/technologies/frameview/frameview-user-guide-1-1-web.pdf

Here's a Youtube video of the replay. Note that because the replay was captured with triples, but I'm only playing it back on one monitor, it looks goofy. The goal here is just to give folks a loose idea of what the video was like. 

* https://www.youtube.com/watch?v=I1PxbWalp70

[![Watch the video](https://img.youtube.com/vi/I1PxbWalp70/default.jpg)](https://youtu.be/I1PxbWalp70)

The replay file is 178 MB - too big for github. Even zip compressed still 120 MB. If you want to try, let me know.
* Kunos, if you're out there, please let us trim replay files!

When testing, I would:
* Set up FrameView - record for 120 seconds, no delay, when hitting F10
  * If you're out there NVidia, please update FrameView so that it saves its settings!!
* ACC -> Main menu -> Options -> Video -> Make graphics settings changes
  * Hit Apply (if you don't hit apply, it doesn't warn you that you haven't :( )
  * If you're out there Kunos, please update the Video settings page so that it warns you if you haven't clicked Apply! That would have saved me some time
* ACC -> Main menu -> Gallery
* Select the replay file
* Give it a little bit to load textures, whatever (it usually looks odd for the first few seconds)
* Pick my car (car 17) 
  * I was last or almost last, so I have a good view of the field
* Switch to the higher rear camera - so you can see all of my car, including the rear diffuser, maximizing how far ahead the game has to draw
* Skip to 6:27 of the video (end of the warmup lap)
* Wait until 6:30 and then hit F10
* After Frameview reappears, rewind to 6:27 and do it again (2 tests per configuration to look for outliers)
* The results land in the FrameView directory

Reasons why this methodology is okay
* It produced pretty reproducible results
* It's relatively worst case (lots of cars, external cam)

Reasons why it sucks
* I suck at Nurb GP, and using this means uploading a video of me sucking at the Nurb GP.
* It is in replay mode, so it might not reflect how the game plays in the real world, especially compared to racing against AI. (I never race against AI, so this is not a relevant use case for me)
* There's only one car model - the BMW M4. At least in iRacing, this seems to be a big deal (which is why they capped the number of distinct car models that can be on track at once). I don't think the same is true in ACC, but calling it out. 

## 3dMark TimeSpy results for reference

* 3600 + 2060S: 8398
  * https://www.3dmark.com/spy/25949335
* 3600 + 3070: 11976
  * https://www.3dmark.com/spy/26001553
* 3600 + 3080ti: 15519
  * https://www.3dmark.com/spy/26354048
* 5600x + 3080ti: xxx
  * https://www.3dmark.com/spy/xxxx

## To the numbers!

![go!](https://raw.githubusercontent.com/activeyawcontrol/simrig-evolution/main/acc-go.gif)

## ACC results: triple 1080p

| Resolution | Preset | Extra | 2060S avg | 2060S 99% | 2060S Min | 3070 avg | 3070 99% | 3070 min
| --- | --- | --- | --- | --- | --- |--- | --- | --- |
| 3x 1080p | Mine |              | 69.7 | 54.1 | 46.4 | 
| 3x 1080p | Mid  |              | 74.1 | 57.7 | 47.3 | 90.6 | 66.3 | 49.6
| 3x 1080p | Mid  | DLSS Quality | ---- | --- | --- | 85.8 | 63.7 | 54.7
| 3x 1080p | Mid  | FSR Quality  | ---- | --- | --- | 84.8 | 63.3 |55.8
| 3x 1080p | High |              | 47.3 | 38.0 | 34.4 | 68.4 | 52.0 | 36.2
| 3x 1080p | High | DLSS Quality | ---- | --- | --- | 62.7 | 47.6 | 35.9
| 3x 1080p | High | FSR Quality  | ---- | --- | --- | 67.7 | 50.4 | 34.21
| 3x 1080p | Epic |              | 33.9 | 27.9 | 22.0 | 54.1 | 41.2 | 33.3
| 3x 1080p | Epic | DLSS Quality | 44.8 | 36.1 | 32.1 | 57.6 | 42.8 | 32.0
| 3x 1080p | Epic | FSR Quality  | 44.3 | 35.5 | 29.6 | 62.5 | 47.3 | 34.3

## ACC results: triple 1440p

![the new crysis](https://raw.githubusercontent.com/activeyawcontrol/simrig-evolution/main/acc-worse.gif)

| Resolution | CPU | Preset | Extra | 2060S avg | 2060S 99% | 2060S min | 3070 avg | 3070 99% | 3070 min | 3080ti avg | 3080ti 99% | 3080ti min
| ---      | -- | ---   | ---          | ---  | ---  | ---  | --- | --- | --- |  --- | --- | --- 
| 3x 1440p | 3600 | Basic |              | 73.3 | 56.2 | 43.9 | 108.9 | 79.4 | 64.9 |  --- | --- | ---  
| 3x 1440p | 3600 | Basic | DLSS quality | 62.0 | 49.7 | 39.5 | 91.5 | 68.6 | 46.1 |  --- | --- | ---  
| 3x 1440p | 3600 | Basic | FSR quality  | 65.2 | 50.7 | 40.0 | 98.5 | 69.2 | 47.3 |  --- | --- | ---  
| 3x 1440p | 3600 | Mid   |              | 49.4 | 40.3 | 34.0 | 80.0 | 62.9 | 56.7 |  --- | --- | ---  
| 3x 1440p | 3600 | Mid   | DLSS Quality | 53.6 | 44.5 | 41.3 | 81.0 | 65.1 | 50.8 |  --- | --- | --- 
| 3x 1440p | 3600 | Mid   | FSR Quality  | 44.3 | 35.5 | 29.6 | 86.5 | 68.3 | 62.2 |  --- | --- | ---  
| 3x 1440p | 3600 | High  |              | 31.1 | 25.8 | 20.9 | 51.9 | 41.7 | 37.4 | 70.6 | 54.7 | 46.1
| 3x 1440p | 3600 | High  | DLSS Quality | 41.8 | 34.3 | 28.4 | 63.4 | 49.2 | 34.4 | 71.4 | 54.1 | 43.9
| 3x 1440p | 3600 | High  | FSR Quality  | 42.5 | 34.6 | 29.0 | 67.5 | 53.0 | 45.4 | 73.3 | 55.8 | 41.3
| 3x 1440p | 5600x | High  |              | - | - | - | - | - | - | 71.3 | 55.9 | 39.3
| 3x 1440p | 5600x | High  | DLSS Quality | - | - | - | - | - | - | - | - | - |
| 3x 1440p | 5600x |  High  | FSR Quality  | - | - | - | - | - | - | - | - | - |

### ACC results: triple 1440p, epic preset

![the new crysis](https://raw.githubusercontent.com/activeyawcontrol/simrig-evolution/main/acc-epic.gif)

| Resolution | CPU | Preset | Extra | 2060S avg | 2060S 99% | 2060S min | 3070 avg | 3070 99% | 3070 min | 3080ti avg | 3080ti 99% | 3080ti min
| ---      | ---   | ---  | ---  | ---  | ---  | --- | --- | --- |  --- | --- | --- | --- |
| 3x 1440p | 3600 | Epic  | NA             | 22.0 | 18.2 | 13.7 | 37.7 | 30.4 | 24.2 | 57.4 | 44.3 | 37.4
| 3x 1440p | 3600 | Epic  | DLSS Quality | 31.9 | 26.8 | 21.9 | 50.6 | 40.2 | 37.0 | 66.6 | 50.1 | 36.9
| 3x 1440p | 3600 | Epic  | FSR Quality  | 31.0 | 25.5 | 21.2 | 51.8 | 40.6 | 36.8 | 68.4 | 51.7 | 38.6
| 3x 1440p | 5600x | Epic  | NA | - | - | - | - | - | - | 57.1 | 44.8 | 40.1
| 3x 1440p | 5600x | Epic  | DLSS Quality | - | - | - | - | - | - | - | - | - |
| 3x 1440p | 5600x | Epic  | FSR Quality  | - | - | - | - | - | - | - | - | - |

## Conclusions

* ACC is not nice to GPUs
* FSR does seem to produce slightly better frame rate than DLSS
* Oddly, DLSS made performance worse at triple 1440 basic?
* A 3070 should be enough to play ACC in triple 1440p as long as you turn down the settings and use one of the optimizations (DLSS/FSR). 
  * My goal is to keep things above 60 FPS, not something crazy like 100+. 
* Going from a 3600 to a 5600x did not affect things much. That's fine (for instance, it helps in iRacing), but if high rez ACC is your priority, spend on the GPU first. 

What I'm currently using: until I step-up to a 3080ti, I'm using triple 1440 high + FSR quality. For hotlapping, etc it's plenty, and in a busy field it might drop a little, but that is only for the first couple of laps. 

## Can I help?

If you have a similarly spec'd system (2060S, 3070, or something close) it would be really interesting to see your results too! 

activeyawcontrol at gmail
