# church-sign
What's showing on the church sign. The computer running the sign pulls from here for updates. It is merely a set of images that are displayed for 5 seconds each.

How it works...
crontab has a git pull that grabs the latest sign from here (https://github.com/kylehutson/church-sign)

.config/lxsession/LXDE-pi/autostart contains the line
@/usr/bin/feh -Y -x -q -D 5 -B black -F -Z -z -r /home/pi/church-sign
This starts the display on startup.
