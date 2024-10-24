# eID Hands-on workshop

> A set of Jupyter notebooks for the E-ID hands-on workshop  
> happening on **the 29th of October**.

> Note that the notebooks will use **Typescript** for all excercises.

This project showcases usage of E-ID through some different technologies. 
It goes through clarifying examples of some of the most important concepts in E-ID today including 

- Selective Disclosure
- Zero-Knowledge Proofs
- Unlinkability

The excercises focse on one of the most prominent cryptographic schemes in the E-ID space today **BBS+**.  
Learn more about BBS+ signature scheme [here](https://identity.foundation/bbs-signature/draft-irtf-cfrg-bbs-signatures.html).

# Installation
This project depends on [Python](https://www.python.org/), and [Node.js](https://nodejs.org/en).

To install the library dependencies, we use the following:
```shell
// Install python dependencies
>>> pip install -r requirements.txt

// Install the npm dependencies
>>> npm install

// Install Typescript Kernel for jupyter notebook
>>> tslab install
```

Now, to run the jupyter notebooks, we simply run:

```bash
>>> jupyter lab
```



### Alternatively, using Devbox
We support installation using [Devbox](https://www.jetify.com/devbox/docs/quickstart/) which facilitates environment management.  
Just run the following command to install all dependencies:

```bash
$ devbox run jupyter
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
