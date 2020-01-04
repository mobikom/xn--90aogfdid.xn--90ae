# мобиком.бг
https://www.xn--90aogfdid.xn--90ae/

## IDNA encoding or Punycode domains

### Github Pages does not work properly with cyrillic custom domains

IDNA convention: To prevent non-international domain names containing hyphens from being accidentally interpreted as Punycode, international domain name Punycode sequences have a so-called ASCII Compatible Encoding (ACE) prefix, "xn--", prepended.[2] Thus the domain name "bücher.tld" would be represented in ASCII as "xn--bcher-kva.tld".

Using python you could try encode('idna') to find what characters to use, for example:
```
$ python
>>> x = u'bücher.tld'
>>> x.encode('idna')
b'xn--bcher-kva.tld'
>>> x.encode('idna').decode('idna')
'bücher.tld'
```
