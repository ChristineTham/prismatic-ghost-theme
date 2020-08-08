# Prismatic

[Ghost](http://ghost.org/) Theme for prismaticpath.com, based on TryGhost/Lyra and TryGhost/London, but with additional animations and styling changes
(from [Reedyn/Saga](https://github.com/Reedyn/Saga)).

A custom, image-centric theme for [Ghost](http://github.com/tryghost/ghost/). Made for publishers and portfolios with plenty of graphics to show off to the world. Completely free and fully responsive, released under the MIT license.

**Demo: https://london.ghost.io**

&nbsp;

![london](https://user-images.githubusercontent.com/120485/50552024-84837400-0c82-11e9-8f1d-cf25962c7e62.jpg)


&nbsp;

# Instructions

1. [Download this theme](https://github.com/ChristineTham/prismatic-ghost-theme/archive/master.zip)
2. Log into Ghost, and go to the `Design` settings area to upload the zip file
3. Unzip the theme archive on your computer and locate the file called `routes.yaml`
4. Inside Ghost admin, go to the `Labs` settings area and scroll down until you see the `Custom Routes` section
5. Upload the `routes.yaml` from this theme

That's it! You now have a Ghost publication which supports free and paid memberships. If you need help, check out the <a href="https://ghost.org/docs/members/">Ghost members documentation</a> or chat with other Ghost users on <a href="https://forum.ghost.org">Ghost forum</a>.

# First time using a Ghost theme?

Ghost uses a simple templating language called [Handlebars](http://handlebarsjs.com/) for its themes.

We've documented our default theme pretty heavily so that it should be fairly easy to work out what's going on just by reading the code and the comments. Once you feel comfortable with how everything works, we also have full [theme API documentation](https://themes.ghost.org) which explains every possible Handlebars helper and template.

**The main files are:**

- `default.hbs` - The main template file
- `index.hbs` - Used for the home page
- `post.hbs` - Used for individual posts
- `page.hbs` - Used for individual pages
- `tag.hbs` - Used for tag archives
- `author.hbs` - Used for author archives

One neat trick is that you can also create custom one-off templates just by adding the slug of a page to a template file. For example:

- `page-about.hbs` - Custom template for the `/about/` page
- `tag-news.hbs` - Custom template for `/tag/news/` archive
- `author-ali.hbs` - Custom template for `/author/ali/` archive


# Development

Styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# Install
yarn

# Run build & watch for changes
$ yarn dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

The `zip` Gulp task packages the theme files into `dist/<theme-name>.zip`, which you can then upload to your site.

```bash
yarn zip
```

# PostCSS Features Used

- Autoprefixer - Don't worry about writing browser prefixes of any kind, it's all done automatically with support for the latest 2 major versions of every browser.
- Variables - Simple pure CSS variables
- [Color Function](https://github.com/postcss/postcss-color-function)


# Copyright & License

Copyright (c) 2013-2020 Hello Tham - Released under the [MIT license](LICENSE).
