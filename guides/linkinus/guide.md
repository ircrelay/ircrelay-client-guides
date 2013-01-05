## Linkinus IRCRelay Set-up Guide

### Get the Client

First, you'll need do download and install [Linkinus](http://conceitedsoftware.com/products/linkinus).

### Adding the Server

When you launch Linkinus for the first time you will be greeted by an empty
window. To add a server click on the "+" button in the bottom left corner.

![Welcome](https://raw.github.com/ircrelay/ircrelay-client-guides/master/guides/linkinus/img/welcome.png)

Click on the "New Network" button, the "New Network" panel will look like this:

![New Network](https://raw.github.com/ircrelay/ircrelay-client-guides/master/guides/linkinus/img/add_network.png)

The Name of the Network is up to you! Since we're setting up a freenode
network, I'm going to call mine IRCRelay Freenode.

Your server and port will match the screenshot.

Make sure to check the Use SSL box.

Your password is the password you signed up for IRCRelay with.

Now click "Ok", Linkinus will try to connect to IRCRelay but it will fail.

Open the preferences window ("Preferences..." from the "Linkinus" menu at the
top), then click "Identities".

![Username Dialog](https://raw.github.com/ircrelay/ircrelay-client-guides/master/guides/linkinus/img/username.png)

The only thing you need to change here is the username field. We will
automatically override the rest with the settings you provided when
congfiguring your network on ircrelay.com.

Make sure to go to the settings page in IRCRelay and verifying the username
for this specific network. It is different then the username you signed up with.

Close the preferences window.

Right click on the network in the connection list and click "Edit
Connection...", this will display the inspector:

![Inspector](https://raw.github.com/ircrelay/ircrelay-client-guides/master/guides/linkinus/img/inspector.png)

Click on the pencil near your name, then select the only available item.

Close the inspector.

### Connect

Last but not least, connect to your server by right clicking on the name of it
in the sidebar and pressing connect:

![Connection Dialog](https://raw.github.com/ircrelay/ircrelay-client-guides/master/guides/linkinus/img/conn_dialog.png)

### Support

If you're having trouble, please visit the [support](https://www.ircrelay.com/support) page..
