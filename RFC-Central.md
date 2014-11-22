Dealer based hide an seek
=====

roles: server, client
port: must be in range 5500-5600

server listens on *:<port>, socket type DEALER

server responds w/ "<secret>" to first request      // the <secret> is a fun catch phrase
    // this is a blocking call for the server; it waits until is discovered
server responds w/ "Too late, secret was <secret> but it's taken" to any subsequent request
    // Secret value should be secret :)


client connects DEALER to <ip>:<port>
client reads "<secret>"
    // client collects the name of the found server
