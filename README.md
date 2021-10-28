# maya-arnold

## Install
### 1. Clone it.
Select a dir
`cd /tmp`
#### Choose one:
#### A. Git HTTPS 
`git clone https://github.com/aaronrancsik/maya-arnold-arch.git`
#### B. Git SSH 
`git clone git@github.com:aaronrancsik/maya-arnold-arch.git`
### 2. Download the source 
`cd /tmp/maya-arnold-arch`

`cd /tmp && wget -O MtoA-5.0.0-linux-2022.run shorturl.at/wzFJ3`

[Official Link](https://wdown.solidangle.com/mtoa/MtoA-5.0.0-linux-2022.run)
### 3. Extract it

Choose one:
#### A. Official extractor.
`chmod +x MtoA-5.0.0-linux-2022.run`

`./MtoA-5.0.0-linux-2022.run --noexec --nox11 --keep --target ./`
#### B. Manually. No sketchy hundreds lines of mysterious scrip executed.
##### Strip out the built in script to get the real source.
`tail -c +9476 MtoA-5.0.0-linux-2022.run > MtoA.tar.gz`

*Note the **9476** is the fix byte number where tar.gz content begins. Use `binwalk` for help if you have different version.*
##### Extract
`tar zxvf MtoA.tar.gz`


### 2. Create & install the package.
`makepkg -s`

`sudo pacman -U maya-arnold-5.0.0-1-x86_64.pkg.tar.zst`

### 4. It's done.
