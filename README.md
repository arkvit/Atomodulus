# Atomodulus
Cross platform application bridge framework.
The purpose of this framework is to enable apps to interact with eachother

The framework can be seperated into five major components

# (1) Atomodulus Api Server
The api server is a IPC enabled service that handles communication between a client and an app that has an AAIP.
This server enables IPC enabled apps to interact with apps that have AAIP.

# (2) AAIP - Atomodulus App Integration Plugin
This is a interface for plugins that will be integrated into 3rd party applications.
The plugin registers with The Api Server and exposes the Api Schema for its hosting app to be consumed.
It also lunches Plugin Modules for the particular app.

For example:
- If app A is Microsoft Word
- App B is a custom App that has the purpose of finding all images in current loaded document of app A.
- App A has an AAIP in the form of a COM PLugin.
- This AAIP registers with the server and exposes Api calls
- App B requests Api calls to App A through The Api Server.
- The Api Server makes the request and delivers the response to App B.

# (3) Atomodulus Explorer
This executable handles all UI drawing and desktop management of Atomodulus Apps.

# (4) Atomodulus Explorer Server
IPC service that is responsible for all proccess handling.
Notifies Atomodulus Explorer of all proccess activity and information about proccesses on watchlist.

# (5) Atomodulus App
Is an app that based on web technologies and is managed by the Atomodulus Explorer.
Atomodulus App can overlay another app or be glued to another native window.
Act as an universal plugin for other 3rd party applications. As it can use the Atomodulus Api server
to communicate with an other app and interact with it.

# A framework that aims to bridge the gap between softwares and able rapid development of plugins for applications
