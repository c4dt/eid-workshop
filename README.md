# E-ID Hands-on workshop

These jupyter-notebooks are for the hands-on workshop organized by the C4DT on the
29th of October 2024.
This project showcases usage of E-ID through different technologies. 
It goes through clarifying examples of some of the most important concepts in E-ID today including:

- Selective Disclosure
- Unlinkability
- Predicate Proofs using Zero-Knowledge Proofs

The excercises focus on one of the most prominent cryptographic schemes in the E-ID space today **BBS+**.  
Learn more about BBS+ signature scheme [here](https://identity.foundation/bbs-signature/draft-irtf-cfrg-bbs-signatures.html).

You can find the slides here:

- [Overview of eID landscape](./E-ID_slides_morning.pdf)
- [Hands-on workshop on E-ID cryptography](./E-ID_slides_v1.1.pdf)

# Installation

This project depends on [Python](https://www.python.org/), and [Node.js](https://nodejs.org/en).
It has been tested with Python 3.11 and node 18 and 22.
There are instructions to install it globally on your computer, or use 
[Devbox](https://www.jetify.com/devbox/docs/quickstart/)
for a simpler installation.

## Globally

Make sure that you have node and python installed in the correct versions:

```bash
python --version
# Python 3.11.10
node --version
# v22.8.0
```

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

## Alternatively, use Devbox

We support installation using [Devbox](https://www.jetify.com/devbox/docs/quickstart/) which facilitates environment management.  
Once devbox is install, you can run the following command to launch jupyter-lab:

```bash
devbox run jupyter
```

This will take care of the correct python and nodejs version, install the packages, and run
the jupyter-lab.
You might need to add `--pure` to the command: `devbox run jupyter --pure`, to make sure no
other binaries from your computer interfere.

If the page doesn't open automatically on your computer, look at the output of the `devbox run jupyter` command:

```
    
    To access the server, open this file in a browser:
        file:///Users/something/Library/Jupyter/runtime/jpserver-12345-open.html
    Or copy and paste one of these URLs:
        http://localhost:8889/lab?token=thisisnothex480de91eb865b15f43f6fe973b95eb7a64dc
        http://127.0.0.1:8889/lab?token=thisisnothex480de91eb865b15f43f6fe973b95eb7a64dc
```

Of course your token will be different, so don't use these URLs!

# Exercises

The following exercises are available:

- Exercise 1 - Simple Signing
  - Section 1 - Basic E-ID example using RSA cryptographic scheme
  - Section 2 - Selective Disclosure using hashing
  - Discussion - Security of this scheme, and introduction to unlinkability
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
  - Discussion - Are we anonymous and unlinkable now?
  - Coding exercise - Using the ZKPs
  - Hard Coding Exercise - Revocation test: add an accumlator using a negative membership check
- Exercise 4 - ZKP Measurements
  - Exercise 4a - ZKP Measurements calculations
  - Exercise 4b - Plotting of results

# Solutions

There are now solutions to the challenges and questions in the exercises.
You can find them in the `exercise-x-solution` files.

# Feedback

Happy to receive feedback at c4dt-dev@epfl.ch.

# LICENSE

This is licensed under CC BY-SA 4.0 and MIT license.
