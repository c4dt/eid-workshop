This is an overview of all exercises and questions.

# Exo 1
## 1.1
Make sure that the signature fails in the following cases:
- the message is different from the message used in the signing process
- the public key is different than the public key from the issuer
## 1.2
Print the hashes of hashValue(value) and from the RETRIEVED_DATA(key) and compare them visually
Change the disclosed fields and make sure it still rus
## 1.3. Discussion: security of this scheme, and introduction to unlinkability
Security of hashed values
Unlinkability
## 1.4. Coding exercise: protect the hashes
Create a way to hack the `timeOfBirth`. How can this be made faster?
How would you hack the `name`, or `profession`?
Reimplement the communication between the holder and verifier modifying the hash function in a way that doesn't make it easy to guess the fields

# Exo 2
## 2.1
What is the format for timeOfBirth? And what is the limitations using that format? What else could the format be?
What other fields could be in the credential?
## 2.2
What information do you find in the credential which is sent to the holder? What keywords / algorithms do you recognize?
How many bytes is the proof sent to the holder?
## 2.3
Explore the bbsProofVerifier to see what information is sent to the verifier
Is there information which could be used to de-anonymize the holder?
How long is the proof now? Why is it bigger than the proof sent by the issuer?
## 2.4
Can you create a proof which cannot be validated? What did you change?
Reveal another element of the credential - what did you need to change?
How does the verifier know the credentials to reveal?
## 2.5. Discussion - Unlinkability achieved?
Is there a signature or a cryptopgraphic data that is shared and could used to identify the credential holder?
Is there a part of data hashed or not that was included in the presented data that could be used to identify the credential holder?
## 2.6. Coding exercise - Simulate an issuer-holder-verifier setup
What are the conditions that revealing a field doesn't lead to linkability?
How can the verifier be sure that the proof is not stale, meaning that it is not a replayed proof?
Can you easily implement this? Unfortunately the docknetwork/crypto-library doesn't have a good API documentation. 
Look at the PresentationBuilder. Which field looks like the best to use for the purpose of avoiding replays?

# Exo 3
## 3.1
Change the content of the credential
Why is the timeOfBirth not a string like "21st of March 1998"?
Add a new field to the credential, but don't forget to also add it to the schema
## 3.2
What happens if you try to create a proof which is not satisfied by the credential? Why?
How does the verifier know the bounds check performed? Does it need this information? Why (not)?
Change the proof to be on a different field of the credential
Add a second range proof
## 3.3
If you do the same exercises as for the LegoGroth16, what is the difference in the code?
What other difference do you experience when running the code?
Can you find how the verifier can be sure what is proven by the holder?
## 3.4. Discussion: are we anonymous and unlinkable now?
What did we gain by using Zero Knowledge Proofs?
What does the verifier learn about our credential?
Does this make the proof anonymous? Why? Why not?
Is the proof unlinkable? When is it? When isn't it?
## 3.5. Coding exercise - Using the ZKPs
Create a proof that your age is in a certain range. Why is the age format given like this?
Add a new field for the postal code to the credential and to the schema. Now create a proof that you live in the canton de Vaud.
## 3.6. Hard Coding Exercise - Revocation test: add an accumlator using a negative membership check
