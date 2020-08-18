# Web 4.0 - The Democratic Web Time

[![Mentioned in Awesome Web 4](https://awesome.re/mentioned-badge.svg)](https://github.com/<INSERT LIST URL>)

## About This Repo 

This README features a description of the next evolution of the web, web 4.0. As the technologies emerge, this repo will also feature code and links to the associated technologies.

## What is Web 4.0?

Before we define web 4.0, we must look briefly at the concepts of web 1.0, web 2.0, and web 3.0. We will remove the ".0" for the rest of this document, because that's sooo web 2.

 - **Web 1**
Static files served from a remote server to a user's browser.

 - **Web 2**
Dynamic pages that take user's information and desires into account. Asynchronous requests allow single page applications to thrive. Applications are still served from a central (federated) server.

 - **Web 3**
Decentralized web. Open-source applications exist in distributed networks instead of a central server. This unfederated model trades control and censorship ability for freedom and lack of opinion. 

 - **Web 4**
Time web. Enabling meaningful layers on top of current socioeconomic systems built on time-minted crypto versatile which gains utility in how it is spent. Open source, unfederated biocryptography allows democratic systems to flourish, and takes government identification and corporate oversight out of the picture. Intentional degradation of information changes blockchain paradigms and empowers time-based information models. 

Today, the top 100 websites by traffic are [all](https://www.alexa.com/topsites) web 2 websites. The web 2 paradigm fits closely with the wider environment of corporate-owned information federation. 

As more and more individuals and societies are reconsidering the place of government, censorship,   and federated vs unfederated power, web 3 is emerging as a powerful, provable option to shape the evolution of society on planet Earth. 

A growing portion of web 2 websites and applications today have elements of web 3, like [cryptoblogs](https://peakd.com) and [games], web 2. While web 2 and web 3 can operate independently

Currently, Q3 2020, we are entering the start of maturity of web3. The technology is literally evolving, as we await players like eth2 into a growing space. 

## Defining Web 4
Web 4 introduces provably democratic systems built on top of web 3's open-source decentralized networks. 

There are 4 conceptual underpinnings of web 4

 1. **Time-issued cryptocurrency** 
 2. **Biocryptographic + independent verification signatures**
 3. **Information Degradation**
 4. **Socioeconomic Layers**

We will discuss these concepts one at a time.

# Time-issued cryptocurrency (Time Tokens) 

Time tokens are distributed to users based on the amount of time passed.  

Time tokens allow web 2 and web 3 applications to offer a provably democratic model to their users. 

## The concept behind Time Tokens

Time tokens rely on the following concepts

 1. **Time Unit**
A time unit MUST be a superset of a timestamp. This means that a time unit is some amount (or fraction) of a second
 2. **Time Faucet**
A time faucet provides any verified user with EXACTLY one time token per unit of time passed since their last faucet. This can be an active faucet; requiring some action by the recipient, or a passive faucet; automatically sending the cryptocurrency to the user.
 3. **Verified Recipients**
Recipients of the system must be verified to be an actual human in order to receive time tokens. The issue of verification is very serious if we are to continue from web 3 instead of taking a step backward toward federated systems (like government-issued IDs). Biocryptography is introduced as the solution to this problem.  


For a full description of Time Tokens, visit the  [Time Token repository](https://github.com/dougbutner/time-token). 


## How do Time Tokens work?
Time tokens store a time unit (integer) with a unique user identifier (string) in a hash signed by the user's biocryptographic signature.

Time tokens are platform independent, and can be implemented on any blockchain that allows storage of small data.

Here is the minimum information stored in a time token, using [JWT](https://jwt.io/introduction/) as an example
```
{
  "header": {
    "typ": "JWT",
    "alg": "HS256"
  },
  "payoadData": {
    "time-unit": 294957,
    "userid": "7f3e873a2c3d"
  }
}
```
For the time token to be spendable, a signed JWT Time Token

```
const passedBioData = {..} // See function bioKeyGenerator at bottom of code

const header = {
        "typ": "JWT",
        "alg": "HS256"
      }

const payloadData = {
	"time-unit": "294957", 
	"userid": "7f3e873a2c3d", 
	"appData": "Lots of things"
}

const bioSecret = bioKeyGenerator(passedBioData); // Biometric provider's key or one generated direcly by user


signature = HMACSHA256(
	base64UrlEncode(header) + "."+
	base64UrlEncode(payloadData), 
	bioSecret
)


function bioKeyGenerator(bioData){
	// Function takes data in the form of user input into their browser or smartphone.
	// With data, quantifyable points are taken algorithmically
	// These points expanded to a pre-defined margin of error
	// Finally, all values are hashed, that value is returned  
}

```
The notable parts here are the `time-unit` and `userid` in the payload, and the `signingSecret` which is generated by a user's biometric data.

You can see that this example used only web 2 technology, as JWT doesn't imply decentralized use. If the user's ID is mapped to an address on a blockchain, then web 3 is required. Which begs the question:


## Why can't web 3 (or even web 2) do this?

Web 2 is not a viable candidate for this because the federated nature means that your biometric data must be trusted to a third party, possibly a large corporation or malicious actor. 

Provable democracy cannot be fully achieved in web 3, because there is no control over how many accounts a user may open. [2] Many different consensus models have been developed, most notably, proof of work, proof of stake, and delegated proof of stake. 

These paradigms of consensus are used primarily to determine which chain of transaction blocks is considered valid, securing a blockchain. POS and DPOS is additionally used to in projects like Hive to allow users to "vote" on valuable content, an early example of the democratic web. DPOS is also used for networks to determine who can access network resources.

However, both of these applications are not democratic in the sense that each account is not equal. In both cases, the root of democracy is in the token, not the individual, and the ownership of tokens determines the voting power or processing power of an individual. 


## **2. Verified Recipients**
It could be said that this system could be built without biometric verification. It certainly could. Until suitable biometric technology develops along the open source, user-ran requirements, [solutions](https://www.civic.com/) provide the necessary individuality, at the cost of trust. This and other solutions will happen as different people implement web 4 in their own ways. 

We will present the ideas that are crucial for this system to be different, and represent true growth into web 4.


**Key Aspects** 
1. **Biometric Identification**: A user is presented with an option of different biometric options used to generate a hash that can only belong to this person. 
User can choose to either perform a chosen biometric task to receive their hashed biosecret (trustless) or generate it at any time from a third party provide (trust). Any third party provider will generate the same hash by a set or open-source algorithms. 

2. **Trustless Trustfulness**: User's sensitive biological information and generated algorithmic results are destroyed (made impossible to reconstruct) at the layer of hashing, and data not stored in any way, public or private, as the user runs the software on their local machine (assuming they choose the open-source software, not a third party).

3. **Time-psudeoanonymous**: 




The biggest issue with biometrics is the lack of trust. The lack of trust is almost always associated with an individuals's lack of consent, not the technology itself. 

By using identifying information following open-source algorithms, in a way that is provable, and 

communicable 

## **Degradation of Information**
Web 3 focuses on storing information forever in a provable way. Web 4 introduces a counter-model which may be optionally adopted by any time token based system. In this model, information becomes harder and harder to know the more time that passes. The agent of this difficulty may be CPU cycles, or a democratic mechanism requiring a number of people requesting information in a given timespan where the more people that seek out a particular block of information, the more likely it is to be accessible to all requesters. 

While the inclusion of this concept into web 4 may seem unnecessary, it is a part of the psudeoanonymity that is needed for many social applications. Consider the 


### Erasing Permanent Records
When web 4 is used for social applications

Systems that store high-fidelity information become increasingly difficult to know something after it happens. As a result og the 



# The experience of Web 4


Notable differences in M


# Roadmap to Web 4

Implementing time tokens

Incorporating federated systems

developing biocryptography standards


# Author notes
It is my belief that each version of the web must be 1) fundamentally different than the previous, 2) be built on top of the previous version, and 3) have meaningful impact on society. 

This proposal for the next iteration of the web is an effort to both expand and shift the path of information science in a direction where the meaningful impact of society involves: 1) empowerment of each individual, which serve as the basis for collective (social), economic, and novel applications; 2) provable identity verification while maintaining complete separation from any federated system, including government, with the side-benefit of lifelong recoverability of private keys, and 3) resonance with our containing systems, like the Solar system, which provides us with free energy daily, akin to free time tokens.

While an argument could easily be made that DeFi is Web 4, or another emerging tech, like layers on top of blockchains (sidechains) are web 4, both of these are not new. DeFi mimics the systems of the past in a better way. Sidechains are merely making web 3 more efficient. 

It is my hope that the information presented here will be expanded on and implemented by many developers and systems in the coming years, not for the benefit of the few, but for the empowerment of each individual and the harmony of the human collective. 

**Notes + References**
___

[1] - Solutions like Civic have proved to be effective in verifying individuality. KYC services rely on government-issued identification, physical signature, and minimal, often human-checked bioverification Until the technology is developed for a biometric system resembling the ideas here, this option is viable, though not fully embodying the idea of web 4. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQ3MzA3NzY1NiwzNjk4NTUzMjksLTQ0MT
g4NDQsLTEyMDc1MjQ2NzUsMTc3MjQ1NTE0MywxOTIzNzc1NzA0
LDE5Nzg4NDc0MjcsMTM3Mzc2NzYyNSwtODgwNTM4MDA3LC0yMD
cwMTQyNzA0LC00MjQ0MDcwMzcsLTMxMTIwMTkyNiw4MDQyMTkw
MTcsODQ4MjUyMDIzLDEyMjc2NjgxNjMsLTcyMzg5OTM1MCwtMT
kyNzMzNDA2MiwtODM2NzI3MjA1LC01MzY2NTMxODMsLTc2MDgx
NTEyXX0=
-->