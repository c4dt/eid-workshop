# E-ID Hands-on workshop

> A set of Jupyter notebooks for the E-ID hands-on workshop  
> happening on **the 29th of October**.

> All notebooks use **Typescript** except the last one that uses Python for plotting.

This project showcases usage of E-ID through different technologies. 
It goes through clarifying examples of some of the most important concepts in E-ID today including:

- Selective Disclosure
- Zero-Knowledge Proofs
- Unlinkability
- Anonymous Credentials

The excercises focus on one of the most prominent cryptographic schemes in the E-ID space today **BBS+**.  
Learn more about BBS+ signature scheme [here](https://identity.foundation/bbs-signature/draft-irtf-cfrg-bbs-signatures.html).

# Installation
This project depends on [Python](https://www.python.org/), and [Node.js](https://nodejs.org/en).
It has been tested with Python 3.11 and node 18 and 22

To install the library dependencies and start jupyter-lab, execute the following commands.
If you're using `zsh` on Mac, you can ignore the errors from the `# comments`.

```bash
# Create virtual environment and activate it.
# If this returns an error, be sure that `python --version` is 3.11.
python -m venv .venv
. .venv/bin/activate

# Install python dependencies
pip install -r requirements.txt

# Install the npm dependencies
npm install

# Install Typescript Kernel for jupyter notebook
npx tslab install

# Run jupyter-lab
PATH=$PATH:node_modules/.bin jupyter-lab
```



### Alternatively, using Devbox
We support installation using [Devbox](https://www.jetify.com/devbox/docs/quickstart/) which facilitates environment management.  
Just run the following command to install all dependencies:

```bash
$ devbox run jupyter
```

# Exercises

There are 4 exercises in this repository. The last exercise is split in two parts.

1. Signing simply with RSA
2. Unlinkable proofs using BBS+
3. Range proofs with ZKPs
4.
   a) ZKP Measurements
   b)Plots

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
