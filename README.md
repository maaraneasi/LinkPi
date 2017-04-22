# LinkPi
This is a placeholder repository for the upcoming LinkPi suite which could be installed on a Raspberry Pi3 to create a fully working Pioneer Pro DJ Link bridge to Ableton Link and wireless AP.

The **LinkPi** uses a version of **Carabiner** (https://github.com/brunchboy/carabiner) compiled for ARM to communicate with the **Ableton Link** (https://github.com/Ableton/link) and a lightweight Pioneer Pro DJ Link translator **beat-carabiner** (https://github.com/brunchboy/beat-carabiner).
The current fork of **Carabiner for ARM** (https://github.com/maaraneasi/carabiner), has been compiled using GCC 6.3 and gcc flags *compiled for Raspberry Pi 3 and doesn't support older versions of RPi*. The main reason for not supporting any older version is a built in wifi on RPi 3 - the RPi creates a wifi AP using hostapd so any wireless device can connect and join the Ableton Link. Last but not least is the fact that the RPi 3 is powerfull enough to run the JVM for the beat-carabiner, Carabiner itself and NGINX (or similar, allowing to configure/manage/monitor) this application "stack". In other words - with RPi 3, there is no need to care about the performance or any usb dongle compatibility etc...

The current stage of the project is so called "proof of concept" - it works as expected, but needs some manual effort to start the processes using ssh etc.
The final stage of the project should be an easily installable package, that configures the RPi, installs the necessary packages, downloads the latest versions of the applications, configures the hostapd etc. so the result is a fully headless system, managable using a simple web interface (althought any configuration shouldn't be needed unless you really need to).

Stay tuned!
