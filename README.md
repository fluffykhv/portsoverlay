# portsoverlay
My own ports overlay

Usage:

Overlay:

Put this line in /etc/make.conf:
OVERLAYS+=/path/to/portsoverlay
Build ports

For poudriere:
sudo poudriere ports -c -F -p portoverlay
cd ${LOCALBASE}/poudriere/ports/portsoverlay
git clone https://github.com/fluffykhv/portsoverlay .
poudriere bulk -j 121amd64 -p portstree -O portsoverlay category/port 
