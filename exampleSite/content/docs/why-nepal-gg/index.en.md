---
title: Why Nepal.gg?
description: Why we are starting a nepali gaming based community and what are our plans?
date: 2024-06-25T14:41:33.279Z
draft: false
noindex: false
featured: true
pinned: true
nav_weight: 1
nav_icon:
  vendor: bootstrap
  name: cloud-download
  color: green
series:
  - Docs
categories:
  - Official
tags:
  - Introduction
images:
  - https://example-images.razonyang.com/website-design.webp?width=1920&height=1280
authors:
  - Admin
---

We are a team of enthusiastic gamers who love to spend their free time with games with friends. Gaming can be a gateway to a new world and imagination. This escape helps us deal with the stresses of life or just have a rush of excitement. Gaming in Nepal is still somewhat considered a bad habit and a pathway to isolation and exclusion from responsibility and society. But it doesn't have to be.

We aim to create a competetive and a positivity based community for gaming in Nepal. Developing a nurturing and enthusiastic community is an uphill task but we believe that we can accomplish this with the right people and the right community. 

Considering the economic aspect of most of us in Nepal we are going to recommend and push open source or free games that are easy to get into to get you started in gaming. There are many games which are released for free on some stores like epic games or sometimes they are given away for free by the developers. You can build quite a collection with these games. Then you can pick and choose which genre of game you like and stick with it ohh you can explore till your heart desires.

Gaming can be empowering and gateway to new friendships and community, if one is responsible. Addiction to gaming without restrictions just leads a mental isolation from reality. Everything in moderation, including moderation. Games are way to interact and test your self and other as well in multi-player games. Gaming should be bridging the gap that's growing with the divide created by social media. Instead of meeting real people, people are more focused on creating a fake persona of themselves. 

There are dangers of toxicity and bullying on Gaming platforms, and this can be avoided by idenfying toxic elements and blocking, ignoring them before they get to your head. Most multiplayer games allow you to mute or block players. Use them generously.

{{< bs/alert danger >}}
{{< markdownify >}}
Please run these commands from [PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows) or a Linux terminal such as WSL or Git Bash.
{{< /markdownify >}}
{{< /bs/alert >}}

## Requirements

- Go
- Hugo extended version
- Node.js `16` or later

Read more on [prerequisites](https://hbstack.dev/docs/getting-started/prerequisites/).

## Clone the Repository

```sh
git clone --depth 1 https://github.com/hbstack/theme-cards
```

## Copy the Example Site

```sh
cp -r theme-cards/exampleSite mysite
```

## Change Working Directory

```sh
cd mysite
```

## Tweak `go.mod`

{{< bs/alert >}}
{{< markdownify >}}
This guide uses `sed` command to edit the file, please feel free to open and edit the `go.mod` with your favorite editor.
{{< /markdownify >}}
{{< /bs/alert >}}

### Replace Module Path

The module path is the identifier of your site, which typically is your repo URL, take `github.com/user/repo` as an example, you'll need to replace the `module github.com/hbstack/theme-cards/exampleSite` with `module github.com/user/repo`.

```sh
sed -i '1s/.*/module github.com\/user\/repo/' go.mod
```

### Delete the `replace` Directive

To build the site successfully, you'll need to delete the internal used `replace` directive: `replace github.com/hbstack/theme-cards => ../`.

```sh
sed -i '/^replace/d' go.mod
```

## Install Dependencies

```sh
npm ci
```

## Hugo Module Proxy (Optional)

A [Hugo module proxy](https://hugomods.com/blog/2023/04/go-and-hugo-proxy-servers/) is required when the default proxy isn't accessible from your location, i.e. China.

## Preview Locally

```sh
npm run dev
```

## What's Next?

1. Tweak Configurations, such as `baseURL`, `giscus.*` and so on.
2. Remove testing content.
3. Read the [documentation](https://hbstack.dev/).
4. Find more [modules](https://hbstack.dev/modules/).
