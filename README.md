### What?
This small gzip decompressor unzips the string ('#Zip/H4sIAAAAAAAA...') and renders it.

Inspired by [itty.bitty.site](https://itty.bitty.site)

This tool is hosted on the [IPFS](https://ipfs.io/ipfs/QmXwkqP9kLPRNu9U2W2E4imoztAJryijXPQQnjQ9EYCXnz?filename=unzip.html).

You can create small sites, resumes, animations, games, comic strips, and share them without the need to host them anywhere on the internet.

They are hosted by URL shorteners and your Twitter messages and can be engraved in a blockchain.
### How?
By zipping the HTML in the URL hash. Everything after the # sign is rendered by the browser on visiting the page, and there is no need for a server to host the site.
### Why?
It's fun! And it is convenient - it is decentralized and doesn't cost a penny to run! Create and share for free.
### Limitations
Size is the main feature and also a limitation, but even then you can use libraries 
like preact (3kb) and split your site in a meaningful way and link to the pages with a 
URL shortener like [tinyurl.com](https://tinyurl.com/). You can also use popular CDN libraries if you are willing to sacrifice self-sufficiency.

The biggest challenge is that even though the browser may be able to read big URLs - I've tested with a text that produced an 87k character URL hash and I could still copy and paste it, but probably most URL shorteners and message apps will truncate your URL. Tinyurl supports up to 32k character-long URL, others do merely 4kb. [Here](https://stackoverflow.com/questions/417142/what-is-the-maximum-length-of-a-url-in-different-browsers) is an stack overflow answer on the subject. 

But then again, for books or sites that can be split into multiple parts, you can set up your build to split into 4k to 32k symbols per page, create URLs yourself and shorten them with a shortener API and link them together, starting from the last page.

*Should* you do it only because you *can* do it? In most cases using Gatsby to create sites and then to deploy with Fleek is a more meaningful approach.
### Features
Your site can run javascript.
### Donations
If you are a very rich person (have more than one Lambo and/or a Rocket) 
and wish to make my life better, your donations will be deeply appreciated.

### Roadmap
 - Alpha version - build functionality - written in a single file without build process. Hosted on IPFS with regular DNS domain.
 - Beta version - add stability - build with framework and add tests. Add CI with Fleek. Add .eth domain.
 - version 1 - add PWA with service worker and offline support 

### To do
 - [x] publish alpha version
 
 For beta version:
 - [ ] compare GZIP with alternatives like LZMA, LZJB, LZW, BZIP2, LZP3
 - [ ] set up build with webpack and add preact
 - [ ] set up deploy with Fleek