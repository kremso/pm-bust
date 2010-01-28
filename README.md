Hibernating after a kernel update is one of the biggest mistakes one can make in linux. Hibernated machine fails to load from the image causing data/session and sometimes even hair loss.

pm-bust is a simple wrapper around pm-hibernate to detect and warn you about this situation. It's intended to work with Archlinux and won't work in any other distribution.

Installation
------------

    sudo mv /usr/sbin/{pm-hibernate,pm-hibernate-original}
    sudo ln -s pm-bust/pm-hibernate /usr/sbin/pm-hibernate


Pro tip
-------

If you hibernate with a hotkey, bind it to `pm-hibernate -gui` - you'll get a gtk dialog window

Uninstallation
--------------
    sudo rm /usr/sbin/pm-hibernate
    sudo mv /usr/sbin/{pm-hibernate-original,pm-hibernate}
