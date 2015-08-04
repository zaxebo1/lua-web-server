## Introduction ##

This is a experimental project made to see if I could convert a web server implementation I saw written in Ruby to Lua. As of version 0.1, it only supports the serving of HTML documents.

## Prerequisties ##

This web server requires the Lua interpreter and LuaSocket.
It also needs the [xml parser module](http://code.google.com/p/lua-modules).

## Installing web server ##

You will need to install the Lua interpreter and/or LuaSocket in a location where LuaSocket is accessible by the Lua interpreter. A package containing the Lua interpreter and LuaSocket for Windows is available here (win32lua.zip). Users of other operating systems can find the source code to compile yourself, for both, from the original authors.

Make sure that the path to the interpreter ("lua") is in your operating system's PATH variable or you will have to type the full path in the shell or change the _webs_ script to point to the lua interpreter or run the web server like so:

```
/path/to/lua webserver.lua
```

You can extract the web server from the archive to any location you wish, but the chosen path should be easily accessible from a shell prompt.

## Running web server ##

To run the web server, open a shell prompt and change directory into the directory containing _webserver.lua_.

Start the server with:

```
webs
```

or alternatively:

```
lua webserver.lua
```

The server runs locally on port 8080 and can be accessed in a web browser with http://localhost:8080 or http://127.0.0.1:8080.

HTML files served by the server should be placed in _/www_

## Killing the server ##

The server can be stopped with telnet.
You can connect to the server via telnet from the shell prompt (when in the directory where _webserver.lua_ is located):

```
telin
```

Alternatively, instead of running the _telin_ script, you can do this to connect to the server:

```
telnet localhost 8080
```

Once connected to the server, enter:

```
kill
```