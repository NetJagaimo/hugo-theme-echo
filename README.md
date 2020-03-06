![hugo-theme-echo-preview](https://blog-1251237404.cos.ap-guangzhou.myqcloud.com/VSk6Kq.png)
## hugo-theme-echo

Echo 是一個風格簡潔的 Hugo 主題。

[我的博客](https://blog.forecho.com)

**主要特色：**

- 風格基於 [Tailwind CSS](https://tailwindcss.com/)
- 使用更快的 Chroma 代碼高亮
- 自定義 css，自定義 js，自定義 head
- 文章支持目錄
- 支持相關閱讀

## 誰在用 hugo-theme-echo

- [forecho](https://blog.forecho.com)
- Waiting to add more...

## 如何使用？

**注意：** 這個教程假設你 **第一次** 使用 [Hugo][] 。 [Hugo][] 是一個非常流行的靜態網站生成工具。 你可查看官方文檔 [Hugo Official Docs][] 獲取更多幫助。

[Hugo]: https://gohugo.io/
[Hugo Official Docs]: https://gohugo.io/getting-started/



### 快速安裝 Hugo

從 [Hugo Releases](https://github.com/gohugoio/hugo/releases) 上直接下載安裝適合你的版本。



### 快速創建網站

```bash
hugo new site myBlog
```

上面的命令將會在一個名爲 `myBlog`  的文件夾中創建一個新的 hugo 站點。



### 快速使用 

把這個主題克隆到 `themes` 文件夾

```bash
cd myBlog
git submodule add https://github.com/forecho/hugo-theme-echo.git --depth=1 themes/echo
```

站點設置示例：

```toml
baseURL = "http://localhost:1313"
languageCode = "en-us"
title = "Forecho's Blog"
theme = "echo"
DefaultContentLanguage = "cn"
# 自動檢測是否包含中文/日文/韓文，該參數會影響摘要和字數統計功能，建議設置爲true
hasCJKLanguage = true
# 設置頁面生成形式，將默認的網站路徑/修改成.html
uglyURLs = true
googleAnalytics = ""      # UA-XXXXXXXX-X

## 評論系統
changyanAppid = "" # Changyan app id             # 暢言
changyanAppkey = "" # Changyan app key
disqusShortname = "forecho-blog" # disqus account name
livereUID = "" # LiveRe UID                  # 來必力

[markup.highlight]
codeFences = true # 高亮markdown的代碼塊
guessSyntax = true # 高亮markdown中沒有標註語言的代碼塊
hl_Lines = ""
lineNoStart = 1
lineNos = true
lineNumbersInTable = true
noClasses = true
style = "manni"
tabWidth = 2

# https://gohugo.io/content-management/urls/#aliases
[permalinks]
posts = "/:filename"

[outputFormats.RSS]
mediatype = "application/rss"
baseName = "atom"

[services.rss]
limit = 20

[author]
name = "forecho"
avatar = "https://avatars0.githubusercontent.com/u/1725326?s=460&v=4"
bio = "7年開發經驗，尋求技術 Leader 工作機會。Wechat: ipzone"
homepage = "https://forecho.io/"

[params]
favicon = "https://avatars0.githubusercontent.com/u/1725326?s=460&v=4"
keywords = "Hugo, theme, echo"
description = "Hugo theme echo example site."
toc = true
navItems = [
  ["HOME", "/"],
  ["ARCHIVE", "/posts.html"],
  ["ABOUT", "/about.html"],
  ["RSS", "/atom.xml"]
]
# rss 全文輸出
rssFullContent = true
uglyURLs = true
busuanzi = true # 是否使用不蒜子統計站點訪問量
staticCDNPrefix = "https://cdn.bootcss.com/font-awesome/5.11.2"
extraHead = '<script async src="https://www.googletagmanager.com/gtag/js?id=UA-xxx"></script>'
postAds = ""
profileAds = '<div class="bg-white shadow"><img class=" object-cover w-auto mx-auto mt-6" src="https://blog-1251237404.cos.ap-guangzhou.myqcloud.com/20190424153337.png" alt="微信打賞"></div>'
notFoundAds = ''

# 開啓版權聲明，協議名字和鏈接都可以換
[params.cc]
name = "署名-非商業性使用 4.0 國際 (CC BY-NC 4.0)"
link = "https://creativecommons.org/licenses/by-nc/4.0/deed.zh"

# 文章打賞
[params.reward]
enable = true
title = "打賞"
wechat = "https://blog-1251237404.cos.ap-guangzhou.myqcloud.com/20190424153510.png" # 微信二維碼
alipay = "https://blog-1251237404.cos.ap-guangzhou.myqcloud.com/20190424153431.png" # 支付寶二維碼

############## 評論系統  start ##############
[params.gitment] # Gitment is a comment system based on GitHub issues. see https://github.com/imsun/gitment
owner = "" # Your GitHub ID
repo = "" # The repo to store comments
clientId = "" # Your client ID
clientSecret = "" # Your client secret

[params.utterances] # https://utteranc.es/
owner = "" # Your GitHub ID
repo = "" # The repo to store comments

[params.gitalk] # Gitalk is a comment system based on GitHub issues. see https://github.com/gitalk/gitalk
owner = "" # Your GitHub ID
repo = "" # The repo to store comments
clientId = "" # Your client ID
clientSecret = "" # Your client secret

# Valine.
# You can get your appid and appkey from https://leancloud.cn
# more info please open https://valine.js.org
[params.valine]
enable = false
appId = '你的appId'
appKey = '你的appKey'
notify = false # mail notifier , https://github.com/xCss/Valine/wiki
verify = false # Verification code
avatar = 'mm'
placeholder = '說點什麼吧...'
visitor = false

############ 評論系統  end ##############
## 社交鏈接
[social]
github = "forecho"
jsfiddle = "forecho"
codepen = "forecho"
dribbble = "forecho"
behance = "forecho"
flickr = "forecho"
instagram = "forecho"
youtube = "forecho"
vimeo = "forecho"
vine = "forecho"
medium = "forecho"
wordpress = "forecho"
tumblr = "forecho"
linkedin = "forecho"
slideshare = "forecho"
stackoverflow = "forecho"
reddit = "forecho"
pinterest = "forecho"
weibo = "forecho"
facebook = "forecho"
twitter = "caizhenghai"
douban = "ipzone"
rss = "/atom.xml"
```

啓動 hugo server ：

```bash
hugo server -D
```

打開 http://localhost:1313/ ，你將會看到一個示例網站。



### 開始你的博客

默認配置文件 `config.toml` 位於你的網站的根目錄，請按自身需要進行定製。

默認的文章文件位於 `./content/posts` 目錄。


### 生成你的網站

直接運行 `hugo` ，將會自動生成你的網站到 `public/` 目錄。

如果你有額外的時間，並且想更多的瞭解 [Hugo][] ，請查閱官方文檔 [Hugo Official Docs][] 。


## 單篇文章的設置

**Front Matter** : Hugo 允許你使用 yaml， toml 或者 json 語法在你每一篇文章的開頭進行設置。

**YAML 示例：**

```yaml
---
# 常用定義
title: "An Example Post"           # 標題
date: 2018-01-01T16:01:23+08:00    # 創建時間
lastmod: 2018-01-02T16:01:23+08:00 # 最後修改時間
draft: false                       # 是否是草稿？
tags: ["tag-1", "tag-2", "tag-3", "popular"]  # 標籤
categories: ["index"]              # 分類
author: "forecho"                  # 作者

# 用戶自定義
# 你可以選擇 關閉(false) 或者 打開(true) 以下選項
comment: false   # 關閉評論
toc: false       # 關閉文章目錄
reward: false	 # 關閉打賞
---
```

## 關於熱門文章

如果標籤裏面含有 `popular` 就會自動出現再熱門文章列表中，目前熱門文章只會在側邊欄和404頁面展示，熱門文章列表最多展示5篇文章。

## 感謝

本主題參考了以下主題的部分代碼：

- [hugo-theme-even](https://github.com/olOwOlo/hugo-theme-even)
- [hugo-theme-jane](https://github.com/xianmin/hugo-theme-jane)

## License

Hugo-theme-echo is licensed under the MIT license. Check the [LICENSE](LICENSE.md) file for details.