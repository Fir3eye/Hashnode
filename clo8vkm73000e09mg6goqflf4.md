---
title: "FLP - Figlet Font File"
datePublished: Fri Oct 27 2023 17:16:21 GMT+0000 (Coordinated Universal Time)
cuid: clo8vkm73000e09mg6goqflf4
slug: flp-figlet-font-file
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698425106539/2034d148-0b18-4360-8e33-bc9b4bf8fa9a.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1698426866253/7b5ffb81-b285-4894-872f-65e4221f12a8.png
tags: bash, script, figlet-font-file, figlet, lolcat

---

> **Install figlet**

```bash
apt install figlet
apt install lolcat 
```

> **You will face this Error if the file is not present**

```bash
figlet -d doom "Sen DevOps"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698426715723/724368dc-2b60-446c-a17a-22224e4209ca.png align="center")

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Error - figlet: umscript: Unable to open font file</strong></div>
</div>

> Fix this

* Step -1. Go to the figlet directory
    

```bash
/usr/share/figlet
touch doom.flf
vi doom.flf
# copy to flf file
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698426679379/6ea8a617-8845-4780-9bc8-e2e22f09a7a1.png align="center")

* Step-2. Create your own font style file like doom.flf
    

```bash
https://github.com/hIMEI29A/FigletFonts.git
```

* Step-3. Let's try Again
    

```bash
figlet -f doom "Sen DevOps"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698426645366/d23a0547-acad-46a6-9bf3-9f2a74dbdaa1.png align="center")

```bash
figlet -f doom "Sen DevOps" | lolcat
figlet -f digital "Like Share Subscribe" | lolcat
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698426621971/5ec86d7b-4c2e-485a-813d-9436ff9bc5ae.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698426370251/cecd1d96-32e7-4ca9-b1c7-b09564df0457.png align="center")

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Repeat this step and add any type of font in our figlet directory and enjoy :-)</strong></div>
</div>