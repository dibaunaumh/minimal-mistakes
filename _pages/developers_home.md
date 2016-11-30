---
title: "Developers - Web Wide Matrix"
layout: single
permalink: /developers
date: 2016-11-28T06:00:00-00:00
sidebar:
  - title: "Github project"
    text: "More text here."
    absolute_url: "http://github.com/dibaunaumh/fcs-skateboard"
  - title: "Roadmap"
    text: "More text here."
  - title: "Join the team"
    text: "More text here."
---

Minimal Mistakes has been developed as a [Jekyll theme gem](http://jekyllrb.com/docs/themes/) for easier use. It is also 100% compatible with GitHub Pages --- just with a more involved installation process.

{% include toc %}

## Welcome

If you're running Jekyll v3.3+ and self-hosting you can quickly install the theme as Ruby gem.
If you're hosting with GitHub Pages you'll have to use the old "repo fork" method or directly copy all of the theme files[^structure] into your site.


[^structure]: See [**Structure** page]({{ "/docs/structure/" | absolute_url }}) for a list of theme files and what they do.

**ProTip:** Be sure to remove `/docs` and `/test` if you forked Minimal Mistakes. These folders contain documentation and test pages for the theme and you probably don't littering up in your repo.
{: .notice--info}

### Roadmap

<figure>
  <img src="{{ '/assets/images/roadmap.png' | absolute_url }}" alt="fork Minimal Mistakes">
</figure>

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "minimal-mistakes-jekyll"
```

Add this line to your Jekyll site's `_config.yml` file:

```yaml
theme: minimal-mistakes-jekyll
```

Then run Bundler to install the theme gem and dependencies:

```bash
bundle install
```

### How does it work?

{% include youtube.html id="1T1sHIlxK-w" %}



Fork the [Minimal Mistakes theme](https://github.com/mmistakes/minimal-mistakes/fork), then rename the repo to **USERNAME.github.io** --- replacing **USERNAME** with your GitHub username.


**Note:** Your Jekyll site should be viewable immediately at <http://USERNAME.github.io>. If it's not, you can force a rebuild by **Customizing Your Site** (see below for more details).
{: .notice--warning}

If you're hosting several Jekyll based sites under the same GitHub username you will have to use Project Pages instead of User Pages. Essentially you rename the repo to something other than **USERNAME.github.io** and create a `gh-pages` branch off of `master`. For more details on how to set things up check [GitHub's documentation](https://help.github.com/articles/user-organization-and-project-pages/).

<figure>
  <img src="{{ '/assets/images/mm-gh-pages.gif' | absolute_url }}" alt="creating a new branch on GitHub">
</figure>

Replace the contents of `Gemfile` found in the root of your Jekyll site with the following:

```ruby
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
  gem "jemoji"
end
```

Then run `bundle update` and verify that all gems install properly.

### The architecture

{% include youtube.html id="Ly75njf0drk" %}

If you forked or downloaded the `minimal-mistakes-jekyll` repo you can safely remove the following folders and files:

- `.editorconfig`
- `.gitattributes`
- `.github`
- `/docs`
- `/test`
- `CHANGELOG.md`
- `minimal-mistakes-jekyll.gemspec`
- `README.md`
- `screenshot-layouts.png`
- `screenshot.png`

## The team

Depending on the path you took installing Minimal Mistakes you'll setup things a little differently.

### Organization structure

Starting with an empty folder and `Gemfile` you'll need to copy or re-create this [default `_config.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_config.yml) file. For a full explanation of every setting be sure to read the [**Configuration**]({{ "/docs/configuration/" | absolute_url }}) section.

After taking care of Jekyll's configuration file, you'll need to create and edit the following data files.

- [`_data/ui-text.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_data/ui-text.yml) - UI text [documentation]({{ "/docs/ui-text/" | absolute_url }})
- [`_data/navigation.yml`](https://github.com/mmistakes/minimal-mistakes/blob/master/_data/navigation.yml) - navigation [documentation]({{ "/docs/navigation/" | absolute_url }})

### Join us

Scaffolding out a site with the `jekyll new` command requires you to modify a few files that it creates.

Edit `_config.yml` and create `_data/ui-text.yml` and `_data/navigation.yml` same as above. Then:

- Replace `<site root>/index.md` with a modified [Minimal Mistakes `index.html`](https://github.com/mmistakes/minimal-mistakes/blob/master/index.html). Be sure to enable pagination if using the [`home` layout]({{ "/docs/layouts/#home-page" | absolute_url }}) by adding the necessary lines to **_config.yml**.
- Change `layout: post` in `_posts/0000-00-00-welcome-to-jekyll.markdown` to `layout: single`.
- Remove `about.md`, or at the very least change `layout: page` to `layout: single` and remove references to `icon-github.html` (or [copy to your `_includes`](https://github.com/jekyll/minima/tree/master/_includes) if using it).


---

That's it! If all goes well running `bundle exec jekyll serve` should spin-up your site.