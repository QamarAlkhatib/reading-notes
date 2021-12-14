# Authentication & Production Server

## What exactly is a JSON Web Token?

JSON Web Token (JWT) is an open standard (RFC 7519) that specifies a compact and self-contained method for securely communicating information as a JSON object between two parties. Because it is digitally signed, this information can be checked and trusted. JWTs can be signed using a secret (using the HMAC algorithm) or with an RSA or ECDSA public/private key combination.

## When should JSON Web Tokens be used?

JSON Web Tokens are useful in the following situations:

- Authorization is the most typical case in which JWT is used. Each subsequent request will include the JWT once the user has logged in, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a popular feature that makes use of JWT nowadays due to its low overhead and ability to be used across multiple domains.

- Information Exchange: JSON Web Tokens are an excellent way to send information securely between parties. You can be sure the senders are who they say they are because JWTs can be signed—for example, using public/private key pairs. You may also check that the content hasn't been altered with because the signature is calculated using the header and payload.

--------

## DRF JWT Authentication

An access token and a refresh token are obtained by trading a username and password for a JWT.

The access token is usually only valid for a short period of time (expires in 5 min or so, can be customized though).

The refresh token has a slightly longer lifespan (expires in 24 hours, also customizable). It's similar to a session of authentication. After it expires, you'll need to re-login with your username and password.

## What is the reason for this?

It's a security feature, as well as the fact that the JWT contains a little extra information.

--------------------------------

## Django Runserver Is Not Your Production Server

A typical production setup comprises of several components, each of which is designed and developed to excel at a single task. They are quick, dependable, and laser-focused.

When a request comes in, it should be forwarded to a separate web server. Nginx is an excellent example of a web server.

This is a program that can serve static files from disk (such your CSS and JS files) and handle many requests at the same time. The webserver is configured to transmit this request to the next component if it is not for a static file but should be processed by your application. An application server is the next component. It takes those fancy requests and turns them into Python objects that Django can use. WSGI is a specification that describes how that happens, and it was developed by a group of people. Gunicorn is a WSGI server that can be used as an example.
