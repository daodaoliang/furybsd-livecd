# furybsd-livecd
LiveCD builder for FuryBSD

## Install git required for furybsd-ports

```
pkg install git
```

## Customize
Add more packages to XFCE edition:
```
edit settings/packages.xfce
```

Enable more services:
```
edit settings/rc.conf.xfce
```

## Build a new release to generate tag
Generate an ISO with XFCE:
```
./build.sh
```
Generate an ISO with Gnome3:
```
./build.sh gnome
```
Generate an ISO with KDE Plasma 5:
```
./build.sh kde
```

## Release engineering only push tag to github
```
git clone git@github.com:furybsd/furybsd-ports.git
```

```
cd furybsd-ports && ./tagports.sh
```

## Build a release from the latest tag

```
./release.sh
```

## Burn

Burn the XFCE image to cd:
```
pkg install cdrtools
cdrecord /usr/local/furybsd/iso/FuryBSD-12.0-XFCE.iso
```

Write the XFCE image to usb stick:
```
sudo dd if=/dev/usr/local/furybsd/iso/FuryBSD-12.0-XFCE.iso of=/dev/da0 bs=4m
```

## Credentials for live media
liveuser: furybsd

root: furybsd
