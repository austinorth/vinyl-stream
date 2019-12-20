# vinyl-stream
A collection of files for setting up an Icecast streaming server to
stream vinyl records.

Run the following as `root` or with `sudo` on the Pi:

```bash
apt update
apt install icecast2 ices2 apache2 -y
mkdir /var/log/ices
mkdir /etc/ices2
mv icecast2/icecast.xml /etc/icecast2/icecast.xml
mv ices2/ices-alsa.xml /etc/ices2/ices-alsa.xml
mv ices2/ices2.service /etc/systemd/system/ices2.service
systemctl daemon-reload
systemctl enable ices2.service
sysemtctl start ices2.service
```

Now plug your USB turntable into the Pi and start playing something.
Then open the IP address and port for the Pi in your web browswer to
listen!  Should look something like this:

http://192.168.1.101:8000

You can find the Pi's IP address by running the command `ip addr` from
your terminal session on the Pi.

You can also set up a simple Apache webserver on the Pi to host the
stream on a custom webpage rather than listening from the Icecast page
if you want. If there is demand for this, I will add resources and
instructions to this readme. Enjoy!

--Austin
