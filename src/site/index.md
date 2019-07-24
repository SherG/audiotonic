---
title: AudioTonic
subtitle: We create Alexa skills for small businesses and non-profits
layout: layouts/base.njk
---


## What are Alexa skills?

Alexa skills are interactive voice apps designed for use with Amazon devices like the Echo Spot, Echo Show and <a href="https://www.amazon.com/Introducing-Echo-Auto-first-your/dp/B0753K4CWG/" target="blank">Echo Auto</a>. 

- AudioTonic creates new skills that use Alexa's built-in capabilities
- Alexa's abilities include: answering questions, recommending local businesses, playing music, querying a data source, and providing news updates 
- Alexa skills come in a variety of <a href="https://www.amazon.com/b?ie=UTF8&node=13727921011" target="blank">categories</a> like "Business & Finance" and "Health & Fitness"


## About Alexa Devices

The pages found in in the posts

<ul class="listing">
{%- for page in collections.post -%}
  <li>
    <a href="{{ page.url }}">{{ page.data.title }}</a> -
    <time datetime="{{ page.date }}">{{ page.date | dateDisplay("LLLL d, y") }}</time>
  </li>
{%- endfor -%}
</ul>

## Links from an external data source

These links were sourced from [hawksworx.com](https://www.hawksworx.com/feed.json) at build time.

<ul class="listing">
{%- for item in hawksworx.entries.slice(0,5) -%}
  <li>
    <a href="{{ item.link }}">{{ item.title }}</a>
  </li>
{%- endfor -%}
</ul>


## What's next on the Alexa horizon? 

- Automotive is the new frontier. With Echo Auto you'll be able to query your car from within or another location. 
- Ask questions like "What's my EV charge status?" "What's my fuel level?"
- Enjoy voice-controlled navigation. Set appointments, make calls, add items to a task or shopping list, play audiobooks or music from various sources
- Create routine, location-based actions.
- Amazon has forged partnerships with Ford, BMW, Hyundai, and Volkswagen. <a href="https://www.amazon.com/Introducing-Echo-Auto-first-your/dp/B0753K4CWG/" target="blank">Echo Auto is currently available by invitation only. 
  

## Running locally

```bash
# install the dependencies
npm install

# External data sources can be stashed locally
npm run seed

# It will then be available locally for building with
npm run start
```

## Add some Netlify helpers
Netlify Dev adds the ability to use Netlify redirects, proxies, and serverless functions.

```bash
# install the Netlify CLI in order to get Netlify Dev
npm install -g netlify-cli

# run a local server with some added Netlify sugar in front of Eleventy
netlify dev
```

A serverless functions pipeline is included via Netlify Dev. By running `netlify dev` you'll be able to execute any of your serverless functions directly like this:

- [/.netlify/functions/hello](/.netlify/functions/hello)
- [/.netlify/functions/fetch-joke](/.netlify/functions/fetch-joke)

### Redirects and proxies

Netlify's Redirects API can provide friendlier URLs as proxies to these URLs.

- [/api/hello](/api/hello)
- [/api/fetch-joke](/api/fetch-joke)




