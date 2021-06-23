---
title: "How I Make My Site"
date: 2021-06-23T17:15:42-04:00
draft: false
---

**How I Make My Site**

My site is pretty minimalist. It’s just a static site - no dynamic content, no
tracking[1], and no client-side JS at all. That being said, I’m not digging
around my text editor opening and closing `<p>` tags by hand. I’ve done that for
sites in the past (when I was _slightly_ more of a noob) and it’s a pain. If I
find myself needing to copy/paste changes across multiple files - it’s time to
rethink my approach. I’ll show you how I make this site and maybe it will work
for you.

**Static Site Generator**

I use a static site generator named [Hugo](https://gohugo.io/). That’s it.
That’s the secret sauce that will get you 90% of the way there.There are a ton
of great [themes](https://themes.gohugo.io/) that are free to use and modify.
People have made themes for all kinds of focus areas like blogs, photography
portfolios, you name it. You can grab one and adapt it to your needs.

Personally, I found a lot of Hugo’s features a little intimidating at first and
I wasn’t always able to find what I needed in the docs. The most helpful
solution for me was exploring the example project inside of a theme’s repo.
Being able to see the different components and how they’re put together made
things a lot more clear. You can play with the layout and content using hot
reloading (`hugo server -D`) and see how the changes affect the output.

Initially, I write each blog post, page, etc. in
[markdown](https://guides.github.com/features/mastering-markdown/) and make sure
to finish the content before really focusing on the presentation. The truth
about all this is that content is the most important thing. Look at [Dan Luu’s](https://danluu.com/) 
site. It’s not winning any design awards - but that doesn’t stop it from being
one of the best programming blogs on the entire internet.

Once the content is squared away, I’ll fire up Hugo’s dev server and make sure
it looks right. Again, the hot reloading really shines here - any change is
reflected immediately. Once a post looks good to me, I commit the repo and push
to my [GitHub](https://github.com/drake6m).

**Hosting**

For domains, I use [Porkbun](https://porkbun.com/) and I’ve never had any
problems. This is the **only money I spend** on the site, costing me just
$4/year.

I use [Netlify](https://www.netlify.com/) for hosting and I would highly
recommend it to anyone with this use case. After initially setting up the Hugo
build process, I have **never** had to even think about it again. Whenever I
push the repo, Netlify begins the build process and takes it from there. After a
build (Netlify will show you the logs in case something goes wrong), the changes
are live and served right away.

That’s it! Once you get the process set up, it’s super easy to add content and
update the site.

I do use a Google font, and I assume they’re paying attention to the “Referer”
header if your browser sends one.
