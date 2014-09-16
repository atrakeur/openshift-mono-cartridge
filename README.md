# Mono cartridge for openshift

## Provides:

Mono runtime env
Openshift integration scripts
NO webserver
NO implementation

## Cases of use

This implementation is perfect for realtime servers. For standard webservers, please look at ASP.Net implementation in openshift.
However, the implementation of the server itself is up to you. This package provides only with the mono environnement, and run scripts needed by openshift.
This approach give you more control over your server because you can now use any piece of code that comply with http standards.
Server must be allready compiled as compilation isn't handled by the cartridge (and is maybe too costly?)

## How to use:

In openshift, just create a cartridge using the following manifest URL:

https://raw.github.com/atrakeur/openshift-mono-cartridge/master/metadata/manifest.yml

This cartridge comes with a full mono runtime environement. A simple application that output hello is provided.

If you try to load your cartridge url in your browser, you have to see that hello.

Now you just have to create a console app in C# that will listen for http requests. Websockets are available of course! (that the whole point of this btw)

##Flaws

All the server implementation is up to you.
The server executable must be named Server.exe and not something else.
The server must comply with openshift ip bindings.
The server must comply with http standards (websockets allowed)
