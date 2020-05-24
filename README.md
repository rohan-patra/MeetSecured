
![Logo](https://i.imgur.com/aAV4KCD.jpg)

# Demo

[rohanpatra.com/MeetSecured](https://rohanpatra.com/MeetSecured/)

# MeetSecure
Free and Secure Blockchain Vide Conferencing - Based on Jitsi SIP Framework

# What?
MeetSecure is an open-source video conferencing platform. It is encrypted and running on the Ethereum Blockchain network for state-of-the-art security and privacy. 

Video is transfered in two ways, main video feed is transferred via the webRTC protocol for a peer-to-peer conference, and compressed for added streaming speed using Google's Brotli algorithm. 

Subsidiary video feeds are streamed via a decentralized system through Ethereum's Blockchain.

All data is stored in the users' cached and individual users are identified via hardware identifiers such as os, pgp key, viewport, etc. 

# Features

 - Free
 - Unlimited Users
 - Completely Private
 - No Logs
 - Fast Streaming
 - Screen Share

# Technologies Used/Credits

- Backend: NodeJS, webRTC, web3.js, Ethereum Blockchain, PostgresSQL
- Frontend: Bootstrap, ReactJS
- Google Brotli Compression
- SRTP-DTLS Encryption
- [8x8's Jitsi SIP Framework](https://github.com/jitsi/jitsi)
	- Frontend React UI Library
	- In-Browser Video Processing/Decryption/Decompression
- [ethereum-connect.js](https://raw.githubusercontent.com/ethereumjs/ethereumjs-connect/master/dist/ethereumjs-connect.min.js)
- Cloudflare Rate-Limiting and DNS
- DigitalOcean Kubernetes Cluster (Increase Room Sizes)
- [LivepeerJS](https://github.com/livepeer/livepeerjs)
	- Communicate with the Ethereum network and implement live, instantaneous video transfer over blockchain

# Coming Soon...

 - Mobile Apps
 - One-Time Use Links
 - Secure In-Chat File Sharing
 - Realtime Closed-Captioning
 - Text-to-Speech Via Chatbox
 - REST Api
 - reCaptcha V3
 - AI-Based Compression Algorithm Decisions on-the-fly
 - Flask Universal App
