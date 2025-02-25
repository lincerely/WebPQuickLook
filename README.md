Quick Look Plugin for WebP Files
================================

### About this fork

  This is a fork of [emin/WebPQuickLook](https://github.com/emin/WebPQuickLook)
  with patches from:

 - [capnslipp](https://github.com/lincerely/WebPQuickLook/pull/2), fixes memory leak;
 - [saagarjha](https://github.com/lincerely/WebPQuickLook/pull/1), fixes bus error and updates libwebp to 1.0.2.

  Tested on MacOSX 10.14.6, but should work on 10.9+.

### What is this?

  Quick Look is a part of Mac OS X. It provides you a quick way
  to look at your content without open it in an application.
  In Finder, choose a file or folder and push the space button, then QuickLook
  mechanism quickly show the preview of the content. And also it is responsible
  for the thumbnail creation.

  Most people know this mechanism. By default, OS X doesn't provide preview and
  thumbnail for all file types. [WebP](https://developers.google.com/speed/webp/) is Google's new image format and OS X
  doesn't recognize the .webp files. This plugin will give you an ability to
  see previews and thumbnails of WebP images.

### How does it look like?

  Just like an ordinary image file:

  ![quicklook webp](https://raw.github.com/lincerely/WebPQuickLook/master/screenshot.png 'WebP')


### How can I install it?

  This is simple for those of you who are familiar with terminal
  (console).

  Open your terminal app (or whatever you use) and copy paste the below
  command:

  ```bash
  mkdir -p ~/Library/QuickLook
  curl -OL https://github.com/lincerely/WebPQuickLook/releases/download/v1.0.0/WebpQuickLook.qlgenerator.tar.xz
  xattr -c WebpQuickLook.qlgenerator.tar.xz
  tar xvf WebpQuickLook.qlgenerator.tar.xz -C ~/Library/QuickLook
  qlmanage -r
  ```

  That's it. You just installed it. Enjoy your WebP files just like ordinary
  image files.

  If you use [homebrew](https://brew.sh/) you can do:
  
	brew install --cask lincerely/tools/WebPQuickLook
  

### The other users can't use it. What can I do?

  You can do it same operations by logining their account. But if you want
  to install for all users, that's simple and similar the above commands.
  Just use this installation script,
 
  ```bash
  mkdir -p ~/Library/QuickLook
  curl -OL https://github.com/lincerely/WebPQuickLook/releases/download/v1.0.0/WebpQuickLook.qlgenerator.tar.xz
  xattr -c WebpQuickLook.qlgenerator.tar.xz
  sudo tar xvf WebpQuickLook.qlgenerator.tar.xz -C /Library/QuickLook
  qlmanage -r
  ```

  This requires an administrator account, if you are not administrator you
  can't install it. It'll ask for password then you're done.


