`redcarpet` handles the passwordless login page for a WiFi router. You'll need to edit it to handle the proper SSID and URL.

`redcarpet.conf` is an Upstart script. It allows you to run redcarpet as a system service.

To install it, switch to the directory containing these files and run:

    sudo adduser --system --home /nonexistent --shell /bin/false --no-create-home --disabled-password --disabled-login redcarpet
    sudo cp redcarpet /usr/local/bin/
    sudo cp redcarpet.conf /etc/init/
    sudo service redcarpet start
