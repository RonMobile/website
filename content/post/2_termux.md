---
title: "Step 1 - Termux"
author: "Krzysztof Joachimiak, Adam Karolewski"
date: '2022-02-23'
image: ''
slug: []
subtitle: ''
tags: []
categories: []
type: ''
---

# TERMUX

The best way to instll R on Android is via Termux. 

The nice way how to do it one may find on this website: https://conr.ca/post/installing-r-on-android-via-termux/

1. Install Termux

2. Add pointless package repository
pkg install curl gnupg
mkdir -p "$PREFIX/etc/apt/sources.list.d/"
echo "deb https://its-pointless.github.io/files/24 termux extras" > "$PREFIX/etc/apt/sources.list.d/pointless.list"
curl "https://its-pointless.github.io/pointless.gpg" | apt-key add

3. Install required .deb packages
pkg install r-base \
            make \
            clang \
            gcc-9 \
            libgfortran5 \
            openssl \
            libcurl \
            libicu \
            libxml2
            
