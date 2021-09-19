# Auto Save Snips
## Why do I need this?
Have you ever used Windows 10's snip and sketch feature? If yes, then you must have encountered the frustration of choosing the desired location to save the snip if you are not pasting it.

I encountered this issue everytime I did a custom screenshot and that is why I thought of automating it.

## What is Snip and Sketch?
Windows program that enables you to custom capture screen and paste or save it.

![snip](screenshots/snip.jpg)

## What is the process to save the snip?
1. Open the snip and sketch application or use the keyboard shortcut Win+Shift+S

![issue1](screenshots/issue1.jpg)

2. Then click the desired Screenshot and click on the save button at the top right and choose a location(everytime!!).

![issue2](screenshots/issue2.jpg)

I searched a lot to find a way to auto save the snips I take to a desired location but couldn't. So, I thought to do it on my own.

# How does this work?
After doing some finding, I came to know that the snips are saved in the clipboards (which are stored not at any location but the Live memory RAM).
I needed the location where this screen captures are stored so that I can manipulate their location and get them in the desired location everytime without actually saving.

## Solution:
After some more research😁, I found that when we open the snip preview, they temporarily get stored at a location.
Once the preview is opened and the temparary file is generated, I thought of moving it to the desired position.

### Simple way to do this is:
1. Monitor the folder where the temporary files are stored.
2. Whenever there is a file_created event check if the file has an extension of jpg
3. If it does have a jpg extension move the file to the desired location.

Now we just have to take a snip and preview it.
It will be automatically saved in the desired location.

Before screenshot
![screenshot captured](screenshots/output1.jpg)

After Screenshot
![automatically saved](screenshots/output2.jpg)

Thank You😊