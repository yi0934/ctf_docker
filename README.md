# ctf_docker
for ctfer play pwn and reverse

# Usage
## replace libc
patchelf --set-interpreter ./ld-2.23.so ./app

patchelf --replace-needed  libc.so.6 ./libc.so.6 ./app

## connect by xpra
xpra start --start=gnome-terminal --bind-tcp=0.0.0.0:14500

xpra attach tcp://127.0.0.1:14500/
