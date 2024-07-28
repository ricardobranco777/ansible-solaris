
```
sudo pkg install pkg:/package/pkg
sudo pkg set-publisher -g https://pkg.omnios.org/bloody/extra extra.omnios
sudo pkg install pkg:/developer/illumos-tools
sudo pkg install pkg:/developer/omnios-build-tools
sudo pkg install pkg:/ooce/omnios-build-tools
sudo pkg install developer/omni

sudo zfs create -o mountpoint=/build rpool/build
sudo chown $USER /build

/opt/ooce/bin/omni setup /build ricardobranco777

/opt/ooce/bin/omni update_illumos
/opt/ooce/bin/omni update_omnios
/opt/ooce/bin/omni build_illumos
/opt/ooce/bin/omni build_omnios

/opt/ooce/bin/omni build_media
```
