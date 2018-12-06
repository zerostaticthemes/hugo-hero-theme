# Hugo Hero Theme

Hero is a multipurpose business theme with bold clean lines, fullscreen images and fullwidth sections. It contains content types and functionality for a archetypical small business.

[Live Demo](https://hugo-hero.netlify.com/)

![Hugo Hero Theme screenshot](https://github.com/JugglerX/hugo-hero-theme/blob/master/images/screenshot-with-border.png)

## Theme features

- Fullscreen and fixed height hero image partials that use paramaters
- Services (Content Type)
- Work (Content Type)
- Masonry style gallery on Work single pages
- Features (Data)
- About (Single Page)
- SCSS (Hugo Pipelines)
- Responsive design
- Bootstrap 4 grid and media queries only
- Responsive menu managed in `config.toml`
- 100/100 Google Lighthouse speed score
- Under 30KB without images or 80KB with images and illustrations ⚡
- Robust example content included
- Royalty free images included (Unsplash)

## Installation

Inside the folder of your Hugo site run:

    $ cd themes
    $ git clone https://github.com/jugglerx/hugo-hero-theme.git

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.

## Getting started

After installing the Hero theme successfully it requires a just a few more steps to get your site finally running.

### Adding example content

The fastest way to get started is to copy the example content. Copy the contents of the `exampleSite` folder to the root folder of your Hugo site. This theme comes with content for the following content types: `services` and `work`. The `about` us page is a single page with alternating fullwidth sections. It includes JSON data for `features` and `contact`. It also includes the `config.toml` file which has an example menu.

### Edit config

After you copy the `config.toml` into the root folder of your Hugo site you will need to update the `baseURL`

```
baseURL = "/"
```

## Running Hugo

After installing the theme, generate the Hugo site.

```
hugo
```

Hugo's built-in local server.

```
hugo server
```

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.
