# js_yt_speed_shortcut
Change youtube playback speed without giving away your fingerprint.

```
document.onkeypress = function () {
    var characterPressed = String.fromCharCode(event.keyCode);
    //console.log(characterPressed);

    playbackRate = document.getElementsByClassName("video-stream html5-main-video")[0].playbackRate;

    if ((characterPressed === ":") && (playbackRate < 5.0)) {
        document.getElementsByClassName("video-stream html5-main-video")[0].playbackRate += 0.25;
    }
    if ((characterPressed === "?") && (playbackRate > 0.25)) {
        document.getElementsByClassName("video-stream html5-main-video")[0].playbackRate -= 0.25;
    }
};
```

Because of the recent Firefox drama, I have changed my browser to Librewolf (LW).  
A feature that is enabled by default is [RFP (Resist Fingerprinting)](https://librewolf.net/docs/faq/#what-are-the-most-common-downsides-of-rfp-resist-fingerprinting).  
There are some consequences to using it:  
- The window size at start is not full screen.  
This is not a big problem as I suspend my computer, so I rarely start the browser.  
- Key combinations (using Shift, Alt, Control) may not work.  
I'm pretty used to speeding up videos on youtube and I need the shift key with the layout I usually use,  
so that's annoying. This repo is a solution.  
- LW does not remember zoom value for a website.  
I usually read the wiki at 150% zoom and it is annoying to set it every time.

Use an extension that allows you to set a javascript code that runs every time a site loads.  
Copy the above code into it for youtube's url.  
  
### Sources  
[YouTube speed control with JavaScript](https://dev.to/walternascimentobarroso/youtube-speed-control-with-javascript-4mfb)  
[SO Intercepting keyboard presses](https://stackoverflow.com/a/12010245)  
