# reboot

for running kexec

```bash
sudo kexec -l vmlinuz \
  --initrd=initrd \
  --append="ip=dhcp cloud-config-url=https://rhildred.github.io/reboot/ ds=nocloud-net;s=https://rhildred.github.io/reboot/ autoinstall"
sudo systemctl kexec
```

wait for a couple of minutes and then on another machine run:

```bash
ssh -i id_rsa installer@192.168.40.167
```