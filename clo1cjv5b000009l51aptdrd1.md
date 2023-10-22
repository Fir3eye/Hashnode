---
title: "Terminal Banner"
seoTitle: "Bash Banner"
datePublished: Sun Oct 22 2023 10:49:30 GMT+0000 (Coordinated Universal Time)
cuid: clo1cjv5b000009l51aptdrd1
slug: terminal-banner
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697971623773/2e20b70f-670a-4efb-9b3a-4726750f6e0e.png
tags: bash, bash-shell-script

---

## Create a Banner for our Terminal

![image](https://github.com/Fir3eye/Bash_Script/assets/93431222/586d399a-ac6b-47df-8f4d-0e4d9610d215 align="center")

## First you need to install the figlet and lolcat

```bash
which figlet 
apt install figlet 
apt install lolcat
```

## Write your own script

```bash
touch banner.sh 
vi banner.sh
```

## Banner Script

```bash
#!/bin/bash
figlet -f slant "Terminal Name" | lolcat 
figlet -f digital "Description of your terminal" | lolcat 
```

## Save file and use Sudo su

* press 'esc'
    
* press ':'
    
* press 'wq' Enter
    
* sudo su
    

## Give the Permissions

```bash
chmod +x banner.sh
```

## Check Script -----&gt; Working or Not

```bash
./banner.sh
```

## Now Set the banner in your Terminal Background

```bash
vi ~/.bashrc
```

## Add script in bashrc file in the last section

```bash
#!/bin/bash
figlet -f slant "Your Terminal Name" | lolcat 
figlet -f digital "Description of our terminal" | lolcat 
```

## If not working reboot the terminal

```bash
reboot
```

## Result

![image](https://github.com/Fir3eye/Bash_Script/assets/93431222/586d399a-ac6b-47df-8f4d-0e4d9610d215 align="left")