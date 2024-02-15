# 📶 DNS

DNS (**D**omain **N**ame **S**ystem): The phonebook of the internet, translating human-friendly domain names into IP addresses that computers use to identify each other on the network.

## History

The DNS was introduced in 1983 by Paul Mockapetris and Jon Postel, and it was designed to replace the HOSTS.TXT file that was used to map domain names to IP addresses.

The HOSTS.TXT file was a manually maintained file that quickly became unmanageable as the internet grew, leading to the development of a distributed and hierarchical naming system that we now know as the DNS.

## Structure

The DNS is a hierarchical and decentralized system that consists of multiple components, including:

### Root Servers

The root servers are the first step in the DNS resolution process, and they are responsible for providing the IP addresses of the top-level domain (TLD) servers.

### Top-Level Domain (TLD) Servers

The TLD servers are responsible for providing the IP addresses of the authoritative name servers for each domain within their TLD.

### Authoritative Name Servers

The authoritative name servers are responsible for providing the IP addresses of the name servers for a specific domain.

### Recursive Resolvers

The recursive resolvers are responsible for resolving domain names on behalf of clients, and they are typically operated by internet service providers (ISPs) or other network administrators.

### Caching Resolvers

The caching resolvers are responsible for caching the results of DNS queries, which helps to reduce the load on the root and TLD servers.

## Resolution Process

When a client wants to resolve a domain name, it follows a multi-step process that involves querying the root servers, TLD servers, and authoritative name servers to obtain the IP address of the domain.

The resolution process is as follows:

1. The client sends a query to the recursive resolver, asking for the IP address of the domain.
2. The recursive resolver checks its cache to see if it has the IP address for the domain.
3. If the IP address is not in the cache, the recursive resolver sends a query to the root servers, asking for the IP address of the TLD servers for the domain.
4. The root servers respond with the IP addresses of the TLD servers.
5. The recursive resolver sends a query to the TLD servers, asking for the IP address of the authoritative name servers for the domain.
6. The TLD servers respond with the IP addresses of the authoritative name servers.
7. The recursive resolver sends a query to the authoritative name servers, asking for the IP address of the domain.
8. The authoritative name servers respond with the IP address of the domain, and the recursive resolver caches the result.
9. The recursive resolver sends the IP address to the client, and the client can now connect to the domain.
10. The client caches the IP address for future use.
