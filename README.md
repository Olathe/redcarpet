#### Files
* `redcarpet` automatically accepts the recurring terms-of-service web page for a WiFi router. You'll need to edit it to handle the proper SSID and URL.
* `redcarpet.bat` starts `redcarpet` on Windows.
* `redcarpet.conf` is an Upstart script. It allows you to run `redcarpet` as a system service on Ubuntu.

#### Installing as an Upstart service
To install it, open a shell, switch to the directory containing these files, edit `redcarpet` to make it work for your access point, and execute the following:

```sh
emacs redcarpet # edit redcarpet script so that it works properly
sudo adduser --system --home /nonexistent --shell /bin/false --no-create-home --disabled-password --disabled-login redcarpet
sudo cp redcarpet /usr/local/bin/
sudo cp redcarpet.conf /etc/init/
sudo service redcarpet start
```
#### License
Redcarpet is licensed under <a href="http://www.gnu.org/licenses/gpl.html">GPL 3</a>.