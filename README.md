# maya-arnold
## Install
### 1. Clone this source.
`cd /tmp`
#### Choose one:
#### A. Git HTTPS 
`git clone https://github.com/aaronrancsik/maya-arnold-arch.git`
#### B. Git SSH 
`git clone git@github.com:aaronrancsik/maya-arnold-arch.git`
### 2. Get the source zip.
`cd /tmp/maya-arnold-arch`

`cp /tmp/maya20221_BIG/Packages/package.zip /tmp/maya-arnold-arch/`
### 3. Create & install the package.
`makepkg -s`

`sudo pacman -U maya-arnold-4.2.3-1-x86_64.pkg.tar.zst`

### 4. It's done.
