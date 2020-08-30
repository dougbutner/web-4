# WIP v 0.0.1
# The Web 4 Manifesto - Awakening the Democratic Web 

Collaborative Democracy [Alt title]

[![Mentioned in Awesome Web 4](https://awesome.re/mentioned-badge.svg)](https://github.com/dougbutner/awesome-web4)

## About This Repo 

This README features a description of the next evolution of the web, **web 4**. As the technologies emerge, this repo will also feature code and links to the associated technologies. For more cool Web 4 stuff, visit the [**Awesome Web 4**](https://github.com/dougbutner/awesome-web4) **repo**.

## What is Web 4?

Before we define web 4, we must look briefly at the concepts of web 1, web 2, and web 3. 

 - **Web 1**
**Static web**. Files are served from a remote server to a user's browser.

 - **Web 2**
**Dynamic web**. Web pages that take user's information and desires into account. Asynchronous requests allow single page applications to thrive. Applications are still served from a central server.

 - **Web 3**
**Decentralized web**. Open-source applications exist in distributed networks instead of a central server. This unfederated model trades control and censorship ability for freedom and lack of opinion. 

 - **Web 4**
**Democratic web**. Enabling meaningful layers on top of current socioeconomic systems built on time-minted crypto versatile which gains utility in how it is spent. Open source, unfederated biocryptography allows democratic systems to flourish, and takes government identification and corporate oversight out of the picture. Intentional degradation of information changes blockchain paradigms and brings meaning to time-based information models. 

Today, the top 100 websites by traffic are [all](https://www.alexa.com/topsites) web 2 websites. The web 2 paradigm fits closely with the wider environment of **corporate-owned information.** 

As more and more individuals and societies are reconsidering the place of **government, censorship, centralization and federated power**, web 3 has emerged as a powerful, provable option to **shape the evolution of society** on planet Earth. 

A growing portion of web 2 websites and applications today have elements of web 3, like [cryptoblogs](https://peakd.com) and [games](https://www.stateofthedapps.com/rankings/category/games). While web 2 and web 3 can operate independently, web 3 enhances the abilities of web 2. 

As web 3 matures, we start to open a **pandoras box of practical applications**. With transaction fees near non-existent on second layers, we can re-imagine what is possible. 

Web 4's dreams up **proof of individuality** through encrypted biodata that kickstarts a collaborative society, one driven by enabling each individual with **free daily tokens** that can be burnt to complete an action, e.g. voting on a community proposal. 


Web 4 lays the foundation for this to be built. But, like any democratic system. **We need your help.** Please read this paper, and consider these ideas. If you believe you can make them better, please **submit a pull request** with your ideas. If you are a developer, I want to remind you of the license of this repo, and **invite you to forge any of these ideas into hot-pressed applications**. 

## Guiding Philosophy
Web 4 seeks to implement systems in **harmony with the universe itself** by replicating nature: the **abundance** of the Sun, rising **entropy** in closed systems, and even the **equality** of each conscious being. 

We believe when we create information systems in **harmonic resonance** with natural systems, our society will be able to advance more rapidly than ever before, as we will be able to **"fit in" with the larger systems of information processing** around us (the Earth, Sun, and Galactic core). 

## Defining Web 4
Web 4 introduces **provably democratic systems** built on top of web 3's open-source decentralized networks. 

There are 4 conceptual underpinnings of web 4

 1. **Time-issued cryptocurrency** 
 2. **Proof of Individuality**
 3. **Information Entropy**
 4. **Harmonic GeoSocial Systems**

We will discuss these concepts one at a time, then look at possible applications of these web 4 concepts, and a roadmap to reality.

# #1: Time-issued cryptocurrency (Time Tokens) 

Time tokens are distributed to users' wallets periodically as time passes. These tokens provide the user with an action. The action burns the token, which may cause some change in the state of a system, or minting of another token, or any other action. 

## The Gears of Time Tokens

Time tokens rely on the following concepts:

 1. **Time Unit**
A time unit MUST be a superset of a timestamp. This means that a time unit is some amount (or fraction) of a second. Each time token MUST be the only one in existence stamped with a particular time unit for each user (wallet). 
 2. **Time Token Faucet**
A time faucet provides any verified user EXACTLY one time token per unit of time passed since their last faucet. This can be an active faucet; requiring some action by the recipient, or a passive faucet; automatically sending the cryptocurrency to the user.
 3. **Verified Recipients**
Recipients of the system MUST be verified to be an actual human in order to receive time tokens. Biocryptographic secrets are suggested as the solution to this problem, and examined further down.  


For a full description of Time Tokens, visit the  [Time Token repository](https://github.com/dougbutner/time-token). 


## How do Time Tokens work?
Time tokens store a time unit (integer) with a unique user identifier (string) in a hash signed by the user's biocryptographic signature.

Time tokens are platform independent, and need only store simple data involving time unit and an account identifier at the most bare level.

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
	"appData": {
		"location": 
	}
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
	// These points expanded to a pre-defined margin of error geometrically for each input type
	// Finally, ranges of values are hashed, that value is returned  
}

```
The notable parts here are the `time-unit` and `userid` in the payload, and the `signingSecret` which is generated by a user's biometric data.

You can see that this example used only web 2 technology, as JWT doesn't imply decentralized use. If the user's ID is mapped to an address on a blockchain, then web 3 is required. Which begs the question:


## Why can't web 3 (or even web 2) do this?

Web 2 is not a viable candidate for this because the federated nature means that your biometric data must be trusted to a third party, possibly a large corporation or malicious actor. 

Provable democracy cannot be fully achieved in web 3, because there is no control over how many accounts a user may own. [2] Many different consensus models have been developed, most notably, proof of work, proof of stake (POS), and delegated proof of stake (DPOS). These paradigms of consensus are used primarily to determine which chain of transaction records (blocks) is considered valid, securing a blockchain. 

POS and DPOS is additionally used to in projects like Hive to allow users to "vote" on valuable content, an early example of the democratic web. DPOS is also used for networks to determine who can access network resources.

However, both of these POS/DPOS use cases (curation and resource allocation) are not democratic in the sense that **each account is not equal**. In both cases, the root of democracy is in the token, not the individual, and the ownership of tokens determines the voting power or processing power held by an individual. 

In the end, the only way to implement true democracy in any system is through giving each individual equal power. The only way to do this while keeping web3's decentralized nature is to implement the technological (biocryptology) and idealogical (time faucets, degradation of data) advancements needed to be sure an account is owned by **one individual**, and that individual has **only one account**. These advancements are, for simplicity and communication, called web 4. 

___
<center>~~</center>

___

## **2.  Proof of Individuality - Biometric Secrets + Protecting Identity**
Biometric secrets are akin to any cryptographic secret key, they are a hash of information. The information hashed in a biometric secret comes from a person's biometric expression. In today's biometric space, simple static images are most commonly used for things like fingerprint and facial recognition, and geometry is the means to compare this data. 

Biometric secrets generated from static images are not secure, as static images can be easily faked in innumerable ways [GETCIT]. Video offers a better solution to this problem, as it is harder to fake, can include audio, and lets developers create a whole new set of algorithms based on a changing stream of data. 

### What is used to generate a biosecret?
This stream of data (video + audio biometric expression) could be a user doing a series of hand gestures, singing a part of a song, speaking a phrase, speaking a phrase in different voices, clapping, making a series of facial expressions, or anything else one can imagine.

For security, biometric expressions must be unique and many types (gesture, singing, clapping) must be available and used in combination. If each person's biometric secret was generated from the same single biometric expression, it would be a matter of time before specific AI could be developed to deepfake it for anyone. If the user is the only one that knows their biometric expressions it becomes nearly impossible to guess the type and nature of the expression, and even if that is known, impossible to use the same technique on more than one account. 

The nature of the uniqueness could be chosen by the user, or generated at random from the biosecret software which would prompt the user to complete an action in a specific way. The user-chosen methos would be up to the user to remember, possibly by storing a hint, and the prompted way would require local storage of the prompt. 

## Why do we need this, again?
Democratic systems certainly could be built without biometric verification, and must be at least until suitable biometric technology develops along the open source, client-side requirements. For now, decentralized solutions like [Civic](https://www.civic.com/) provide the necessary individuality at the cost of trust and requirement of citizenship. As different project inplement  implement web 4 in their own ways. 

We will present the ideas that are crucial for this system to be different, and represent true growth into web 4.


**Key Aspects** 
1. **Biometric Expression**: A user is presented with a choice of different biometric options used to generate a hash that can only belong to this person. 
User can choose to either perform a chosen biometric task to receive their hashed biosecret (trustless) or generate it at any time from a third party provide (trust). Any third party provider will generate the same hash by a set or open-source algorithms. 

2. **Biosecret Generation**: User's sensitive biological information and generated algorithmic results are destroyed (made impossible to reconstruct) at the layer of hashing, and data not stored in any way, public or private, as the user runs the software on their local machine (assuming they choose the open-source software, not a third party).

3. **Time Psudeoanonyminity**: Any outward-facing display of information about a users usage of time tokens should be pseudo-anonymous. That means that a user's identity and time unit (what token is spent) is masked and presented as an alias for each token type. Each use involves a secret key that is known only to the verifying entity, a paet 


The biggest issue with biometrics is the lack of trust, mostly due to the growing number of facial recognition softwares and databases. The lack of trust is almost always associated with an individual's lack of consent, not the technology itself. 

To alleviate the trust issue, solutions must be: 1) open-source, 2) run entirely on the individual's hardware (client-side), and 3) not expose any biometric data to any other users or systems. 

By using identifying information following open-source algorithms, in a way that is provable, and 

communicable 

There will always be security concerns with biometrics. For example, if a user uses their biometric secret to unlock their mobile device, another app could be secretly recording the camera in the background. A person could record them doing their secret, and try to play that video back to the camera to gain access. Or more realistically, deep fakes AI.[] All of these concerns and more must be dealt with before this technology reaches massive adoption. 

The upside of biometric secrets is they cannot be lost, and the account will always be recoverable by the individual. In a web 4 ecosystem, where the tokens are distributed daily and often spent daily, a hack would be much less catastrophic. The attacker will be able to access the user's balance, but not alter the past transactions, nor continue to collect the future deposits, because the real user will (in theory) quickly recover the account and change the biometric secret generation means so that the hacker's biofake is no longer working. 

___
<center>~~</center>

___

## Degradation of Information
Web 3 focuses on storing information forever in a provable way. Web 4 introduces a counter-model which may be **optionally** adopted by any time-token-based system. In this model, who did what becomes **harder and harder to know** the more time that passes. 

This idea hinges upon incremental time units, the number of which is used to decide how difficult information about a particular individual is to access. 

With pseudoanonymity, it is difficult, but not impossible, to piece together a story about an individual user by knowing they are responsible for a set of transactions over time. The further back in time a transaction is, the harder it is to link it to another transaction with any certainty. 

Though the user's actual identity can never be known (unless the user exposes their key outside of the blockchain)




## **Degradation of Information Fidelity**
Information fidelity requirements can also be degraded over time. For example, when generating a users biosecret, it can be assumed that the more time that passes, the more the bioinformation of the individual will change. 

Biosecrets are generated from a **range of biometric values**. This range of values can be expanded over time. The effect is, instead of having one hashed biosecret for eternity, the generation process will create a set of biosecrets from an increasingly wide range of data. This concept may be needed to keep people in control of their accounts as they age. There is considerable work to be done to develop this concept, as each 





While the inclusion of this concept into web 4 may seem unnecessary (and totally is), it is another guarantee of the psudeoanonymity that is needed for many social applications. It can be used for performance benefits as well. Philosophically, degradation of information also fits in with the general web 4 desire to reflect systems in nature.

When querying data becomes intensive, and a client couldn't hold all the information


Incentives are give for the ratity of the 

Performance Benefits
In the event that 


# 4. GeoSocial Layers

Each version of the web must evolve. I believe the greatest evolution happens when we can harness the concepts of collaborative social environment more th 


# The experience of Web 4


Notable differences in M


# Roadmap to Web 4 Reality

**Phase One**
> Implementing time tokens

**Time tokens** are implemented on any and all blockchains where developers see the value. These developers provide open-source instructions and tools to helps others make their own time tokens. 

**Provable individuality** for Time Tokens is up to each application and blockchain, and these application can choose to ignore this requirement, risking their system' integrity. Federated  (Google / SSO) and decentralized options (Civic) may be used. 

**Information entropy** and geosocial layers are starting to be theorized. 

Action Points: 
- ERC proposal (and similar for other blockchains)
- Federated + 

**Phase Two**

**Phase Three**
biocryptography
developing biocryptography standards

**Phase Four**
**Information entropy** is added to the systems where it can be of use. 



# Author notes

## Change Without Conflict
No one can stop us from building collaborative systems with web 4 and even self-governing. We don't need to "tear down the system" or separate from society to do so. We can still exist fully embedded in the geopolitical systems around us, while building up web 4 layers, the underpinnings of collaborative democracy.

If and when the "old system" meets demise, as all things do, we can transition rapidly to a web 4 system like [Effective Collective](https://github.com/dougbutner/effective-collective) or another, as it will already be in place. 

## Why use the term "Web 4"
It is my belief that each version of the web must 1) be built on top of the previous version, 2) be fundamentally different than the previous version by introducing new technology, and 3) have meaningful impact on society. 

This proposal for the next iteration of the web is an effort to both expand and shift the path of information science in a direction where the meaningful impact of society involves: 1) empowerment of each individual, which serve as the basis for collective (social), economic, and novel applications; 2) provable identity verification while maintaining complete separation from any federated system, including government, with the side-benefit of lifelong recoverability of private keys, and 3) resonance with our containing systems, like the Solar system, which provides us with free energy daily, akin to free time tokens.

While an argument could easily be made that DeFi is Web 4, or another emerging tech, like layers on top of blockchains (sidechains) are web 4, both of these are not new. DeFi mimics the systems of the past in a better way. Sidechains are merely making web 3 more efficient. 

It is my hope that the information presented here will be expanded on and implemented by many developers and systems in the coming years, not for the benefit of the few, but for the empowerment of each individual and the harmony of the human collective, and every layer of Gaia. 

**Notes + References**
___

[1] - Solutions like Civic have proved to be effective in verifying individuality. KYC services rely on government-issued identification, physical signature, and minimal, often human-checked bioverification Until the technology is developed for a biometric system resembling the ideas here, this option is viable, though not fully embodying the idea of web 4. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbODQzMjkwNjYzLDE1MzAwNzM5MjcsMTU4Mz
U3MjI2NCwyNTEzNDAzMjQsMTUxODkwMjYxNSwtMTk3ODc0Nzc3
NSwzMTc3MzkyOTYsLTE5Mzg0NTA5MjAsLTE3MjIyNDU1ODksLT
c3MDAwNDYyNSwtMTgzMDQ4MTYzMiwtMTU4NDU1NTc0NiwxNjkx
MDYxNTMwLC0xMjI2OTYwMzAwLDM3NDE0NDAwNSwtMTg1OTkyNj
U4NSwxMjE2MTI2MTExLDU5Nzg3NTI1Niw3MzE4NDc5OTIsMTE1
MDQyNzk5XX0=
-->