# Material Files

[![Android CI](https://github.com/peternmuller/MaterialFiles/actions/workflows/android.yml/badge.svg)](https://github.com/peternmuller/MaterialFiles/actions)
[![GitHub Release](https://img.shields.io/github/v/release/peternmuller/MaterialFiles?logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij48cGF0aCBkPSJNNy43NSA2LjVhMS4yNSAxLjI1IDAgMSAwIDAgMi41IDEuMjUgMS4yNSAwIDAgMCAwLTIuNVoiIGZpbGw9IiNGRkZGRkYiPjwvcGF0aD48cGF0aCBkPSJNMi41IDFoOC40NGExLjUgMS41IDAgMCAxIDEuMDYuNDRsMTAuMjUgMTAuMjVhMS41IDEuNSAwIDAgMSAwIDIuMTJsLTguNDQgOC40NGExLjUgMS41IDAgMCAxLTIuMTIgMEwxLjQ0IDEyQTEuNDk3IDEuNDk3IDAgMCAxIDEgMTAuOTRWMi41QTEuNSAxLjUgMCAwIDEgMi41IDFabTAgMS41djguNDRsMTAuMjUgMTAuMjUgOC40NC04LjQ0TDEwLjk0IDIuNVoiIGZpbGw9IiNGRkZGRkYiPjwvcGF0aD48L3N2Zz4=&label=Release&link=https%3A%2F%2Fgithub.com%2Fpeternmuller%2FMaterialFiles%2Freleases)](https://github.com/peternmuller/MaterialFiles/releases)
[![GitHub License](https://img.shields.io/github/license/peternmuller/MaterialFiles?logo=gnu&label=License&link=https%3A%2F%2Fgithub.com%2Fpeternmuller%2FMaterialFiles%2Fblob%2Fmaster%2FLICENSE)](LICENSE)
[![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/peternmuller/MaterialFiles/total?logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij48cGF0aCBkPSJNNC43NSAxNy4yNWEuNzUuNzUgMCAwIDEgLjc1Ljc1djIuMjVjMCAuMTM4LjExMi4yNS4yNS4yNWgxMi41YS4yNS4yNSAwIDAgMCAuMjUtLjI1VjE4YS43NS43NSAwIDAgMSAxLjUgMHYyLjI1QTEuNzUgMS43NSAwIDAgMSAxOC4yNSAyMkg1Ljc1QTEuNzUgMS43NSAwIDAgMSA0IDIwLjI1VjE4YS43NS43NSAwIDAgMSAuNzUtLjc1WiIgZmlsbD0iI0ZGRkZGRiI+PC9wYXRoPjxwYXRoIGQ9Ik01LjIyIDkuOTdhLjc0OS43NDkgMCAwIDEgMS4wNiAwbDQuOTcgNC45NjlWMi43NWEuNzUuNzUgMCAwIDEgMS41IDB2MTIuMTg5bDQuOTctNC45NjlhLjc0OS43NDkgMCAxIDEgMS4wNiAxLjA2bC02LjI1IDYuMjVhLjc0OS43NDkgMCAwIDEtMS4wNiAwbC02LjI1LTYuMjVhLjc0OS43NDkgMCAwIDEgMC0xLjA2WiIgZmlsbD0iI0ZGRkZGRiI+PC9wYXRoPjwvc3ZnPg==&label=Downloads&link=https%3A%2F%2Fgithub.com%2Fpeternmuller%2FMaterialFiles%2Freleases)](https://github.com/peternmuller/MaterialFiles/releases)

### An open source Material Design file manager, for Android 5.0+.

[Help translation on Transifex](https://www.transifex.com/zhanghai/MaterialFiles/) ([Search Android & GNOME translations](https://translations.zhanghai.me/), [Microsoft language resources](https://learn.microsoft.com/en-us/globalization/reference/microsoft-language-resources), [MIME type translations](https://gitlab.freedesktop.org/xdg/shared-mime-info/-/tree/master/po))

## Preview

<p><img src="fastlane/metadata/android/en-US/images/phoneScreenshots/1.png" width="32%" /> <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/2.png" width="32%" /> <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/3.png" width="32%" />
<img src="fastlane/metadata/android/en-US/images/phoneScreenshots/4.png" width="32%" /> <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/5.png" width="32%" /> <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/6.png" width="32%" /></p>

## Features

- Open source: Lightweight, clean and secure.
- Material Design: Follows Material Design guidelines, with attention into details.
- Breadcrumbs: Navigate in the filesystem with ease.
- Root support: View and manage files with root access.
- Archive support: View, extract and create common compressed files.
- NAS support: View and manage files on FTP, SFTP, SMB and WebDAV servers.
- Themes: Customizable UI colors, plus night mode with optional true black.
- Linux-aware: Like [Nautilus](https://wiki.gnome.org/action/show/Apps/Files), knows symbolic links, file permissions and SELinux context.
- Robust: Uses Linux system calls under the hood, not yet another [`ls` parser](https://news.ycombinator.com/item?id=7994720).
- Well-implemented: Built upon the right things, including [Java NIO2 File API](https://docs.oracle.com/javase/8/docs/api/java/nio/file/package-summary.html) and [LiveData](https://developer.android.com/topic/libraries/architecture/livedata).

## Why a fork of Material Files?

Some custom ROMs, like [SomethingOS](https://github.com/SomethingOS), include Material Files by default. However, these custom ROMs often do not fully adhere to the best practices for including third-party apps as outlined in the [Inclusion in custom ROMs](https://github.com/peternmuller/MaterialFiles?tab=readme-ov-file#inclusion-in-custom-roms) section. Specifically, they sometimes fail to avoid conflicts with the Play Store or F-Droid versions of the app. When the app is signed with a different certificate, it cannot be updated through these app stores. To address this issue, I forked the [original Material Files project](https://github.com/zhanghai/MaterialFiles) to change the package name to `fr.peternmuller.android.files`, so that users can receive updates, either by downloading them manually or through [Obtainium](https://github.com/ImranR98/Obtainium).

## Why Material Files?

Because I like Material Design, and clean Material Design.

There are already a handful of powerful file managers, but most of them just aren't Material Design. And even among the ones with Material Design, they usually have various minor design flaws (layout, alignment, padding, icon, font, etc) across the app which makes me uncomfortable, while still being minor enough so that not everybody would care to fix it. So I had to create my own.

Because I want an open source file manager.

Most of the popular and reliable file managers are just closed source, and I sometimes use them to view and modify files that require root access. But deep down inside, I just feel uneasy with giving any closed source app the root access to my device. After all, that means giving literally full access to my device, which stays with me every day and stores my own information, and what apps do with such access merely depends on their good intent.

Because I want a file manager that is implemented the right way.

- This app implemented [Java NIO2 File API](https://docs.oracle.com/javase/8/docs/api/java/nio/file/package-summary.html) as its backend, instead of inventing a custom model for file information/operations, which often gets coupled with UI logic and grows into a mixture of everything ([example](https://github.com/TeamAmaze/AmazeFileManager/blob/master/app/src/main/java/com/amaze/filemanager/filesystem/HybridFile.java)). On the contrary, a decoupled backend allows cleaner code (which means less bugs), and easier addition of support for other file systems.

- This app doesn't use `java.io.File` or parse the output of `ls`, but built bindings to Linux syscalls to properly access the file system. `java.io.File` is an old API missing many features, and just can't handle things like symbolic links correctly, which is the reason why many people rather parse `ls` instead. However parsing the output `ls` is not only slow, but also [unreliable](https://news.ycombinator.com/item?id=7994720), which made [Cabinet](https://github.com/aminb/cabinet/blob/master/app/src/main/java/com/afollestad/cabinet/file/root/LsParser.java) broken on newer Android versions. By virtue of using Linux syscalls, this app is able to be fast and smooth, and handle advanced things like Linux permissions, symbolic links and even SELinux context. It can also handle file names with invalid UTF-8 encoding because paths are not naively stored as Java `String`s, which most file managers does and fails during file operation.

- This app built its frontend upon modern `ViewModel` and `LiveData` which enables a clear code structure and support for rotation. It also properly handles things like errors during file operation, file conflicts and foreground/background state.

In a word, this app tries to follow the best practices on Android and do the right thing, while keeping its source code clean and maintainable.

Because I know people can do it right.

[Nautilus](https://wiki.gnome.org/Apps/Files) is a beautifully-designed and user-friendly file manager on Linux desktop, and it's fully Linux-aware. [Phonograph](https://github.com/kabouzeid/Phonograph) is an open source Material Design music player app (which I've been using for years), and it has just the right Material Design and implementation.

So, it's time for yet another Android file manager.

## Inclusion in custom ROMs

Thank you if you choose to include Material Files in your custom ROM! However since I've received several user complaints due to improper inclusion, I'd like to offer some suggestions on including this app properly for the good of end users:

- Please don't replace the AOSP [DocumentsUI](https://android.googlesource.com/platform/packages/apps/DocumentsUI/) app with this app. This app is not designed to replace DocumentsUI and can't handle a number of functionalities in DocumentsUI - in fact, it relies on DocumentsUI to do things like granting external SD card access.

- Please make sure this app can be uninstalled or at least disabled. Some users may not want this app for a variety of reasons, and get very upset when they can't remove it.

- Please avoid conflict with the Play/F-Droid version of this app. App stores cannot update apps signed with a different certificate, so you can either ship an APK that's signed by me (or F-Droid) so that users will be able to update it on Play/F-Droid, or fork this project and rename the package name when you need to sign the APK with a different certificate and potentially making other changes.

## License

    Copyright (C) 2018 Hai Zhang

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program. If not, see https://www.gnu.org/licenses.


    Copyright (C) 2024 Peter Noël Muller

    Modifications made by Peter Noël Muller to the original Material Files project are licensed under the GPL-3.0 License.