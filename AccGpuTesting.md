## What is this?

There isn't a lot of great data about ACC, triple screens, and graphics cards.

I have been running an Asus 2060 Super for about 18 months. I recently bought an EVGA 3070 bundle from antonline. 
Later that day, I realized that I could enroll in the "step up" program through EVGA. 
Since I would have access to three relevant GPUs in a relatively short period of time, I figured I'd do my best to try some science (tm)

** jesse gif

### My PC

* AMD Ryzen 5 3600
* 16 GB RAM, XMP'd to 3200
* 512 GB NVME drive where ACC lives
* Asus 2060 Super Dual Evo (or something like that)
* EVGA 3070 FTW3 (non Ti)

## Methodology

I captured a replay of a ~40 car grid from a SimRacing604 fun race. It was shortly after the ACC 1.8 update and so everyone was in the BMW M4 at Nurburgring.

Frameview documentation here
* https://www.nvidia.com/content/dam/en-zz/Solutions/GeForce/technologies/frameview/frameview-user-guide-1-1-web.pdf

Here's a Youtube video of the replay (IIRC, 1440 triple + epic detail + FSR quality)

** TODO upload video

Here's the replay file if you would also like to try it:

** TODO upload replay

When testing, I would:
* Set up FrameView - record for 120 seconds, no delay, when hitting F10
* Make graphics settings changes
* Hit Apply (if you don't hit apply, it doesn't warn you that you haven't :( )
* Go to main menu -> gallery
* Select the replay file
* Give it a little bit to load textures, whatever
* Pick my car (car 17) - I was last or almost last, so I have a good view of the field
* Switch to the higher rear camera - so you can see all of my car, including the rear diffuser, maximizing how far ahead the game has to draw
* Skip to 6:27 of the video (end of the warmup lap)
* Wait until 6:30 and then hit F10
* After Frameview reappears, rewind to 6:27 and do it again
* The results land in the FrameView directory

Reasons why this methodology is okay
* It produced pretty reproducible results

Reasons why it sucks
* I suck at Nurb GP, and using this means uploading a video of me sucking at the Nurb GP.
* It is in replay mode, so it might not reflect how the game plays in the real world, especially compared to racing against AI. (I never race against AI, so
* this is not a relevant use case for me)
* There's only one car model. At least in iRacing, this seems to be a big deal (which is why they capped the number of distinct car models that can be on track at once). 
* I don't think the same is true in ACC, but calling it out. 

## 3dMark results for reference

* 2060S: 
* 3070: 

## ACC results

| Resolution | Preset | Extra | 2060S avg | 2060S 99% | 2060S Min |
| --- | --- | --- | --- | --- | --- |
| 3x 1080p | Mine | | 69.7 | 54.1 | 46.4 |
| 3x 1080p | Mid | | 74.1 | 57.7 | 47.3 |
| 3x 1080p | High | | 47.3 | 38.0 | 34.4 |
| 3x 1080p | Epic | | 33.9 | 27.9 | 22.0 |
| 3x 1080p | Epic | DLSS Quality | 44.8 | 36.1 | 32.1 |
| 3x 1080p | Epic | FSR Quality | 44.3 | 35.5 | 29.6 |

| Resolution | Preset | Extra | 2060S avg | 2060S 99% | 2060S min | 3070 avg | 3070 99% | 3070 min
| --- | --- | --- | --- | --- | --- | --- | --- | --- | 
| 3x 1080p | Mine | | 69.7 | 54.1 | 46.4 |--- | --- | --- | 
| 3x 1080p | Mid | | 74.1 | 57.7 | 47.3 |--- | --- | --- | 
| 3x 1080p | High | | 47.3 | 38.0 | 34.4 |--- | --- | --- | 
| 3x 1080p | Epic | | 33.9 | 27.9 | 22.0 |--- | --- | --- | 
| 3x 1080p | Epic | DLSS Quality | 44.8 | 36.1 | 32.1 |--- | --- | --- | 
| 3x 1080p | Epic | FSR Quality | 44.3 | 35.5 | 29.6 |--- | --- | --- | 

