# Pandora's Box

*From 2024 Cyber Skyline National Cyber League Gymnasium*

The hackers have created their own custom protocol for private communication. Luckily, our analysts have managed to obtain the documentation describing the protocol. Use it to fill out this report.
Overview

The communication between the client and server will contain three types of messages: Initialization, Encrypt Request, and Encrypt Response.
A connection is started with the client sending an Initialization message, which contains the number of Encrypt Requests that the client wishes to make.
Then, the server will send the length of its response.
Then, the client sends their Encrypt Requests to the server.
After all of the Encrypt Requests have been received, the server will finish sending a single Encrypt Response which contains hashes of all of the data that was sent by the client.
Initialization (Client -> Server)

    N - A 4-byte integer in network byte order that represents the number of Encrypt Requests that will be sent.

Encrypt Request (Client -> Server)

    Check - A fixed 2-byte integer in network byte order that verifies the integrity of the message.
    Len - A 4-byte integer in network byte order that represents the length of the data in bytes.
    Data - The data that will be encrypted.

Encrypt Response (Server -> Client)

    Count - The length of the data, in bytes, that follows.
    Hashes - The encrypted hashes requested by the client. Each hash is in the form of a fixed-length chunk. These hashes are in the same order that the requests were made.


## Questions

1. What is the IP address of the server?
2. What is the IP address of the client?
3. What port is the server listening on?
4. What is the magic 2-byte ID in decimal representation?
5. How many encrypt requests were made by the client?
6. What is the length of the first encrypt request (in bytes)?
7. What is the length of the second encrypt request (in bytes)?
8. How large is an individual encrypt hash (in bytes)?
9. What was the encrypt response, in hexadecimal representation, for the first request? (e.g. 123456789ABCDEF)
10. What was the encrypt response, in hexadecimal representation, for the second request?
11. What is the hidden flag being sent over the protocol?
