title: main

----

# Who?

Kevin. (Open source) software enthusiast. I prefer statically typed and compiled
languages, especially [Go](http://golang.org). I also have a warm heart for C, although 
I have never really programmed with it. C++ is also ok. As of late, I've grown tired
of Java even though I have to admit that's the language I know best.

# Online stuff

1. [Uninteresting blog](/blog) - a collection of rants, notes and other things.
1. [Dump](http://dump.omgwtfbbq.nl) - where I dump stuff for quick sharing.
1. [Github](http://github.com/krpors) - my github profile page with projects.

# Miscellaneous

1. [SVN log chart](/svn/barchart.html) - Analyzed SVN logs from my current workplace, as a barchart.
1. [SVN log table](/svn/table.html) - Same data, except in a sortable table.

# Projects

This is a collection of small open-source projects I maintain.

### [hmon](http://github.com/krpors/hmon) - a very simplistic http 'monitor'.

At work I'm maintaining several hundreds of HTTP (web)services on test environments.
Think WSDL and XML (yuck). I was frequently 'challenged' to check whether every single
one of these services are still running. I could obviously use something like SoapUI,
but I grow tired of GUIs. Therefore I created something of my own, which 'pings' these
webservices, and on the response zero or more content 'assertions' are fired to check
whether the service is still returning what I expect.

### [wasp](http://github.com/krpors/wasp) - web based 'remote control' for mplayer.

The idea was to put this on a Raspberry Pi. `mplayer` doesn't make use of the GPU 
however, and therefore I couldn't really make use of my own program yet. Besides,
[XBMC](http://xbmc.org) exists which does the job much better. I am keeping the
source for nostalgia's sake, since it's the first Go program I've created.

### [navi](http://github.com/krpors/navi) - directory based music player for Linux.

This was my pet project to learn C++ more thoroughly. It makes use of [wxWidgets](http://wxwidgets.org)
and [GStreamer](http://gstreamer.net). It was pretty much functional, but lost interest
a bit since I'm currently using Spotify (Premium) to listen to music.
