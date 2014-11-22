Hide and Seek
=============

Purpose
-------

We are providing a server that is hiding, for clients that are trying to find them.
Once servers are found, they are out of the game and can't be found anymore.

To make sure, clients know which servers they found,
servers are obliged to send the client a unique identifier when they are found.


Server specifications
---------------------

- A server SHOULD accept a tcp-connection on port 5559.
- A server SHOULD accept only one client connection.
- A server SHOULD quit when the client sends any message.
- A server SHOULD send its identifier to the client before quiting.

Client Specification
--------------------

- A client SHOULD connect to a tcp-connection on port 5559.
- A client MAY accept a replay with the identifier of the client.
- A client MAY connect to as much servers as it wants/can.
