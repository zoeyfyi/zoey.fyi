---
title: "Boop GTK"
date: 2020-08-02T01:18:15+01:00
draft: false
toc: false
images:
tags:
  - software dev
  - linux
---

When I saw [Boop](https://github.com/IvanMathy/Boop) while exploring new Github projects, I found a tool that I have been wanting for a long time. Boop is a simple editor that allows you to execute scripts on the buffer. The idea is that don't have to paste potentially secret infomation in to shady websites to do some simple transforms, like format json and decoding query strings.

Unfortunatley Boop is written in Swift using Apple UI librarys and Apple's JavascriptCore, so its not possible to use it on linux (or windows). I decide to rewrite it in Rust with GTK and Chrome's V8 engine. The result is [Boop-GTK](https://github.com/mrbenshef/Boop-GTK).

![Screenshot](/boop-gtk/screenshot.png)

Boop-GTK is completely cross-platform, feature complete (as far as I can tell) and script compatible with Boop. If you like the look of Boop, you will like Boop-GTK!

Check it out on Github: https://github.com/mrbenshef/Boop-GTK

Pull requests welcome :)