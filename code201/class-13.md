# Local Storage

One area where native client apps have had an advantage over online applications is local storage.
Every HTTP request includes cookies, which slows down your online application by transferring the same data over and over again. Every HTTP request includes cookies, which sends data across the internet unencrypted (Unless your entire web application is SSL-encrypted) Cookies can only store roughly 4 KB of data, which is enough to slow down your program, but not enough to be very useful. **what we want is** a lot of client storage space that lasts longer than a page refresh and isn't sent to the server


# A Brief History of Local Storage Hacks Before HTML5

- In 2002, Adobe introduced a feature in Flash 6 that gained the unfortunate and misleading name of “Flash cookies.” Within the Flash environment, the feature is properly known as Local Shared Objects.

- Brad Neuberg developed an early prototype of a Flash-to-JavaScript bridge called AMASS (AJAX Massive Storage System), but it was limited by some of Flash’s design quirks.

- Flash gives each domain 100 KB of storage “for free.” Beyond that, it prompts the user for each order of magnitude increase in data storage (1 Mb, 10 Mb, and so on).

- By 2009, dojox.storage could auto-detect (and provide a unified interface on top of) Adobe Flash, Gears, Adobe AIR, and an early prototype of HTML5 storage that was only implemented in older versions of Firefox.

# Introducing HTML5 Storage

“HTML5 Storage” is a specification named Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons.

Also, almost evey browser with latest version supports HTML5. here is an image that show you the html5 browsers.
![](images/browser.png)

# Using HTML5 Storage
You store data based on a named key, then you can retrieve that data with the same key in JavaScript.