+++
comments = false
slug = ""
toc = true
draft = false
date = "2016-10-24T03:12:08+07:00"
title = "My very first post: Use Hugo to build a blog"
featured = "img/featured/hugo.jpg"

+++
![Hugo](/img/hugo.png)

It's 2 in the morning, and i was still awake to finish my first blog. Not the first, but like the first serious one which i really put my mind to. So, you guys maybe wonder: why did i have to suffered a lot like that, for just a blog?

# Why not Wordpress
Wordpress is kind of easy, but **Wordpress is old**. And it becomes bigger and more complicated every single year. I don't want a giant CMS with an entire database, dealing with tons of logic, just for a single simple blog.
So it came up when I read an article about the ***static site generator*** on SitePoint, which was taken down eventually, and they said that this is the future. I'm like "What the... How cool is that!" and started to look for it. And it turns out pretty amazing :)

# So, what is a static site generator
Just simple like this: the generator takes the input file (Markdown files, in my case), and turns them into static mark-up, ready-to-render files. After that, we can immediately serve these static files, without the server cares about anything else. And it runs the generator on our computer, not the server.

[Hugo](https://gohugo.io/) is a static site generator written in Go, and it's so awesome.

---

# The Hugo

### It runs anywhere
Written in Golang, so yeah, runs on any platform.

### Performance
I think maybe [Hugo](https://gohugo.io/) is the **fastest static site generator** in the world. And they think so too. Wordpress looks like nothing compares to this monster :)

<iframe width="100%" height="315" src="https://www.youtube.com/embed/CdiDYZ51a2o" frameborder="0" allowfullscreen></iframe>

With the generated files, the server will response to the requests in lighting fast.

### Flexible
You can customize the site in anyway you want, and it seems easier (*no it's not*) cause we don't have to deal with tons of code or plugins or widgets or server-side effect... It's just fun and simple.

## And that's enough reasons for me to use Hugo
---

# How I built it

Just download the .deb file and install, then you good to go. Now I will show you **how to deploy it on Github pages**, and get a free custom domains.

### Get a free domains at <a href="http://freenom.com" target="_blank">Freenom</a>
Register a domain and then we will configure it later.

### Deploy our site with <a href="https://pages.github.com/" target="_blank">Github IO</a>
![My githubio page](/img/githubio.png)
Just follow the instruction, so you can have our site visited at something like `kiendt07.githubio.com`. Don't visit this, cause I already change it to a custom domain. Let's see..

### Change the custom domain in Github settings
![Change to custome domain](/img/custom_domain_github.png)
Go to the Github repo that you contain the site, click Settings, and then type the domain that you just registered on Freenom. Then we move to the final step

### Change the DNS settings of our domain
* Look in to My Domain after log in to [Freenom](http://freenom.com)
![My Domains](/img/my-domains.png)
* Click on Manage Domain of your target domain
* Go to Manage Freenom DNS tab
* Add two `A` records in `TTL` and `Target` column to FreeNom DNS provider and click Save changes
  - `3600` `192.30.252.153`
  - `3600` `192.30.252.154`

    like this:
    ![DNS records](/img/dns-records.png)
    
    You may just have to understand that the DNS config from above will redirect every single request to our custom domain, point to out githubio domain.
* Then we're good to go. Wait at most 5 minutes, then navigate to our domain. See the painless magical.

---

# Summary

I created my site by using [Hugo](http://gohugo.io), with `VEC` theme. Feel free to check that out.
The domain `.tk` I used was registered on [Freenom](http://freenom.com), and [Github Pages](https://pages.github.com) for serving static files.
So, last but not least, check my site usually guys ;)  hahaha

### [JBroc.tk](http://jbroc.tk)

