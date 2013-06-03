## WeeChat IRCRelay Set-up Guide

WeeChat is a console based IRC client similar to irssi. It is fast, lightweight and scriptable in several languages.

### Get the Client

First, you’ll need to download and install [weechat](http://www.weechat.org/). If you’re on OS X it’s available using homebrew:

`brew install weechat`

### Adding the Server

We’ll use freenode for the example IRCRelay network, and the suggested username convention of `<username>_<irc network name>` e.g. `my-name_freenode`.

`/server add IRCRelay irc.ircrelay.com/6667 -autoconnect`

`/set irc.server.IRCRelay.username my-name_freenode`

`/set irc.server.IRCRelay.password ircrelay-password`

Available settings can be displayed using:

`/set irc.server.IRCRelay.*`

Available settings can be changed using:

`/set irc.server.IRCRelay.SETTING setting-value`

#### SSL Verify

It’s a good idea to use SSL. To do so, use the following to set up your connection to IRCRelay. Note that the port is different and a few additional options are set:

`/server add IRCRelay irc.ircrelay.com/6697 -autoconnect -ssl -ssl_verify`

WeeChat by default does not ship with CA information, so will be unable to verify the SSL certificate for irc.ircrelay.com unless you obtain a certificate bundle. On Linux this is usually the `ca-certificates` package. On OS X you will want to obtain a certificate bundle from a trusted location.

One such certificate bundle is available from the [curl website](http://curl.haxx.se/docs/caextract.html).

WeeChat will probably look for a certificate bundle by default in the following location:

`/etc/ssl/certs/ca-certificates.crt`

You can double check this by issuing the following command in WeeChat:

`/set weechat.network.gnutls_ca_file`

As `/etc/ssl/certs/ca-certificates.crt` probably doesn’t exist, or isn’t writable, point WeeChat at your certificate by issuing the following command:

`/set weechat.network.gnutls_ca_file <your custom path>`

### Connect

To start your connection to IRCRelay just use `/connect IRCRelay`.

### Support

If you’re having trouble, please visit the [support](https://www.ircrelay.com/support) page or visit us in `#ircrelay` on freenode.
