---
title: Hugo主题PaperMod配置
date: 2024-06-28T16:16:40+08:00
draft: true
slug: Hugo主题PaperMod配置
categories: Hugo
---

```yaml
baseURL: "your domain"
title: ExampleSite
paginate: 5
theme: PaperMod

enableRobotsTXT: true
buildDrafts: true
buildFuture: true
buildExpired: true

minify:
  disableXML: true
  minifyOutput: true

params:
  env: production # to enable google analytics, opengraph, twitter-cards and schema.
  title: ExampleSite
  description: "ExampleSite description"
  keywords: [Blog, Portfolio, PaperMod]
  author:
  # author: ["Me", "You"] # multiple authors
  images: ["<link or path of image for opengraph, twitter-cards>"]
  DateFormat: "2006-01-02"
  defaultTheme: auto # dark, light
  disableThemeToggle: false

  ShowReadingTime: true
  # ShowShareButtons: true
  ShowPostNavLinks: true
  ShowBreadCrumbs: true
  ShowCodeCopyButtons: true
  ShowWordCount: true
  ShowRssButtonInSectionTermList: true
  UseHugoToc: true
  disableSpecial1stPost: false
  disableScrollToTop: false
  comments: false
  hidemeta: false
  hideSummary: true
  showtoc: true
  tocopen: true

  assets:
    # disableHLJS: true # to disable highlight.js
    # disableFingerprinting: true
    favicon: "/favicon.png"
    favicon16x16: "/favicon.png"
    favicon32x32: "/favicon.png"
    apple_touch_icon: "/favicon.png"
    safari_pinned_tab: "/favicon.png"

  label:
    text: "Home"
    icon: /favicon.png
    iconHeight: 35

  # profile-mode
  profileMode:
    enabled: false # needs to be explicitly set
    title: ExampleSite
    subtitle: "This is subtitle"
    imageUrl: "<img location>"
    imageWidth: 120
    imageHeight: 120
    imageTitle: my image
    buttons:
      - name: Posts
        url: posts
      - name: Tags
        url: tags

  # home-info mode
  homeInfoParams:
    Title: "Hi there \U0001F44B"
    Content: Welcome to my blog

  # socialIcons:
  #   - name: x
  #     url: "https://x.com/"
  #   - name: stackoverflow
  #     url: "https://stackoverflow.com"
  #   - name: github
  #     url: "https://github.com/"

  # analytics:
  #   google:
  #     SiteVerificationTag: "XYZabc"
  #   bing:
  #     SiteVerificationTag: "XYZabc"
  #   yandex:
  #     SiteVerificationTag: "XYZabc"

  cover:
    hidden: true # hide everywhere but not in structured data
    hiddenInList: true # hide on list pages and home
    hiddenInSingle: true # hide on single page

  # editPost:
  #   URL: "https://github.com/<path_to_repo>/content"
  #   Text: "Suggest Changes" # edit text
  #   appendFilePath: true # to append file path to Edit link

  # for search
  # https://fusejs.io/api/options.html
  fuseOpts:
    isCaseSensitive: false
    shouldSort: true
    location: 0
    distance: 1000
    threshold: 0.4
    minMatchCharLength: 0
    limit: 10 # refer: https://www.fusejs.io/api/methods.html#search
    keys: ["title", "permalink", "summary", "content"]
menu:
  main:
    - identifier: categories
      name: categories
      url: /categories/
      weight: 10
    - identifier: tags
      name: tags
      url: /tags/
      weight: 20
    - identifier: example
      name: example.org
      url: https://example.org
      weight: 30
# Read: https://github.com/adityatelange/hugo-PaperMod/wiki/FAQs#using-hugos-syntax-highlighter-chroma
pygmentsUseClasses: true
markup:
  highlight:
    noClasses: false
    # anchorLineNos: true
    # codeFences: true
    # guessSyntax: true
    # lineNos: true
    # style: monokai

```