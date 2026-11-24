A minimal Jekyll template using Bootstrap 4 and
Sass. See
<https://www.danielsieger.com/blog/2019/01/12/creating-jekyll-bootstrap-template.html> for details.

## Running locally

The site is published by GitHub Pages as a project site at
<https://jedla22.github.io/rouvycyclingteam.github.io/>, so `_config.yml` sets
`baseurl: "/rouvycyclingteam.github.io"`.

Same paths as production (open http://127.0.0.1:4000/rouvycyclingteam.github.io/):

    bundle exec jekyll serve

At the server root (open http://127.0.0.1:4000/):

    bundle exec jekyll serve --config _config.yml,_config_dev.yml

## Writing links

Never hard-code root paths like `/img/x.png` or `/team.html`: on GitHub Pages they
point outside the site and return 404. Always pass them through `relative_url`:

    <img src="{{ '/img/x.png' | relative_url }}">
    <a href="{{ menu.url | relative_url }}">...</a>

In `css/style.scss` use paths relative to the CSS file, e.g. `url(../img/x.png)`.
