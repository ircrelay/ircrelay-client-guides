## Textual IRCRelay Set-up Guide

### Get the Client

First, you'll need do download and install [irssi](http://www.irssi.org/).

### Adding the Server

We'll assume that you're setting up a connection to freenode and have used the standard convention of ```<username>_<irc network name>``` e.g. ```pearkes_freenode```.

```/SERVER ADD -auto -ssl -ssl_verify -network IRCRelay irc.ircrelay.com 6697```
```/NETWORK ADD -user pearkes_freenode IRCRelay```

If you don't mind your IRCRelay password being available in clear text, you could amend the ```/SERVER``` command to include your password as so.

```/SERVER ADD -auto -ssl -ssl_verify -network IRCRelay irc.ircrelay.com 6697 <your IRCRelay password>```

### Connect

To start your connection to IRCRelay just use ```/CONNECT IRCRelay```.

If you didn't specify your irc password, you'll be prompted to provide on the initial connection and can use the following command: ```/QUOTE PASS <IRCRelay <your IRCRelay password>```

Incidentally when you next start up irssi, you'll automatically connect to IRCRelay.

### Support

If you're having trouble, please visit the [support](https://www.ircrelay.com/support) page.
