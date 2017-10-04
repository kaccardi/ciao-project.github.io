# Contributing to ciao-project.github.io

This repository contains the source code for the ciao-project.github.io web
site.  The source code is composed of two separate entities; a Jekyll theme,
[Jekyll Documentation
Theme](http://idratherbewriting.com/documentation-theme-jekyll/index.html) that
provides the look and feel of the website in addition to the code that manages
things like the table of contents, blogs, etc, and the textual content of the
web-site that describes the Cloud Integrated Advanced Orchestrator project.  An
attempt has been made to try to keep the textual and theme content separate.
The webpages displayed on the site are generated from markdown (actually
[krampdown](http://idratherbewriting.com/2016/02/21/bug-with-kramdown-and-rouge-with-github-pages/))
files, all of which are stored in the top level
[ciao](https://github.com/ciao-project/ciao-project.github.io/tree/master/ciao)
directory.

## Updating an existing web page

The webpages you see on ciao-project.github.io are generated on the fly by
github pages when a new commit is pushed to this repository.  HTML content is
generated by applying the [Jekyll Documentation
Theme](http://idratherbewriting.com/documentation-theme-jekyll/index.html) to
the markdown files in the
[ciao](https://github.com/ciao-project/ciao-project.github.io/tree/master/ciao)
directory.  This is nice as it means that the webpage can be updated by simply
modifying a markdown file and pushing the change to the repository.

It is possible to run the [Jekyll Documentation
Theme](http://idratherbewriting.com/documentation-theme-jekyll/index.html)
locally on your machine before submitting a pull request.  The site content and
theme can be compiled to HTML, stored in the _site folder and served up by a
web server bound to localhost.  You'll be able to view your changes by pointing
your browser at the reported URL.  See [Getting started with the Documentation
Theme for
Jekyll](http://idratherbewriting.com/documentation-theme-jekyll/index.html) for
more details.

## Adding a new web page

There are three steps involved here.

1. Create a new markdown file in the appropriate directory under the
[ciao](https://github.com/ciao-project/ciao-project.github.io/tree/master/ciao)
directory.  Note the directory hierarchy used in the ciao folder is chosen to
mirror the organisation of the web site presented by the sidebar.  This
hierarchy is not reflected in the source code of the final generated web site.
When jekyll generates the HTML pages it places them all in the root directory of
the website.

2. Add the
[frontmatter](http://idratherbewriting.com/documentation-theme-jekyll/mydoc_pages.html#frontmatter)
to the markdown file.  If you do not do this your markdown file will not be
converted to HTML.

3. Update the
[sidebar](https://github.com/ciao-project/ciao-project.github.io/blob/master/_data/sidebars/home_sidebar.yml)

## Sending Pull Requests

Fork the repository, create a new branch, push the changes to the branch in your
fork and send a pull request.

In order to get a clear contribution chain of trust we use the [signed-off-by
language] (https://01.org/community/signed-process) used by the Linux kernel
project.

## Patch format

Beside the signed-off-by footer, we expect each patch to comply with the following format:

```
<component>: Change summary

More detailed explanation of your changes: Why and how.
Wrap it to 72 characters.
See [here] (http://chris.beams.io/posts/git-commit/)
for some more good advice.

Fixes: <URL to bug fix if appropriate>

Signed-off-by: <contributor@foo.com>
```

For example:

```
Remove references to 01org
    
A number of places in the documentation used out of date
URLs and package names for ciao components.  This commit fixes
the issue, by replacing 01org, with ciao-project.
    
Fixes: https://github.com/ciao-project/ciao-project.github.io/issues/2
    
Signed-off-by: Mark Ryan <mark.d.ryan@intel.com>
```



