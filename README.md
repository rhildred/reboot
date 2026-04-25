# reboot

for running kexec

```
sudo kexec -l vmlinuz \
  --initrd=initrd \
  --append="ip=dhcp cloud-config-url=https://rhildred.github.io/reboot/ ds=nocloud-net;s=https://rhildred.github.io/reboot/ autoinstall"
sudo systemctl kexec
```