---
layout: post
title: "Removing the bell on emacs"
date: 2014-05-30 21:26:24 +0100
comments: true
categories: [code, emacs]
---
As I started blogging again with Spotify on the background, I noticed how annoying
the audible bell is. Of course, there is a variable `visible-bell` which toggles
between the audible and the visible bell. The visible bell in OS X is an ugly square
that appears over the Emacs window, and which is pretty much useless.

Fortunately there is yet another variable `ring-bell-function` which, if non-`nil`,
will be called as a function instead of showing/ringing the bell. So all I need
to set the bell to a reasonable value is:

```cl
;;; Turn audible and visible bells off
(setq ring-bell-function (lambda ()))
```
