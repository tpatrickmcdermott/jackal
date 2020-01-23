---
layout: post
title:  "Jekyll Setup Notes"
date:   2020-01-22 10:10:34 -0500
categories: jekyll update
---

## Mac Installation

(Assuming Ruby installed)
* Install Bundler (ruby gem)
* Create Gemfile
  * Create a directory and add a file called *Gemfile* (no extension)
    * Contents:
    ```
    gem 'github-pages'
    source 'https://rubygems.org'
    ```
* Install jekyll (this will create a new subfolder which is the actual site)
  * `jekyll new {siteName}`
  * Change to new directory and initialize a Git repository
    * `cd {siteName} | git init`
* Fire it up!
  * `jekyll serve`


## Customizing Jekyll
### Configuration

Edit \_config.yml. Default install version:
```yaml
# Site settings
title: Your awesome title
email: your-email@domain.com
description: > # this means to ignore newlines until "baseurl:"
  Write an awesome description for your new site here. You can edit this
  line in _config.yml. It will appear in your document head meta (for
  Google search results) and in your feed.xml site description.
baseurl: '' # the subpath of your site, e.g. /blog/
url: 'http://yourdomain.com' # the base hostname & protocol for your site
twitter_username: jekyllrb
github_username: jekyll

# Build settings
markdown: kramdown
```

Edited version:
```yaml
title: Paddy's Jekyll site
email: dev1@pmcder.com
description: >- # this means to ignore newlines until "baseurl:"
  A guide to getting started with Jekyll (and learning how to spell 'jeckal')
baseurl: "" # the subpath of your site, e.g. /blog
url: 'http://localhost:4000' # the base hostname & protocol
twitter_username: jekyllrb
github_username:  tpatrickmcdermott

# Build settings
sass_dir: _sass
include: [_pages]
kramdown:
  input: GFM
theme: minima
plugins:
  - jekyll-feed
```









<hr style="margin-top: 4em; margin-bottom: 4em">

#### boilerplate stuff below

```css
  body {
    background-color: #99f;
  }
```

```javascript
const arr = [];
function foo() {
  return 'bar'
}
```

{% highlight javascript %}
const arr = [];
function foo() {
  return 'bar'
}
{% endhighlight %}

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
