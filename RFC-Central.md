Dealer based hide an seek
=====

roles: server, client
port: must be in range 5500-5600

server listens on *:<port>, socket type DEALER
server sends "<name>"       // the <name> is the name of the server
    // this is a blocking call for the server; it waits until is discovered


client connects DEALER to <ip>:<port>
client reads "<name>"
    // client prints the name of the found server
    // at this point the server will terminate - it has been found
