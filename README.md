# Somediceguys Dnd Podcast

[Template link](http://jekyllthemes.org/themes/jekyll-podcaster/)


### Change background color code
change the base color under _sass/base.scss


## Contents

- [Screenshots](#screenshots)
- [Installation](#installation)
- [Customize](#customize)
  - [Basics](#basics)
  - [Links](#links)
  - [Includes](#includes)
  - [Colors](#colors)
  - [Images](#images)
  - [config.yml](#config.yml)
- [Development](#development)
- [Credits](#credits)
- [License](#license)


## Installation

There are four way to use this theme: Netlify, Github Pages, as a gem-based theme and by forking this repo.

### Download the files
You can [download the files](https://github.com/PandaSekh/Jekyll-Podcaster/releases/latest) and add them in your directory to start working.


### Github Pages

Github Pages uses the [--safe flag](https://jekyllrb.com/docs/configuration/options/) to build jekyll websites, which disable custom plugins, caching to disk and ignore symbolic links. Because of that, I suggest you to use any other method. Netlify works great with a 5 minute config, so I suggest you use it.

1. [Fork this repo](https://github.com/PandaSekh/Jekyll-Podcaster/generate).
2. Create a new branch in your repo and call it `gh-pages`.
3. Publish your website and choose gh-pages as the target branch.

### Gem-based theme
1. Add this line to your Jekyll site's `Gemfile`:

    ```ruby
    gem "jekyll-podcaster"
    ```

2. And add this line to your Jekyll site's `_config.yml`:

    ```yaml
    theme: jekyll-podcaster
    ```

3. And then execute:

    ``` bash
    $ bundle
    ```

4. Or install it yourself as:

    ``` bash
    $ gem install jekyll-podcaster
    ```

## Customize
TODO: Explain how to customize theme.

### Basics
In `_data/settings.yml` you can activate Disqus comments by adding your Disqus shortname.
`translate-date` activate translation for the months. If set to true, you can translate months in the file `_includes/date.html`.
If `shownotes` is set to true, every post/episode will include the `_includes/shownotes.html` file. You can use it to add the same text under every post, in case you need to spam your merch store or Patreon, for example.

### Links
In `_data/settings.yml` you can add links next to the Podcast title, social links in the sidebar and links to your podcast.
The social links have a "type" attribute, which defines Font Awesome's font type (fas is solid, fab is brand). Out of the box this theme has support colors for a bunch of social. If your social isn't supported, just add the color in the `sidebar.css`.

### Includes
Modifying file in the `_includes` folder can break things, so please be careful. You should modify only these files:
- `date.html` to translate the website to your language;
- `playerjs.html` if you need to translate the player;
- `shownotes.html` to change your shownotes.

Everything else is modified automatically when you cnage your `settings.yml` and `config.yml` files.

### Colors
You can change colors in the `_sass/base.scss` and `_sass/sidebar.scss` files.
Changing the "wave" colors is a bit harder. You need to decode the svg in the `_scss/background.scss` file, the one in the `background-image` tag. To do that, please refer [to this website](https://mothereff.in/url). Once decoded, change the `path fill` attribute, then encode again and use it.

### Images
You need three different dimensions of your podcast cover for this website:
- Podcast_Cover_500.jpg --> 500x500 pixels
- Podcast_Cover_Small.jpg --> 210x210 pixels
- Podcast_Cover.jpg --> High-Res, I use 3000x3000 pixels

Put those images in the /assets/img/ folder.

### config.yml
It's the usual file in every Jekyll theme. Just compile it. The last part about the podcast metadata is optional, as at the moment this theme won't create a RSS feed. It's just there in case I find the time to add it in the future.


## Development

[Contributions are welcomed and encouraged](https://github.com/PandaSekh/Jekyll-YAMT/issues).

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, `_sass` and `assets` tracked with Git will be bundled.
To add a custom directory to your theme-gem, please edit the regexp in `yamt.gemspec` accordingly.
 
## License
The theme is available as open source under the terms of the [MIT License](https://github.com/PandaSekh/Jekyll-YAMT/blob/master/LICENSE.txt).
TL;DR
Use it for free but keep my name in the footer. Thanks!
