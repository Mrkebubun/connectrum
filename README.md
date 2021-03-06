Connectrum
----------

Stratum (electrum-server) Client Protocol library
=================================================

Uses python3 to be a client to the Electrum server network. It makes heavy use of
`asyncio` module and newer Python 3.5 keywords such as `await` and `async`.

For non-server applications, you can probably find all you need
already in the standard Electrum code and command line.

Python 3.5 is absolutely required for this code. It will never work
on earlier versions of Python.


Features
========

- can connect via Tor, SSL, proxied or directly
- filter lists of peers by protocol, `.onion` name
- manage lists of Electrum servers in simple JSON files.
- fully asynchronous design, so can connect to multiple at once
- a number of nearly-useful examples provided

Examples
========

In `examples` you will find a number little example programs.

- `cli.py` send single commands, plan is to make this an interactive REPL
- `subscribe.py` stream changes/events for an address or blocks.
- `explorer.py` implements a simplistic block explorer website
- `spider.py` find all Electrum servers recursively, read/write results to JSON


TODO List
=========

- be more robust about failed servers, reconnect and handle it.
- connect to a few (3?) servers and compare top block and response times; pick best
- some sort of persistant server list that can be updated as we run
- type checking of parameters sent to server (maybe)?
- lots of test code
- an example that finds servers that do SSL with self-signed certificate
- an example that fingerprints servers to learn what codebase they use
- some bitcoin-specific code that all clients would need; like block header to hash
