

# openssl: Toolkit for Encryption, Signatures and Certificates Based on OpenSSL

[![](http://www.r-pkg.org/badges/version/openssl)](http://cran.rstudio.com/web/packages/openssl/index.html)

* CRAN: http://cran.r-project.org/web/packages/openssl/index.html
* GitHub: https://github.com/jeroenooms/openssl


```r
> library(openssl)
```

```

Attaching package: 'openssl'
```

```
The following object is masked from 'package:digest':

    sha1
```

バージョン: 0.9.1

-----



| 関数名 | 概略 |
|--------|------|
| `aes_cbc` | Symmetric AES encryption |
| `askpass` | Password Prompt Utility |
| `base64_encode` | Encode and decode base64 |
| `bignum` | Big number arithmetic  |
| `cert_verify` |X509 certificates |
| `encrypt_envelope` | Envelope encryption |
| `hashing` | Vectorized hash/hmac functions |
| `keygen` | Generate Key pair |
| `my_key` | Default keypair |
| `openssl` | Toolkit for Encryption, Signatures and Certificates based on OpenSSL  |
| `rand_bytes` | Generate random bytes and numbers with OpenSSL |
| `read_key` | Parsing keys and certificates |
| `rsa_encrypt` | Low-level RSA encryption |
| `signature_create` | Signatures |
| `write_pem` | Export key or certificate |

-----

## aes_cbc / aes_cbc_encrypt/ aes_cbc_decrypt



## hashing / sha1 / sha256 / sha512 / md4 / md5


```r
> sha1("admin")
```

```
[1] "d033e22ae348aeb5660fc2140aec35850c4da997"
```

```r
> md5(c("foo", "bar"))
```

```
[1] "acbd18db4cc2f85cedef654fccc4a4d8" "37b51d194a7513e45b56f6524f2d51f2"
```

