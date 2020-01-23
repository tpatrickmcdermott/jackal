---
layout: post
title:  "Push Jekyll to Github pages"
date:   2019-10-15 10:10:34 -0500
categories: jekyll deploy github
---
Create an empty repository in GitHub (make sure github pages is enabled in settings).

Duplicate \_config.yml and rename \_config_dev.yml.

Leave \_config_dev.yml as is, and change \_config.yml for the live site.

```yaml
baseurl: "/startjekyll"
url: "https://tpatrickmcdermott.github.io"
```

To run the site locally, run:

```
  jekyll serve --config _config.yml,_config_dev.yml
```

### Push to Github

Add the repository
```
  git remote add origin https://github.com/tpatrickmcdermott/jackal.git
```

Ensures that you're on the gh-pages branch, not master.
```
  git checkout -b gh-pages
```

track all  files
```
  git add .
```

commit all files
```
  git commit -am "Initial commit"
```

Push all files to gh-branch
```
  git push origin gh-pages
```
