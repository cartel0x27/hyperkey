Hyperkey is a tool for generating a password given:

  1. Any file. The SHA256 hash of this file will be used as the base seed and salt for the password generator. This can be a local file or an http(s) url.
  1. A policy identifier (Green - default pwgen. Yellow - FIPS112. Red - 24 characters.) Other policies can be defined by editing the code.
  1. A service id (arbitrary: could be a username or service; username@gmail for example).
  1. A passphrase.

Given the same four inputs hyperkey will always return the same password.

Usage example:

```
$ ./hyperkey.py http://tinyurl.com/redacted yellow gmail 
[!] this is hyperkey, a thoughtcrime project
[!] retreiving seedfile via http
[?] passphrase: 
[+] hashing: done.
[+] iterating: done.
[!] generated password: s7c/Ipg7hmRm
[+] copied to clipboard
[!] we're done here
```

Runs on Linux, Windows, OS X and Android (via sl4a). Android support currently needs the url to the seed file hard coded.