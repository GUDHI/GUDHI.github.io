# GUDHI website

GUDHI website is a fork of <http://phlow.github.io/feeling-responsive/>.

To get to know *Feeling Responsive* check out all the features explained in the [documentation](http://phlow.github.io/feeling-responsive/documentation/).

And what license is *Feeling Responsive* released under? [This one](https://github.com/Phlow/feeling-responsive/blob/gh-pages/LICENSE)).

## Gitlab
To modify the web site, an Inria gitlab account is required. If you are not familiar with Git, please follow this [mini-tutorial](http://rogerdudler.github.io/git-guide/).

To 'compile' the web site, [Jekyll](https://jekyllrb.com/docs/installation/) is required.

In a command line :
```bash
   jekyll serve
```

And the web site is constructed under `_site` generated directory.

The web site is reconstructed on the fly when you modify pages (mostly `.md` files - for MarkDown) while jekyll serve is running.
And you can your modification on the web page [http://127.0.0.1:4000/](http://127.0.0.1:4000/).

If you want the specific developper configuration:
```bash
   jekyll serve --config _config_dev.yml
```

### Gitlab-CI

Gitlab-CI pipelines are also configured to test your website modifications.
The result is on page https://gudhi.gitlabpages.inria.fr/gudhi-website/

## Jekyll installation
To install Jekyll on Ubuntu : <http://michaelchelen.net/81fa/install-jekyll-2-ubuntu-14-04/>

## Utilities page
This page is generated from the version with the following command :
```bash
rm utilities.md; find . -type f -name README | grep utilities | sort | xargs cat -- >> utilities.md
```
