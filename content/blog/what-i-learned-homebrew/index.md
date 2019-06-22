---
title: What I Learned Using Homebrew Package Manager
date: "2019-06-21"
description: Learn How to Download Homebrew Onto Your Mac & Use It To Quickly Install/Uninstall Developer Tools From Your Terminal. Grab Your Mac, Sit Down & Get Ready to Follow Along. Start Learning Now! (5 Min Read) 
---

Yesterday I used [Homebrew](https://brew.sh/) "the missing package manager" for the first time at work. I have used it before, but didn't know what it was or why I needed it. My brother-in-law just downloaded it for me when I started to learn how to code and said it was really useful. 

I didn't know why it was so useful until I needed it working as database administrator at [Uptown Studios](https://uptownstudios.net/). I will discuss how to download Homebrew and how it increased my effeciency at work. 

If you just want to paste the Homebrew code snippet to your MacOS terminal, then here it is:

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)`

If you want to learn how Homebrew sped up my workflow and how I learned of its power then keep reading.

## How Homebrew Made Me Feel At Home While At Work

I work as Google Ads manager at Uptown Studios and was just offered the opportunity to become database administrator for all of the websites we host on our server. 

I have never done this before, but if there is anyting I learned about being a freelance web developer, never say no to a job. 

I immediately said yes, not really knowing what I was going to do. Instead of my usual panicking and trying to research everything about database administrator, I called my mentor and he reassured me I did the right thing. 

This made me feel better about my decision and I was able to go home to my family and be present. 

The next day I lit my gratitude candle with my sandalwood incense and sat my statue of Buddha down next to me. I prayed to find the courage to ask for help and to listen. I let my incense burn out and blew out candle, then drove to work and spoke with our web developer with a clear mind. 

He showed me how he access websites on their server using SSH access. I noticed his Terminal used highlighting syntax, autosuggestions, and autocomplete. I was blown away because all he had to do was type SSH then right arrow key and he was connected to the desired httpdocs folder.

>"I downloaded it with Homebrew" - Our Awesome Web Developer

I asked him how he magically did this and he said he uses [Fish Shell](https://fishshell.com/) to autocomplete Terminal suggestions making his workflow much faster. Interestingly, I had never heard of Fish Shell and immediately asked him how I can use it. 

He went to Fish Shells website and said "I downloaded it with Homebrew". Homebrew! I haven't heard that word since I started learning how to code. I immedately felt at home and knew I could do this job. 

Homebrew has been there for me when I was just learning how to use Terminal to manage my local directories and now I was using it at work to manage multiple website directories at once.


## How To Download Homebrew to Your OS

Paste into your MacOS Termial:

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)`

Knowing I wanted to setup my dev environment before I started working as Uptown Studios database administrator, I immediately went to Homebrew's website to get the code snippet to download on my machine. 

I went to Homebrew and found the code snippet at the top in all of its beauty. I copied the code snippet and pasted into my terminal. Within seconds I had Homebrew installed.

In addition, I immedately went to Fish Shell's website and found the Homebrew code snippet to quickly download it.

Simply type the following into Homebrew:


`brew install fish`

That's it! 

Homebrew installed Fish Shell into its own directory and then symlinked its file into a `usr/local` path.

I was able to set Fish Shell as my default Terminal shell by hitting `cmd` + `,` to open Terminals Preferences. Enter the `usr/local` path Fish Shell created into the "Command (complete path)" input. 

I then exited out of the Terminal Preferences and reset my Terminal, then magically Fish Shell was set as my default shell. 

Yay!

## In Conclusion

I am a beginner web developer and database manager. However, I understand the importance of package managers such as Homebrew. There are many more applications you can perform with Homebrew that I haven't mentioned and really haven't tried yet.

However you can create your own packages and simple ruby scripts by learning from other's open source code at [Homebrew Formulae](https://formulae.brew.sh/).

If you are looking to be able to quickly install/unistall developer tools without having to download dependencies or find them on Github. 

I highly recommend using Homebrew package manager. It will save you time and let you have fun with things called Fish Shell.

If this was helpful for you or if you felt this helped you understand Homebrew better. Then awesome! Writing this blog helped me understand it a little bit better too! Give yourself a pat on the back and code on my friend. 


_This blog post was inspired by my mentor and [freeCodeCamp](https://www.freecodecamp.org/) who recommends blogging about everything you learn. Thank you dev community for being amazing!_





