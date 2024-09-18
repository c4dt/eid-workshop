# eID Hands-on workshop

This is the first set of Jupyter notebooks for the eID hands-on workshop
on the 29th of October.

## Installation

Please use [Devbox](https://www.jetify.com/devbox/docs/quickstart/) to run
jupyter-lab:

```bash
devbox run jupyter
```

# Exercises

The following exercises are (will be) available:

- Selective disclosure and unlinkability
  - RSA/ECDSA: NO SD, NO unlink
  - RSA/ECDSA with hashing fields: YES SD, NO unlink
  - BBS+: YES SD, YES unlink
- BBS+
  - Selective disclosure examples
  - Unlinkability proof
  - check [Cryptographer's feedback](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/issues/200) for more ideas / examples
- ZKP
  - Simple proof-range
  - Combined proof-range with SD
  - Set membership (diploma example from Imad)
