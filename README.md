# Web 4.0 - The Democratic Web

## About This Repo 

This README features a description of the next evolution of the web, web 4.0. As the technologies emerge, this repo will also feature code and links to the  associated technologies.

## What is Web 4.0?

Before we define web 4.0, we must look briefly at the concepts of web 1.0, web 2.0, and web 3.0. We will remove the ".0" for the rest of this document, because that's sooo web 2.

 - **Web 1**
Static files being served from a server to a user's browser.
 - **Web 2**
Dynamic pages that took user's information and desires into account. Asynchronous requests allow single page applications to thrive. Applications are still served from a central (federated) server.

 - **Web 3**
Decentralized web. Applications exist in distributed networks instead of a central server. This unfederated model trades control and censorship ability for freedom and lack of opinion. 

 - **Web 4**
Democratic web. Enabling meaningful layers on top of current socioeconomic systems built on time-limited crypto income that is given freely to verified recipients. 

Today, the top 100 websites by traffic are [all](https://www.alexa.com/topsites) web 2 websites. The web 2 paradigm fits closely with the wider environment of corporate-owned information federation. 

As more and more individuals and societies are reconsidering the place of government, censorship,   and federated vs unfederated power, web 3 is emerging as a powerful, provable option to shape the evolution of society on planet Earth. 

A growing portion of websites and applications today have elements of web 3 

## Defining Web 4
Web 4 introduces provably democratic systems built on top of web 3's decentralized networks. 

There are 3 conceptual underpinnings of web 4

 1. **Time-issued cryptocurrency** 
 2. **Biocryptographic + independent verification signatures**
 3. **Socioeconomic Layers**

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

    {
      "header": {
        "typ": "JWT",
        "alg": "HS256"
      },
      "body": {
        "time-unit": 294957,
        "userid": ""7f3e873a2c3d
      }
    }



## Why can't web 3 do this?
Provable democracy cannot be fully achieved in web 3.0, because there is no control over how many accounts a user may open.[2] Instead, many different models have been developed to deal with this issue, most notably, proof of work, proof of stake, and delegated proof of stake. 

These paradigms of democracy are used primarily to determine which chain of transaction blocks is considered valid, securing a blockchain. POS and DOPS are also used to in applications like Hive to allow users to declare 


## **3. Verified Recipients**
It could be said that this system could be built without verification. It certainly could. This will no-doubt happen, as different people implement this 



Biometric Identification resonance
Open Source - 
Time-psudeographic
Degradation of information - becomes increasingly difficult to know something after it happens


The biggest issue with biometrics is the lack of trust. The lack of trust is almost always associated from teh person's lack of consent, not the use of the technology itself. By using identifying information




# The experience of Web 4


**Notes + References**
___

[1] - Solutions like Civic have proved to be effective in verifying individuality. KYC services rely on government-issued identification, physical signature, and minimal, often human boirecognition.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwOTg0NTI4MzAsMjA3MjQ5Nzg1LC04Mz
U1MTc2NzgsOTkzNDkxNDEwLC0xODk1ODA0NDM3LDE1OTgzMjA0
MywtMzQ1ODc2OTEzLDE2NzU0MDMyMjIsLTEwODg4NTI2MjEsLT
YxODM2MzE5OCwzNjM0NzY0MjEsLTE1NTEwOTQyNjUsMTk1Mjcy
MzU1OCwxNzA1MDY1ODUsNTA4OTQyMjM1LDM2ODIxNDY3NSw3Nj
kwOTMzMjBdfQ==
-->