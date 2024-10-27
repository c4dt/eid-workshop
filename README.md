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

### Alternatively, use Devbox
We support installation using [Devbox](https://www.jetify.com/devbox/docs/quickstart/) which facilitates environment management.  
Once devbox is install, you can run the following command to launch jupyter-lab:

```bash
devbox run jupyter
```

# Exercises

The following exercises are available:

- Exercise 1 - simple signing
  - Section 1 - Basic E-ID example using RSA cryptographic scheme
  - Section 2 - Selective Disclosure using hashing
  - Discussion - security of this scheme, and introduction to unlinkability
  - Coding exercise - protect the hashes
- Exercise 2 - Unlinkability with BBS+
  - Section 1 - Credential - Setting up a corresponding JSON Schema
  - Section 2 - Issuer - Setting up and creating a BBS+ signature
  - Section 3 - Holder - Creating a proof
  - Section 4 - Verifier - Verifying the proof is valid
  - Discussion - Unlinkability achieved?
  - Coding exercise - Simulate an issuer-holder-verifier setup
- Exercise 3 - Zero Knowledge Proof
  - Section 1 - Issuer - Setting up and signing a credential
  - Section 2 - Creating a range proof using LegoGroth16
  - Section 3 - Creating a range proof using Bulletproofs++
  - Discussion - are we anonymous and unlinkable now?
  - Coding exercise - Using the ZKPs
  - Hard Coding Exercise - Revocation test: add an accumlator using a negative membership check
- Exercise 4 - ZKP Measurements
  - Exercise 4a - ZKP Measurements calculations
  - Exercise 4b - plotting of results
