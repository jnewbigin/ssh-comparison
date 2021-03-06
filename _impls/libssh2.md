---
title: libssh2
homepage: http://www.libssh2.org/
source-repository: https://github.com/libssh2/libssh2/
license: "[BSD style](http://www.libssh2.org/license.html)"
first-release:
    date: 2004-12-08    # version 0.1, initial release, date from repository
latest-release:
    version: 1.7.0
    date: 2016-02-23
changelog: http://www.libssh2.org/changes.html
client: yes
server: no
library: client

protocols:
    cipher:
        - aes128-ctr    # not documented; enabled if using OpenSSL >= 0.9.7, or libgcrypt, but not with Windows CNG
        - aes192-ctr    # not documented; enabled if using OpenSSL >= 0.9.7, or libgcrypt, but not with Windows CNG
        - aes256-ctr    # not documented; enabled if using OpenSSL >= 0.9.7, or libgcrypt, but not with Windows CNG
        - aes256-cbc
        - rijndael-cbc@lysator.liu.se
        - aes192-cbc
        - aes128-cbc
        - blowfish-cbc
        - arcfour128
        - arcfour
        - cast128-cbc
        - 3des-cbc
    compression:
        - zlib
        - zlib@openssh.com  # added in 1.4.3
        - none
    hostkey:
        - ssh-rsa
        - ssh-dss
    kex:
        - diffie-hellman-group14-sha1
        - diffie-hellman-group-exchange-sha1
        - diffie-hellman-group1-sha1
        - diffie-hellman-group-exchange-sha256
    mac:
        - hmac-sha2-256
        - hmac-sha2-512
        - hmac-sha1
        - hmac-sha1-96
        - hmac-md5
        - hmac-md5-96
        - hmac-ripemd160
        - hmac-ripemd160@openssh.com
    userauth:
        - password
        - publickey
        - hostbased
        - keyboard-interactive
---
* C library for clients.
* Not to be confused with the unrelated [libssh](/impls/libssh.html)
