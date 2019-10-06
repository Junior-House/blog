---
title: How I Built the Blog (Consolidated)
author: Ryan Othniel Kearns
date: 2019-10-05T22:09:44
---

Hello, blog!

First, an outline of some previous posts to the blog that I made during the 'development phase.' Here they are in summary:

**Blog Posts Through the Terminal**

_September 26, 2019_

This post should make it official. The latest blog build, with some simple bash scripting, allows us to write posts using a command-line interface and the Xcode editor. Hopefully I hash out some cooler and smarter features soon!

I will have to write up a little bit of setup that Alex and Harry will be able to follow — the fully automated process involves some environmental variable settings to keep everything consistent. With a bit more development I hope that the process will be totally painless! That should at least make us blog more…

**A Post, Automagically Deployed**

_September 26, 2019_

This post was deployed live all through my terminal session with some small updates to the bash script. Progress!

**Did that Just Work?**

_September 27, 2019_

I think (and this post being online should prove it) that the blog has just moved to its new, permanent, home within the Junior House github organization. Yay! (Yay?) If this is the case, we should expect either of Alex or Harry to come in hot with some unintelligible nonsense sometime soon. Does this blog have spell check?

**...so here we are!**

This blog idea is the spawn of a summertime curiosity for me, and a few days of actual technical work. The process that I went through to bring it to life is outlined below. I'm excited to see where this thing can go with a bit of disciplined content creation.

**Blog, Explained**

This blog is for myself, and also for my two friends & co-founders. It went live about a week ago, as you can see in the timestamps. The source code is open in [this repository](https://github.com/Junior-House/blog) if you're interested in taking a peek. I wanted to build a product for the three of us that was integrated into our technical workflows, had a clear division (for myself) between 'developer' and 'user', and cost us less than \$10 a year -- around 1/20th the price of a WordPress blog for the same scalability.

To accomplish this, I forked a boilerplate blog template from GatsbyJS ([here](https://github.com/gatsbyjs/gatsby-starter-blog)). Gatsby leverages React with querying from GraphQL, two technologies with which I was already familiar, and does all the proper handling for SEO and reusable layout containerizing.

Gatsby's coolest feature, though, is that it builds an entirely static site out of your React app upon deploying. This means no browser-side logic on page-load, giving us a perfect score on Google Developer's PageSpeed Insights despite my using a totally free hosting service, Netlify. I also tweaked the boilerplate project's querying of markdown slugs, which allows blog posts to live within public sub-directories in markdown files. Post files are hundreds of bytes large, and are served with the site, meaning no database config to speak of and no Heroku dynos to wake up. This won't scale without pagination, but I'll solve that problem when I come to it. Currently, the max first input delay clocks in at 200ms.

Next, I wanted to set up automatic site deployments through the repository. With Netlify hosting, I was able to configure rebuilds on commits to our repo's master branch that don't affect site uptime. This has an added benefit in that our site can use GitHub as de facto authentication -- which is gratuitous since no scripting even happens client-side, but a nice note.

My next step was to make posting to the blog totally automated and possible without opening source code. I wrote a bash shell script and defined some aliases in my .bash_profile that name and create the proper sub-directories and files for you. The script also opens vim automatically, which serves as a very intuitive and zen blogging environment :). When the markdown file is saved, the user has the option to deploy it immediately, which automates a commit to the master branch and triggers a rebuild. You can also do this step manually if you'd like to see your changes in Gatsby's dev environment first.

Finally, I wrote up some documentation. You can see it on our GitHub repository. You may think that documentation is unnecessary, since the blog's admin side has exactly 3 users, and you'd be right! I only did so as a kind of practice for building future projects of further complexity, since documentation is so essential to user experience in general.

Oh, and I bought our catchy domain name from Namecheap. That was the cause of the \$8 per year we spend on the project!

It's also not quite accurate to categorize this project as a "past one," since there are a number of improvements I have in my backlog at the moment, including: - Automatic handling of assets. Currently, images have to be loaded in manually into their proper locations in source code. - Improved namespace collision resilience. If you post twice with identical titles, things… get a little hairy currently. I'm thinking of piping a grep call in the shell script to tackle this issue. - Pagination! There must be some way to serve portions of the blog content to different page endpoints to keep our speed up as posts scale. Doing so will require some GraphQL magic for post sorting, but I anticipate there is developer support for doing something of the like with markdown already.

If you have ideas, submit an issue or pull request!! Let's take this thing to space.

Ryan
