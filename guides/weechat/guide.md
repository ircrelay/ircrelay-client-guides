## WeeChat IRCRelay Set-up Guide

WeeChat is a console based IRC client similar to irssi. It is fast,
lightweight and scriptable in several languages.

### Get the Client

First, you'll need to download and install [weechat](http://www.weechat.org/). If you're on OS X it's available using homebrew:
 
`brew install weechat`

### Adding the Server

We'll use freenode as the example network and assume you use the standard convention of `<username>_<irc network name>` e.g. `user_freenode`.

`/server add IRCRelay irc.ircrelay.com/6697 -ssl -autoconnect -username user_freenode -password <your IRCRelay password>`

This will setup the basic connection details. You may still want to
adjust a few settings for the server. Available settings can be
displayed using:

`/set irc.server.IRCRelay.*`

#### SSL Verify

It's a good idea to enable the ssl verify option with the following:

`/set irc.server.IRCRelay.ssl_verify on`

However, WeeChat by default does not ship with CA information so will be unable to verify
the SSL certificate for irc.ircrelay.com unless you obtain a
certificate bundle. On Linux this is usually the `ca-certificates`
package. On OS X you will want to obtain a certificate bundle from a
trusted location.

One such certificate bundle is available from the
[curl website](http://curl.haxx.se/docs/caextract.html)

WeeChat will look for this certificate bundle by default in the
following location:

`~/.weechat/ssl/CA.pem` 

You can optionally point to a different location than the default by
customizing `weechat.network.gnutls_ca_file` with:

`/set weechat.network.gnutls_ca_file <your custom path>`

### Connect

To start your connection to IRCRelay just use `/connect IRCRelay`.

### Support

If you're having trouble, please visit the
[support](https://www.ircrelay.com/support) page or visit us in `#ircrelay` on freenode.
