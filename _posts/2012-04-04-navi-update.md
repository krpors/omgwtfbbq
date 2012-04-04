---
layout: base
header-title: NAVI!
title: Navi updated
category: programming
tags: navi
---

Navi has been updated
=====================

Navi, [my little custom project](http://github.com/krpors/navi), is a 
directory based music player for teh Linux. It uses wxWidgets for UI stuff
and whatnot, and the very much excellent GStreamer framework for playback.

I've updated the source to disable OSD notificiations due to incompatibilities
between ``libnotify`` versions:

*Version 0.5.0*

    NotifyNotification *notify_notification_new
        (const char *summary,
         const char *body,
         const char *icon,
         GtkWidget  *attach);

*Version 0.7.3:*

    NotifyNotification *notify_notification_new
        (const char *summary,
         const char *body,
         const char *icon);

As you can see, the fourth argument is missing, making them incompatible. In the
meantime, I've decided to skip OSD altogether until I find a way to manage this
version difference correctly (or use a different OSD library altogether).

Also, a column for track duration has been included! You can check out the project
by invoking:

    git clone https://krpors@github.com/krpors/navi.git

or see the [README here](https://github.com/krpors/navi/blob/master/README.md).
