# CONTEXT

FRIEND ASKS MY OPINIONS ABOUT BSKY, SAYS THEIR MAIN ISSUES W/ SOCIAL MEDIA ARE POLITICAL/PSYCHOLOGICAL/SOCIOLOGICAL/ETHICAL

I GIVE A STREAM OF CONSCIOUSNESS RESPONSE. THIS IS NOT FACT CHECKED, THAT'S WHAT I'M GOING TO DO BEFORE PUBLISHING THIS FOR REAL.

PLEASE DON'T GET MAD IF IT'S WRONG

# RAW MESSAGES

i'm not particularly interested in the anthropic issues, because i don't think of those as endemic to social media as much as they are endemic to society as a whole. 
To solve the idea of influence operations on any social media platform would be akin to solving the concept of influence operations in and of themselves;
social media is just a technological development, and every technological development that proliferates on the internet is going to contain the best and worst aspects of any individual, 
group, or community that has access to the internet. 

that said, the technological problems that the current generation of social media platforms are trying to solve are about creating or explicitly rejecting system architectures that 
reflect the way in which the creators believe they can address those problems. 
so my thoughts are going to be focused on the technology and what that means for downstream development or consumption

> ![NOTE] NOTE:
> `[FRIEND 2]` SAYS THEY ARE UNFAMILIAR WITH THE THREE SO I GIVE AN OVERVIEW:

right now there are a slew of alternatives to twitter/facebook/etc. there are some like cohost that are just kinda trying to be A New Twitter, 
and iirc they're about to go belly up because they're not actually trying to solve what seems to be the consensus opinion of the other alternatives:

1. Users should be able to maintain some level of ownership over their online identity
2. Users should be able to migrate their data between providers of the social media service they use
3. The solution is not to create a new Twitter, but to create a protocol for how social media platforms should interact with each other in ways that solve 1 and 2

a similar divergence is happening for chat platforms like discord, but i'll limit scope to just microblogging sites

from what i've seen, there are two primary protocols that have emerged as viable options for a path forward (with a third existing but not really taking off to the same degree): 
ActivityPub, ATProtocol, and Nostr.

Mastodon is built off ActivityPub, and Bluesky is built off of ATProtocol. 
Nostr doesn't have a platform per se, since their protocol attempts to emulate the decentralized nature of protocols like bittorrent and bitcoin.

For Mastodon and Bluesky, there's a similar decentralization push, but conceptually they diverge quite rapidly from nostr, then from each other

All three want to be social media type agnostic, and solve things in different ways. 
ActivityPub is a baseline that gets extended into different types of sub-protocols that emulate popular sites like twitter, imgur, reddit, etc., 
where communities can build up around specific server instances that utilize one or more of these sub-protocols 
(e.g. infosec.exchange is built off mastodon, but there's also a lemmy instance that is connected to the same AP accounts hosted on infosec.exchange)

Bluesky lumps everything into an action on a blockchain-adjacent algorithm called a merkle tree, 
and uses a three-tiered delivery system where all those actions get sent out from user-or-company-hosted servers to something they call the "Firehose". 
from there, the social media "type" is just a specific type of UI application that uses a filtering algorithm to decide what kind of content gets displayed

Nostr just treats everything as a JSON object and then has these things called NIPs (nostr implementation possibilities) that i guess are like... 
optional add-ons for a specific UI that listens to nostr relays? i don't really fully grasp what they're going for

where my opinions come in are on the pros and cons of the design philosophies that APub and ATProto, and that i've already kinda discarded nostr

all three are trying to approach a federated system model, to follow in the whole decentralized thesis that seems to be required to solve the 3 problems mentioned above. 

nostr is dead simple - you have a client, which lets users connect to relays, which can be hosted by users or providers. 
the users have their own keymat, the clients validate the keymat, and pull/push data from/to the relays on behalf of the users.

activitypub is more graph theory in how it approaches federation - an instance is stood up by a user or provider, which connects to other instances. 
the instance can choose to defederate with specific nodes on the graph, and other nodes can choose to defederate with this new instance. 
when a user makes an account on an instance, all their data is hosted on and tied to that instance.
they can change instances, but basically all they're doing is issuing a notice to the instance they're joining to link up the followed/following 
from the old instance and then posting a redirect notice on the old account profile.

my opinion: these are good solutions for certain types of communities, but do not work as a universal protocol for social media. 
to your point about the social/political issues present on social media platforms `[FRIEND]`, 
nostr takes a decidedly anti-censorship stance and leaves it up the the user, while activitypub centralizes power in instance administrators. 
i think both of these approaches would prevent communities from having the tools/resources required to handle those problems, 
and i think it is ultimately up to communities to handle issues like that because i don't see any way in which you can solve those issues through technology alone

i think activitypub is great if you want to have like... your own small little webring, or for people who want to engage in a form of roleplaying where you social media in-character, 
or (if you are the kind of person who thinks it's not weird) a company could have a private social media their employees can connect over

niche communities with niche interests connecting only with other niche communities with niche interests. fiefdoms if you want to be cynical, but i don't honestly believe they are like that

with ATProtocol, you're given a unique identifier, and all your data is tied to that unique identifier. 
it's a double edged sword, because much like cryptocurrencies it is pseudonymous - whatever persona you've given to that ID will be 100% traceable, visible to anyone who is watching the firehose. 
even when bsky was in closed beta, there were constant reminders about how it wasn't and will never be private. 
but that trade off allows the user to actually retain total control over their data. 
as long as the interactions were sent out to the firehose, your data can be transferred between whatever server you want to host that data on.

because there are those separated layers, you can create a more personally curated social media environment - you choose who hosts your data, 
you choose who tracks the firehose, you choose who filters the firehose, and you choose who displays that information to you. 
and because your data is tied to your ID, you still retain the sort of "i can do every bit of this myself" independence that nostr is trying to allow, 
while also being accessible to the broadest possible user base

personally i really like bluesky, but i also have an account on infosec.exchange (a mastodon instance). i'm @mussar.io on bsky (cause you can set your handle to be any domain you can edit the TXT record of)
