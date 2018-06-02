NAME:
    mydig - DNS lookup utility

USAGE:
    ./mydig <domain> [<rdtype>]

DESCRIPTION:
    mydig is a flexible tool for interrogating DNS name servers. mydig performs 
    DNS lookups and displays the answers that are returned from the name 
    server(s) that were queried.

    mydig will always try each of the root servers listed in 
    https://www.iana.org/domains/root/servers namely the following:
    a.root-servers.net (198.41.0.4)
    b.root-servers.net (199.9.14.201)
    c.root-servers.net (192.33.4.12)
    d.root-servers.net (199.7.91.13)
    e.root-servers.net (192.203.230.10)
    f.root-servers.net (192.5.5.241)
    g.root-servers.net (192.112.36.4)
    h.root-servers.net (198.97.190.53)
    i.root-servers.net (192.36.148.17)
    j.root-servers.net (192.58.128.30)
    k.root-servers.net (193.0.14.129)
    l.root-servers.net (199.7.83.42)
    m.root-servers.net (202.12.27.33)

SIMPLE USAGE:
    A typical invocation of mydig looks like:
        ./mydig domain rdtype

    where:
        domain - is the name of the resource record that is to be looked up.
        rdtype - indicates what type of query is required — A, MX and NS. 
                 If no type argument is supplied, mydig will perform a lookup for an A record.

OUTPUT:
    It outputs the Answer section returned as a response for a DNS query. 
    Along with this it prints extra information like Query Time, Root Server, MSG Size recv and When was the command run 

LANGUAGE USED:
    Python

EXTERNAL LIBRARIES USED:
    dnspython
