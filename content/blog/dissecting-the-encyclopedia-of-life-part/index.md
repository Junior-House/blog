---
title: Dissecting the Encyclopedia of Life [Part 2]
author: Alex Langshur
date: 2019-10-15T21:34:00
---

**Chapter Two: A Small Revelation**

Per usual, my paradigm-shifting revelation strikes as I'm in deep within a far-too-hot shower. As I'm slamming the glass door open and wiggling towards the nearest red towel, I notice that several key details of the original thought are already slipping away. Shit... Hands on a computer keyboard no more than 45 seconds later, I desperately jot down the important stuff. Here we go.

I'm thinking about this all wrong. The majority of my early thoughts concerning the dynamics of the Encyclopedia of Life (simpler, more brandable name coming soon) solely involved users and their experiences -- a first user would share an experience and a second user would reap the benefits of this shared experiential knowledge. Yet, this idea is unclear in many ways. What is experiential knowledge? Why would users share their knowledge? Why would anyone be incentivized to help others out? 

It was with these internal questions that the revelation hit. I quickly realized that by basing a platform on a form of knowledge as specific as the broadly empirical (i.e. experiences), I was massively overcomplicating. Instead, users would benefit (for reasons of sharing and reading) far more from a far less narrow definition of the allowed content. I needed to expand on my trivial concept of experience sharing to include any other form of geographically positioned information that users enjoy sharing. 

With this step forward, the second half of the revelation hit. EOL should not be a medium for users to share and read about experiences. EOL needs to be a social media environment for learning and engaging a city (I use this word a lot to refer to any metropolitan entity) on a far more personal and social level than ever thought possible -- where people in a city can come together to talk about anything, from interesting experiences to interesting news to interesting events, all of which are pinpointed directly on the map. EOL will be built to bring a city closer together than ever before. Below I want to dissect the three verticals that "synergize" this vision:


**Vertical 1: Content sharing.**

The most fundamental vertical that I'm going to cover is that of content sharing -- how do users share with the rest of the platform and what will this look like under-the-hood? The idea here is that a user will be able to add a post to the map that targets a specific location. This post will spawn a thread exactly like any thread on Reddit -- a small communication environment where people can pseudo-anonymously communicate with one another (which has been proven to setup a rich dialogue between users) about the post at-hand (as well as any spurious topic that intercepts the flow of dialogue as Reddit has demonstrated) and vote on comments ("upvote" or "downvote") for the sake of crowd-sourced content moderation. 

In a large city, it is unlikely for a single post in a specific location to go unaccompanied. In fact, considering that individual posts/threads will occur densely within densely populated environments, we can use keyword detection (and maybe even semantic construction) among geographically clustered threads to deduce the popular purpose (as well as opinion, in theory) of that location on the map (greater confidence rating if overlayed threads share a set of keywords). This will be very important when delivering query responses to a user -- based on a specific user query (such as for the most unbelievable nightlife experience), we can return a set of threads attached to an appropriate search location (perhaps a retro bar or nightclub) that we derived using overlayed post keywords. 

Moreover, we can use a user's post to begin building them a powerful preference profile -- if we register a user's post about an enjoyable lakeside picnic location, for example, we can attach the post's keywords (and the confidence-boosted keywords of clustered posts) to the user under-the-hood to derive better content suggestions in the future. 


**Vertical 2: User experience.**

**Sub-vertical 2.1: Content lookup.**

The first component of this vertical was highlighted briefly above -- a cornerstone utility that the platform will provide is the ability to lookup threads/posts around a city that would be of direct interest to the user. The idea here is to take an exponential moving average of the histogram frequency for each keyword that the user interacts with over time (iterate the EMA each new-day login). This will build a powerful descriptor for the user's general platform preferences and will tie directly into deciding the results of a user's content query.

Note that there are two possible routes for handing search results back to the user. The first, most simple idea is to grant users a set of relevant threads dispersed throughout the city: these will be decided by a number of criterion ranging from thread popularity (this is important since posts should receive a correct amount of attention and comments -- not starved of attention and not over saturated with activity), user preferences, and query-to-thread keyword matching. The second possibility is to grant users a set of thread containers throughout the city -- these are bundles of trending and relevant threads that belong to a single unified location around a map. The main difference between these two approaches is that the former will narrow down all the related threads from a specific location into a single most popular and relevant thread, whereas the latter will return collections of the highest-scoring threads for a single location (you can think of the latter idea as defining each location with multiple threads as its own subreddit, and then returning these subreddits throughout the map to the user). 

**Sub-vertical 2.2: Content catering.**

As explained above, EOL will most definitely provide the ability to users to intentionally search for threads on the map (whether that be targeted experiences around the city, news on a specific location, or anything else). Yet, this active form of user participation should never be relied upon. People are inherently lazy. Every platform that strives to not drive users away in large groups must always provide a form of passive use. In the case of the Encyclopedia of Life, this would take on the form of general content suggestion to the user -- threads around the city that may peak the user's curiosity (based on their preference profile as outlined above) or perhaps interesting locations (deduced from clustered threads as was also explained above). This functionality should support a limitless emission of fun content for users to explore and intake without turning on their thinking caps and actively targeting platform knowledge.


**Vertical 3: Event posting (Advertisement and Sponsorship Opportunities).**

One of the most exciting possibilities that would drive the utility of the platform through the roof is the inclusion, and potential monetization of, events. Before jumping into the specifics of this vertical, let me first talk about the inspiration. My hometown, Chicago, has the most fantastic summers (in my humble opinion) -- my pals and I lose our shit at the dozens of events, from Taco Fest to Pride to Wicker Park Fest to large music festivals (e.g. Lollapalooza, Spring Awakening, Mamby on the Beach, etc) and many, many, many more. There are always things to do. 

Yet, these public events are often really hard to come by. I consider myself a relatively active internet adventurer -- and I rarely stumble across these events online. Can you imagine having them all in single, hyper-clean map format? EOL could make this a reality. What's more: EOL could factor these events directly into each users' preference profile to enforce that everyone sees the most absolutely relevant events (without crowding the UI). 

Let's chat briefly about a monetization caveat imposed by this idea -- direct advertisement and event sponsorship on the platform. While I would never allow a business to influence the content catering or lookup processes above for user content (Yelp does this. Need I say more?), a sponsorship program for events could be incredibly effective. For example, imagine if the Chicago Cubs (go Cubbies) came along after a disappointing end to their 2019 season and wanted to raise attendance for the 2020 season home opener (this will never happen BTW; Cubs attendance is absolutely stacked)? The Cubs organization could sponsor an event-display on the map UI that users will be forced to see (sort of like Google Ads in the search engine). If the event space on EOL takes off -- if it gathers attention as the only true place to easily learn about your city's events --, then the potential for strategically sponsoring events would be absolutely unprecedented. 


That's it folks. The various ideas discussed throughout need some de-wrinkling, but that next iteration of understanding will be saved for a future post in the series. There's a certain sweet spot in the conception of an idea where additional chit-chat without laying your paws on the technology gets unproductive. I believe I'm approaching that point. A small closing remark: if an idea is truly impossible, drop it immediately. If the risk is any less than that level, you love the idea, and you possess the requisite technical knowledge, build the damn thing. That's where I am and that's where this project is going.
