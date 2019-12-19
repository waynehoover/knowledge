# Static Sites

## Generators
- Big list here: https://staticgen.com
### What I use
- ParcelJS - roll your own
    - Waynehoover.com
    - HealingBeats.com
- Docsify
    - kb.waynehoover.com
### Ones I like
- Eleventy - Clean, easy, node based.
- Gridsome - VueJS
- GatsbyJS - React
- SapperJS - Svelte

## Deployment
- Netlify
    - HealingBeats.com
- Firebase
    - WayneHoover.com
- Github Pages
    - kb.waynehoover.com
- Cloudflare
    - Deployed "hostless" via KV store. Only solution that costs $5/month to start. Small amount of space given, not much for images. 
    - Benefit is access to powerful serverless workers that site in front of the site, but can also get this by just using their DNS.
- zeit.co
    - Much like netlify, but faster? access to more language types than netlify for functions. Though the free tier is about half as generous as netlify.

## Headless CMS
- List here: https://headlesscms.org
### Ones I like
- https://sanity.io
- https://forestry.io
- https://contentful.com

### HealingBeats.com
This is basic a static site I built to sell my Binaural Beats.
- created with parcel.js using pug, and tailwind.js 
- Hosting with Netlify. 
    - I might move off netlify because I like the analytics that cloudflare has for free, and Netlify doesn't like cloudflare in front of netlify.
    - Then I would change the forms to just be a standard email signup form that goes straight to emailoctopus.  
- Payhip.io for payments. 
- Netlify forms -> zapier -> emailoctopus.com (AWS SES plan) for email signups.
- DNS hosted with cloudflare, because I'm testing workers for possibly rolling my own authenticated download area.
- MX (email forwarding) hosted by improvmx.com
- AWS for my transactional and even my email list (through emailoctopus)