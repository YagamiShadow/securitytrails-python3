# securitytrails-python3
Provides a Python 3.7 wrapper to the SecurityTrails.com API, forked from the [Python 2.7 SDK by secops4thewin](https://github.com/secops4thewin/securitytrails-python)

- ![Version](https://img.shields.io/badge/Version-v1.2.0--beta-orange.svg)
- ![Release](https://img.shields.io/badge/Release-Beta-blue.svg)

## SecurityTrails

### Available API Features 

- `test_connect`:              Test connectivity to API
- `get_domain`:                Get various information about domains
- `get_subdomain`:             Get subdomains for a given domain
- `get_tags`:                  Get tags for a given domain
- `get_whois`:                 Get current WHOIS data for a given domain with the stats merged
- `get_history_dns`:           Get specific historical DNS information for a given domain
- `get_history_whois`:         Get specific historical WHOIS information for agiven domain.
- `ip_explorer`:               Get the neighbors of a given IP address range
- `domain_searcher`:           Filter and search specific records. Using simple filter composition, any type of data fetching is possible. The post object uses a very simple dsl where the json key represents the type to filter on and the value, allowing you to create any number of queries depending on your need. The filters are combined using `AND` and work in combination.
- `domain_searcher_stats`:     Get stats for a given domain search. Contains useful information like tld count, hostname count, domain count, etc.

Not every function is documneted below (they will be soon), but all functions in the SDK are documented with full docstrings, so using something like IPython's `?` or `??` on any given function will provide in-depth details on the API function.

***


**Function**

Initial class instantiation

| Parameter | Details | Required |
| --- | --- | --- |
| api_key | API Key authorising connection | Required
| pretty_print | Converts JSON to syntax-highlight pretty-printed output. Without this set, a dictionary is returned | Not Required (Default Set) |
| base_url | API URL. Defaults to `https://api.securitytrails.com/v1/` | Not Required (Default Set) |

#### get_domain

**Function**

Domain information endpoints that return various information about domains.

**Usage**

| Parameter | Details | Required |
| --- | --- | --- |
| domain | The domain that you are requesting | Required |

**Example**

```
s = SecurityTrails(api_key='yourapikey')
s.get_history_whois("netflix.com")
```

***

#### get_subdomain

**Function**

Returns subdomains for a given domain.

**Usage**

| Parameter | Details | Required |
| --- | --- | --- |
| domain | The domain that you are requesting | Required |

**Example**

```
s = SecurityTrails(api_key='yourapikey')
s.get_subdomain("netflix.com")
```

***

#### get_tags

**Function**

Returns tags for a given domain.

**Usage**

| Parameter | Details | Required |
| --- | --- | --- |
| domain | The domain that you are requesting | Required |

**Example**

```
s = SecurityTrails(api_key='yourapikey')
s.get_tags("netflix.com")
```

***

#### get_whois

**Function**

Returns the current WHOIS data about a given domain with the stats merged together.

**Usage**

| Parameter | Details | Required |
| --- | --- | --- |
| domain | The domain that you are requesting | Required |

**Example**
```
s = SecurityTrails(api_key='yourapikey')
s.get_whois("netflix.com")
```

***

#### ip_explorer

**Function**

Returns the neighbors in any given IP level range and essentially allows you to explore closeby IP addresses.

**Usage**

| Parameter | Details | Required |
| --- | --- | --- |
| ip  | The ip that you are requesting |   Required |
| mask | The IP mask. Defaults to 32 bit mask | Not Required (Default Set) |

**Example**

```
s = SecurityTrails(api_key='yourapikey')
s.ip_explorer("netflix.com")
```

***

#### test_connect
**Function**
Test ping to Security Trails API

**No parameters**:
Relies on API key being set in class instantiation.  Returns True for successful connection and False for unsuccessful.

**Usage**

**Example**
```
s = SecurityTrails(api_key='yourapikey')
s.test_connect()
```
