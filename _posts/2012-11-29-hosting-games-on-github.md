---
layout: post
title: Hostings Games on GitHub
published: true
---

The intended audience for this post is rather specific: [Game-Off](http://game-off.github.com), [Game On](http://www.mozilla.org/en-US/gameon/), [Global Game Jam](http://globalgamejam.org/) and other [game jam](http://www.gamejamcentral.com/) particpants. Actually, anyone interested in using GitHub to host both their games' source code and the playable version may be interested.

If you have a static-ish game (HTML5, JavaScript, Flash, Unity, etc) with no serverside dependncies (databases, scoreboards, multiplayer, etc) then you can leverage [GitHub Pages](http://pages.github.com/) for free, fast, and reliable hosting.

## Prerequisites

If you're going to follow along with this micro tutorial, I'm assuming the following:

* You have installed Git
* You have a GitHub account; (you can [sign up for a free account](https://github.com/signup/free))

The simple example I have shows basic command line interaction. If you're not comfortable on the command line, you can can also follow along with GitHub's [Mac](http://mac.github.com) or [Windows](http://windows.github.com) clients.

## Level 1: Forking

I'm not going to creating a game from scratch. Instead, I'm just going to [fork](https://help.github.com/articles/fork-a-repo) the game [Coil](https://github.com/hakimel/Coil).

Let's begin with forking that repository now.

![](http://i.imgur.com/aEYtR.png)

## Level 2: Cloning

Next,  [clone](https://help.github.com/articles/duplicating-a-repo) the repository that you've just forked (replace *leereilly* with your username obviously):

![](http://i.imgur.com/WvL9y.png)

<pre>
$ git clone https://github.com/leereilly/Coil.git
Cloning into 'Coil'...
remote: Counting objects: 37, done.
remote: Compressing objects: 100% (26/26), done.
remote: Total 37 (delta 11), reused 35 (delta 9)
Unpacking objects: 100% (37/37), done.
</pre>

## Level 3: Playing

If you open the index.html file you should be able to play the game locally.

<pre>
$ cd Coil/
$ open index.html
</pre>

## Level 4: Pushing

To host the game on GitHub you'll need to create a branch called [gh-pages](https://help.github.com/articles/creating-project-pages-manually).

<pre>
$ git co -b gh-pages
Switched to a new branch 'gh-pages'
$ git push origin gh-pages
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/leereilly/Coil.git
 * [new branch]      gh-pages -> gh-pages
</pre>

Within a few minutes your game will be available at http://leereilly.github.com/Coil. Again, replace *leereilly* with your username.

## Level 5: Custom Domain Names

You can also set up [custom domain names](https://help.github.com/articles/setting-up-a-custom-domain-with-pages). The `CNAME` file in my [leereilly/leereilly.github.com](https://github.com/leereilly/leereilly.github.com) repository ensures that that leereilly.github.com/Coil redirects to leereilly.net/Coil.

## Games Hosted on GitHub

Here are a couple of random  [#ggo12](https://twitter.com/search?q=%23ggo12&src=hash) games that are using GitHub for version control *and* hosting:

* Alge's Escapade [source](https://github.com/dave-and-mike) · [play](http://dave-and-mike.github.com/game-off-2012/)
* Foku [source](https://github.com/Eugeny/foku) [play](http://eugeny.github.com/foku/)
* Hotfix [source](https://github.com/sdrdis/hotfix) · [play](http://sdrdis.github.com/hotfix/)
* Zombie Head [source](https://github.com/condran/game-off-2012) · [play](http://paulcondran.com/game-off-2012/)

## DLC

* [Getting started with GitHub](https://help.github.com/)
* [Getting Started with GitHub pages](https://help.github.com/categories/20/articles)
* [Jump into Game Development with GitHub](http://leereilly.net/2012/05/01/game-development-on-github.html)
* [Creating Static Sites on Heroku](https://devcenter.heroku.com/articles/static-sites-ruby)
