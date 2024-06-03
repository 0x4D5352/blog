# RESEARCH DOCUMENT

# QUESTIONS TO ANSWER:

- [ ] How do the following protocols *actually* work?
    - [ ] ActivityPub
    - [ ] ATProtocol
    - [ ] Nostr
- [ ] How can I diagram each protocol?
- [ ] What are the pros and cons of each?

# LINKS
https://atproto.com/
https://www.w3.org/TR/activitypub/
https://nostr.com/

# REFERENCES


# QUOTES



# ATProtocol

## Overview

Authenticated Transfer Protocol

Each user is assigned a cryptographic URL called a DID (Distributed IDentifiers), which are associated with a URL and 
a domain name that references that URL. A User's interactions are stored in cryptographically signed repositories which contain
records of all the interactions that user has with the network, such as posts, comments, likes, etc. These repositories are 
federated over the AT Protocol, and services can be built to facilitate user interaction with the network. The network's
capabilties can be extended through the use of "Lexicons", which are standardized naming conventions for featuresets such as
syncing user repositories and performing social interactions.

All services can be built by stacking those three core primitives:
1. Repositories
2. Lexicons
3. DIDs

Example services that exist include the three core services of Personal Data Servers, Relays, and App Views, as well as services
like feed generators and content labelers.

ATProtocol is built around the idea of enshrining user control over their data and their experience on the social network, even
if the user does not control the services that they utilize to interact with the network. A user can choose where they host their
repository, which aggregation sources they use, which application they use, etc. This is intended to allow for two separate
"layers" within the network, separated by personal, community, and organizational curation and moderation - the "Speech" layer, 
which distributes authority and retains user autonomy, and the "Reach" layer, which is filtered to enable actions to be taken to 
combat problems like misinformation, bigotry, and propaganda.

## Repositories


## Lexicons


## Distributed Identifiers (DIDs)



# ActivityPub





# Nostr
