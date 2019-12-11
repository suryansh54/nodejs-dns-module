# Node.js DNS Module
The DNS module provides a way of performing name resolutions.

| Method	| Description
--- | --- 
| getServers()	| Returns an array containing all IP addresses belonging to the current server
| lookup()	| Looks up a hostname. A callback function contains information about the hostname, including it's IP address
| lookupService()	| Looks up a address and port. A callback function contains information about the address, such as the hostname
| resolve()	| Returns an array of record types belonging to the specified hostname
| resolve4()	| Looks up an IPv4 address. The callback function includes an array of IPv4 addresses
| resolve6()	| Looks up an IPv6 address. The callback function includes an array of IPv6 addresses
| resolveCname()	| Looks up CNAME records for the specified hostname. The callback function includes an array of available domains for the hostname
| resolveMx()	| Looks up mail exchange records for the specified hostname.
| resolveNaptr()	| Looks up regular expression based records for the specified hostname.
| resolveNs()	| Looks up name server records for the specified hostname.
| resolveSoa()	| Looks up a start of authority record for the specified hostname.
| resolveSrv()	| Looks up service records for the specified hostname.
| resolvePtr()	| Looks up pointer records for the specified hostname.
| resolveTxt()	| Looks up text query records for the specified hostname.
| reverse()	| Reverses an IP address into an array of hostnames
| setServers()	| Sets the IP addresses of the servers

```javascript
const dns = require('dns');

dns.lookup('google.com', (err, address, family) => {
  console.log('address: %j family: IPv%s', address, family);
});
```

```javascript
const dns = require('dns');

console.log(dns.getServers())
```
