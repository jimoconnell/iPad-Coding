# Using an iPad for Coding
This project will attempt to document my experiences using an iPad as a code-creation device using Git, Github and various applications. This document is *not* about creating iPad apps. 
This document is the README file for a GitHub project located here:
https://github.com/jimoconnell/iPad-Coding

I've had a 64GB iPad 2 that was under-utilized, mainly living near my bed, where it served as an alarm clock and a way to play Pandora while I fell asleep.  This being a waste of usable technology, I decided to factory wipe it and epurpose it as a mini-workstation that wouldn't weigh me down.

I recently got a Raspberry Pi 3 and installed Raspbian Linux on it, so I wanted to use my iPad as a convenient, portable workstation for writing code on it.  It works equally well, though, when I'm writing code for one of my 'real' servers too. 

## Keyboards
Now, coding using the on-screen keyboard would be a hellish way to live your life, but fortunately, the iPad has bluetooth, so you can connect any bluetooth keyboard.  I had one of those aluminum Apple keyboards and that connected well and worked perfectly, but did not lend itself to being tossed in a messenger bag with the iPad, as errant keystrokes woke the iPad, drained the battery and would manage to take dozens and dozens of random screen captures.

USB keyboards are out, obviously, as are any of the Logitec keyboards that use their dongle.  Fortunately, Logitec makes a fairly ideal keyboard, the Logitec K48o bluetooth multi-device keyboard. http://www.logitech.com/en-us/product/multi-device-keyboard-k480?crid=1221

It has a groove that you set your ipad into in landscape mode, or, if you prefer in portrait mode, which frees up enough space for a smartphone.  It makes no attempt to charge your devices, but doesn't get in the way of cables.  It also has a 3-position switch that lets you easily jump between different devices.

## SSH Client
With that sorted out, it was time to go looking for apps with which to get some work done.  The first thing I needed was a reliable SSH client. [Server Auditor] (https://serverauditor.com) is a free, very well-thought-out app that gets the job done. There is a paid version that I haven't tried, but the free version is ad-free.

With SSH working, I had a good, reliable way to do quite a bit of what I need to do, such as logging in to linux servers and editing files.  I could have really stopped there, since my servers all have git and vi, but I started to wonder what else I could do, leveraging the iPad's capabilities.

## Editing and Git
There are a lot of text editors for the iPad, but I wanted one that would work with git and not add a lot of steps to my workflow.  A thread on Reddit recommended the combination of WorkingCopy (git client) and Textastic (TextMate for iPad, basically) for editing.  

## Working Copy Git App
[Working Copy](http://workingcopyapp.com) has a free version that lets you check out repositories, but not push changes back to the repo on GitHub.  While this would be useful to some, I decided to buy the paid version for $14.99 and have not regretted it in the least.  Working copy will become the cornerstone of your workflow on the iPad, both with GitHub as well as privately-hosted repos. (There is an 'Enterprise Version" that lets you get the full-featured version in a single step, but I do not believe it offers any additional features, it's just a convenience for deploying throughout a company.)

Once you have Working Copy, authorize it against your GitHub account and clone or create a repo.  Now, it may appear that you can edit right there in WorkingCopy, but you really want to fire up an a real editor at this point.  Put WorkingCopy in the background and open up Textastic.  

### iOctocat
Working Copy is where you'll manage your git repositories, but if you're using GitHub, you'll also want to install [iOctocat](https://ioctocat.com) to do all of the things on GitHub that come along with being a member of the ecosystem.  GitHub is a social platform, after all, and iOctocat is where you manage your life on it. 

## Textastic Text Editor App
Get the $10 upgrade for Textastic.  I can't remember exactly what's different between the paid and unpaid versions, but the developers deserve the love.

My first instinct was to first open up Textastic, create a file, then check it in to git.  This is *not* the best way to go about it.  

Start from Working Copy.  

Open your repo and click the "+" mark to create a new file. Once you type the name, hit enter and the file will be created.  Switch over to Textastic and the file will be available from the file chooser.
(Yes, you *can* create files in Textastic, but it's more difficult to get them into Working Copy afterwards, so don't bother doing it this way.)

What also threw me a bit was when I looked for the save button.  There is none.  You edit to your heart's content, then switch back to WorkingCopy.  Looking at the repository view, you'll see that it has seen the changes and gives you a simple way to commit your changes. 

## Byword Markdown Editor
GitHub projects default to displaying a README as the top page of your project and they use Markdown syntax for formatting, but I'm a real newbie when it comes to Markdown, so I decided to look for an editor that would let me work visually, rather than just monospaced text and formatting codes. 
[Byword](https://bywordapp.com/) is the app to get.  It's a great Markdown editor, but as it uses IOS's feature for opening iCloud and Dropbox files, it can also open files in the git repo you've cloned in Working Copy. This is crucial for the workflow I am developing.
If you're new to Markdown, keep the [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) handy. 

## Other Utilities
[Fing](https://itunes.apple.com/us/app/fing-network-scanner/id430921107?mt=8) is a network scanning utility that is free and near-perfect.  What's it do? It scans your local network and tells you what machines are live and what services they are running.  This can be very handy if you plug in a new Raspberry Pi and want to log in, but you've forgotten its IP address. (Hint: It may be called 'raspberry pi.local' if you have Bonjour networking enabled.) 
[VNC Viewer](https://itunes.apple.com/us/app/vnc-viewer/id352019548?mt=8) is the VNC client that I use when I need to save myself from plugging a monitor and keyboard into my Raspberry 	Pi to do something that's easier to do graphically, or when giving a demo. Using the mouse is initially not intuitive, but you will grow to appreciate it very quickly. On the Pi, you'll need to install TightVNC and have it [run at boot time](https://learn.adafruit.com/adafruit-raspberry-pi-lesson-7-remote-control-with-vnc/running-vncserver-at-startup).
