# vinyl-stream
A collection of files for setting up an Icecast streaming server to stream vinyl records.

```bash
apt update
apt install icecast2 ices2
mkdir /var/log/ices
mkdir /etc/ices2
mv icecast2/icecast.xml /etc/icecast2/icecast.xml
mv ices2/ices-alsa.xml /etc/ices2/ices-alsa.xml
mv ices2/ices2.service /etc/systemd/system/ices2.service
systemctl daemon-reload
sysemtctl start ices2.service
```
