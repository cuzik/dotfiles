## Intall terminator

sudo apt install terminator

##

sudo apt install git cmake libpq-dev

# with snap

## vscode

### install

sudo snap install --classic code

## remove

sudo snap remove code

## slack

### install

sudo snap install --classic slack

## remove

sudo snap remove slack

## spotify

### install

sudo snap install --classic spotify

## remove

sudo snap remove spotify



# with deb

## chrome

### install

sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo apt-get update
sudo apt-get install google-chrome-stable

### remove

sudo apt-get remove google-chrome-stable



# i3

## display settings


### arandr

```sh
sudo apt install arandr
```

add config file

```
exec sh ~/.screenlayout/initial_poisition.sh
```


## barra de status

### i3status

```sh
sudo apt install i3status
```

### i3blocks

```sh
sudo apt install i3blocks
```

## lock screen

### i3lock

```sh
sudo apt install i3lock
```

## touchpad

```
sudo mkdir -p /etc/X11/xorg.conf.d && sudo tee <<'EOF' /etc/X11/xorg.conf.d/90-touchpad.conf 1> /dev/null
Section "InputClass"
        Identifier "touchpad"
        MatchIsTouchpad "on"
        Driver "libinput"
        Option "Tapping" "on"
        Option "TappingButtonMap" "lrm"
        Option "NaturalScrolling" "on"
        Option "ScrollMethod" "twofinger"
EndSection

EOF
```


## transparent windowns

### compton

```
sudo apt install compton
```


## backlights screen

### light

https://github.com/haikarainen/light

download https://github.com/haikarainen/light/releases/

and

```
tar xf light-x.yy.tar.gz
cd light-x.yy/
./configure && make
sudo make install
```
