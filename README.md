# reboot

for running kexec

```bash
sudo kexec -l vmlinuz --initrd=initrd --append="ip=dhcp autoinstall 'ds=nocloud-net;s=http://192.168.40.22:8081/'"
sudo systemctl kexec
```

wait for a couple of minutes and then on another machine run:

```bash
ssh -i id_rsa installer@192.168.40.167
```