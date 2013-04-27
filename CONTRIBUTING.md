# Contibuting to DrupalCamp Austin website

## Required gems

You may want to configure RubyGems to not install the unneeded RDoc stuff for each gem. To do that, add a `~/.gemrc` file and insert the following lines:

```
install: --no-rdoc --no-ri
update:  --no-rdoc --no-ri
```

In Terminal, run these commands to install everything you need:

```bash
sudo gem update --system
sudo gem install jekyll --pre
sudo gem install uglifier singularitygs jacket
```

## Jekyll server

In Terminal, run the following command to get a server started:

```bash
jekyll serve -w
```

The server will exist as long as your command is running. By default you go to http://localhost:4000/ to see your Jekyll site.

The ```-w``` argument means *watch* so now whenever you (or Sass) make changes to the filesystem, Jekyll will respond by regenerating a new copy of the site. Pretty cool, huh?

We have .gitignore excluding the ```_site``` directory that Jekyll creates because Github will take care of generating that folder when we push to ```gh-pages``` branch.

## Content

Jekyll has a hard requirement for posts' file names. The required format is as follows: ```YYYY-MM-DD-post-slug.md``` — but... we don't want to bother with a valid date for most types of pages. So we're using fake dates for most content. News is the notable exception, which should contain the actual publish date.

```
News: YYYY-MM-DD-post-slug.md
Sessions: 0001-01-01-session-title.md
```