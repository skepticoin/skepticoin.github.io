---
layout: page
title: Getting started with Skepticoin
permalink: /getting-started/
---

Follow the instructions below, and experience the thrill of being an early
adopter without any of the guilt of doing something that you deeply don't
believe in.

The quickstart assumes (for now) that you have Python up and running. _The instructions below are written with
Linux/POSIX in mind._

* If you're a MacOS user, it is presumed that you have `python3` installed (either by e.g. using `pyenv`, or using a recent version of macOS).
* If you're a Windows user, remember to use `Scripts\activate.bat` instead of `.bin/activate`.

```
# Installing:
$ python3 -m venv .
$ . bin/activate
$ pip install --upgrade skepticoin
[..]
Successfully installed skepticoin-0.1.2 ecdsa-0.16.1 immutables-0.15 skepticoin scrypt-0.8.18 six-1.15.0

# Receving coin (copy/paste the cryptic string to someone who can send you money):
$ skepticoin-receive "I want my coin"
Created new wallet w/ 10.000 keys
SKE815dea23355609057721c08fe754efa855b50606949edb3dc300870b2c3f280115d29ea00ce76b202f7bd5fe38c917370cc8a4629a8bc10bf3e344d50d850b02PTI


# Sending coin:
$ skepticoin-send 1 skepticoin SKE815dea23355609057721c08fe754efa855b50606949edb3dc300870b2c3f280115d29ea00ce76b202f7bd5fe38c917370cc8a4629a8bc10bf3e344d50d850b02PTI
Created new directory for chain
Reading chain from disk
[..]
00019000-0130dc3498df05743b3b9a94a8543a5bb06167d7351b827312508b34bb351014
[..]
Creating new peers.json
Starting networking peer in background

NETWORK
Nr. of connected peers: 3           <= watch this to make sure your're connected to the network
  xx.xxx.xx.xxx:2412 - OUTGOING
  [..]

CHAIN
Height    ...
Date/time 2021-03-22T13:36:16       <= watch this bit to get a sense of how the blockchain download is coming along

[.. the above repeats for a while ..]

Chain up to date
Broadcasting transaction on the network Transaction #...........
Monitoring...
Transaction confirmed at .... with 0 confirmation blocks

# Mining
$ skepticoin-mine

[.. similar to the above ..]

Waiting for fresh chain
Starting mining
FOUND 000xxxxx-000xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx <= this displays the height and hash of what you just found
Your wallet now contains 2730 skepticoin                                        <= this is where you start dreaming of a lambo
```

Note that skepticoin's scripts will create whatever files they need to operate
right in the directory where they're being called. This includes your wallet.
