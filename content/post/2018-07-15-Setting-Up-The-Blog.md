---
title: "Setting Up the Blog"
date: 2018-07-15
lastMod: 2018-07-20
draft: false
url: /2018/07/setting-up-the-blog
tags: ["GitHub Pages", "Hugo", "Blog", "2018"]
---

Now that the selection process is complete, I need to put it all together and get it all setup.
This process will include setting up my [Hugo](https://gohugo.io) environment, configuration of GitHub Pages, and configuration of a custom URL.
Upon completion of these steps, I will be ready to start publishing.

<!--more-->

## Setting Up Hugo

Setting up the Hugo platform is amazingly easy to setup regardless of which OS you happen to run.
The Hugo website contains amazing documentation including a [Hugo Quick Start Guide](https://gohugo.io/getting-started/quick-start/).
This guide walks you through the process of installation, creation of a new site, adding a theme, creating your first post, and some site configuration.
While the quick start guide only discusses MacOS as an installation target, Hugo does support Windows and Linux as well.
I departed from the quick start recipe only slightly by forking the theme and using my own repository as a sub-module.
Outside of that minor change, the quick start got me up and running in less than 10 minutes.

It turns out that selecting a theme in Hugo is very dependant on features you are looking to implement for your site.
Unless you want to build your own theme from scratch, you will need to select from a catalog of [Hugo Themes](https://themes.gohugo.io/).
This may have been the longest part of setting up the site.
While Hugo makes it easy to swap themes, each theme needs to be explored to fully understand the features.
I ended up selecting [Beautiful Hugo](https://themes.gohugo.io/beautifulhugo/) as my theme.
This theme allows be to have a clean reactive site that is suitable for both mobile and desktop browsers.
It also allows for extremely easy configuration of social sharing options, search capabilities ([Google Custom Search Engine](https://cse.google.com/cse/)), [Disqus](https://disqus.com/) integration, tagging, and contact options.
This theme ticked all my boxes and I think it looks good to boot!

## Configuring GitHub Pages

GitHub makes it very easy to setup either a project-based repository for your static site, or a site based off of your GitHub username.
I went with the username option and setup the [wcarroll.github.io](https://github.com/wcarroll/wcarroll.github.io) repository.
Just by setting up this repository, GitHub knows to monitor this repository for static HTML content and attempt to host it on the [GitHub Pages](https://pages.github.com/) platform.
As GitHub expects certain items to be in the root and with the method that Hugo compiles the site, it is important to setup a separate repository for the raw source and the named repository just for your compiled site.

It was important for me to utilize a custom URL and to do so you need to own a domain and have access to edit DNS records.
In my case, my registrar is [Google Domains](https://domains.google).
GitHub's preferred method is to setup ALIAS or ANAME records.
Google Domains does not currently support the GitHub Pages recommended ALIAS or ANAME records, so I had to follow the instructions to setup A records for [apex domains](https://help.github.com/articles/setting-up-an-apex-domain/).
Lastly, I also wanted to ensure that any requests directed to a ```www``` sub-domain would be redirected to the apex domain.
This was as simple as configuration of a CNAME record.
To enable HTTPS, GitHub again makes the process super simple.
Navigate to the repository and select the "Settings" tab.
About two-thirds of the way down you will find the "GitHub Pages" section.
This section is where you will enable HTTPS as well as tell GitHub pages to use a custom URL.
Enforcing HTTPS is as easy as checking a box that says, "Enforce HTTPS" and setting the custom domain just requires that you enter the custom domain in the "Custom domain" box and click "Save".
Once these steps are complete, your GitHub Pages configuration should look like the image below.

![GitHub Pages Repository Configuration](/img/GitHubPagesFinal.png)

## Publishing the Site

Now that I have Hugo installed, my theme selected and configured, and GitHub Pages setup it is now time to publish content!
To create the publishable site with Hugo, all you need to do is run the command ```Hugo``` at the root of your site folder.
Running this command will create a new folder in the root of your site called "Public."
This will contain all the HTML and supporting files needed for GitHub Pages to render a site.
It should be noted that this directory should be added to your "GitIgnore" file to ensure that you are not uploading it to your source repository.
Once the site has been generated navigate to the public folder and configure it for your GitHub Pages repository.
Follow normal Git protocol to init the folder and set the upstream location to the GetHub Pages repository, add the content to the git staging, commit, and push.
That is it.
Within a few seconds to a minute your site will be published.

## Final Thoughts

The learning curve here was fairly shallow and both Hugo and GitHub Pages make setting up a blog as simple as can be and completely free.
I thought that I would struggle with composing in [MarkDown](https://en.wikipedia.org/wiki/Markdown) but I have found it very simple and easy.
Next steps are to continue to publish content and I need to replace the default logo.
I am currently looking at different options to find a graphic designer to get me something new.
Thus far I have considered Fivrr and LogoJoy.
Leaning towards Fivrr, but if you have any suggestion, please let me know in the comments below.
