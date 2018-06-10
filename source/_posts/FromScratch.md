---
title: Hexo from scratches
date: 2018-06-09 01:55:39
tags:
---
Lets install same amaizinf, fast blog as you using right now!

### Installation base
* Install node.js here https://nodejs.org/en/
* Install git here https://git-scm.com/

### Installation hexo-cli on PC
``` ruby
$ npm install hexo-cli -g
```

## Init new project
```ruby
$ hexo init SkillingUp
INFO  Cloning hexo-starter to E:\tests\SkillingUp
Cloning into 'E:\tests\SkillingUp'...
remote: Counting objects: 65, done.
remote: Total 65 (delta 0), reused 0 (delta 0), pack-reused 65
Unpacking objects: 100% (65/65), done.
Submodule 'themes/landscape' (https://github.com/hexojs/hexo-theme-landscape.git) registered for path 'themes/landscape'
Cloning into 'E:/tests/SkillingUp/themes/landscape'...
remote: Counting objects: 819, done.
remote: Total 819 (delta 0), reused 0 (delta 0), pack-reused 819
Receiving objects: 100% (819/819), 2.54 MiB | 987.00 KiB/s, done.
Resolving deltas: 100% (433/433), done.
Submodule path 'themes/landscape': checked out '73a23c51f8487cfcd7c6deec96ccc7543960d350'
INFO  Install dependencies
▒▒▒▒▒▒▒▒▒▒: ▒▒ 㤠▒▒▒▒ ▒▒▒▒ 䠩▒▒ ▒▒ ▒▒▒▒▒▒▒ 蠡▒▒▒▒▒.
npm WARN deprecated titlecase@1.1.2: no longer maintained

> nunjucks@3.1.3 postinstall E:\tests\SkillingUp\node_modules\nunjucks
> node postinstall-build.js src

npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@1.2.4 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.4: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})

added 400 packages in 34.151s
INFO  Start blogging with Hexo!
```

Enter in you new build project
```ruby
$ cd SkillingUp
```
Checking is it not empty
```ruby
$ ls
_config.yml    package.json       scaffolds/  themes/
node_modules/  package-lock.json  source/
```
Starting server for check is it working?
```ruby
$ hexo server
INFO  Start processing
INFO  Hexo is running at http://localhost:4000/. Press Ctrl+C to stop.
INFO  See you again
```
Must see this picture...
![Test ok](./../../../../images/hexo- test site.png "Test ok")

You can stop server.

## Generate static files for uploading to server
Edit `_config yml`
```ruby
15 # url: http://yoursite.com/child
16 # root: /child/
17 url: http://yoursite.com/
18 root:
```
Line 18 will add path to all yours css files and js scripts. if you had problems with styles, you must look here.
```ruby
$ hexo generate
INFO  Start processing
INFO  Files loaded in 191 ms
INFO  Generated: index.html
INFO  Generated: archives/index.html
INFO  Generated: fancybox/blank.gif
INFO  Generated: fancybox/jquery.fancybox.css
INFO  Generated: fancybox/jquery.fancybox.pack.js
INFO  Generated: fancybox/jquery.fancybox.js
INFO  Generated: archives/2018/index.html
INFO  Generated: fancybox/fancybox_overlay.png
INFO  Generated: fancybox/fancybox_sprite.png
INFO  Generated: fancybox/fancybox_sprite@2x.png
INFO  Generated: fancybox/fancybox_loading.gif
INFO  Generated: fancybox/fancybox_loading@2x.gif
INFO  Generated: archives/2018/06/index.html
INFO  Generated: css/fonts/FontAwesome.otf
INFO  Generated: fancybox/helpers/jquery.fancybox-media.js
INFO  Generated: js/script.js
INFO  Generated: fancybox/helpers/jquery.fancybox-buttons.css
INFO  Generated: fancybox/helpers/jquery.fancybox-buttons.js
INFO  Generated: fancybox/helpers/jquery.fancybox-thumbs.css
INFO  Generated: fancybox/helpers/jquery.fancybox-thumbs.js
INFO  Generated: css/style.css
INFO  Generated: fancybox/helpers/fancybox_buttons.png
INFO  Generated: css/fonts/fontawesome-webfont.eot
INFO  Generated: css/fonts/fontawesome-webfont.woff
INFO  Generated: css/images/banner.jpg
INFO  Generated: css/fonts/fontawesome-webfont.ttf
INFO  Generated: css/fonts/fontawesome-webfont.svg
INFO  Generated: 2018/06/04/hello-world/index.html
INFO  28 files generated in 828 ms

```
before

![before generate](./../../../../images/before-generate.png "before generate")

after

![after generate](./../../../../images/after-SkillingUp.png "after generate")


## Deploy project
So you got public folder, you can deploy manually by copy-paste your public folder to any server or you can install hexo deployer, witch will deploy(upload) it automaticaly after `hexo delpoy` command will entered.
```ruby
$ npm install hexo-deployer-git --save
npm WARN deprecated swig@1.4.2: This package is no longer maintained
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@1.2.4 (node_modules\fsevents):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@1.2.4: wanted {"os":"darwin","arch":"any"} (current: {"os":"win32","arch":"x64"})
+ hexo-deployer-git@0.3.1
added 31 packages in 9.295s
```


Edit `_config yml`
```ruby
81 deploy:
82  type: git
83  repo: https://github.com/EvilEpicCoder/m4sterbunny.github.io.git
84  branch: master
84  message: update
```
---
