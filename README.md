# Hugo Hero Theme

Hero is a multipurpose theme with fullscreen hero images and fullwidth sections. It contains content types for a business or portfolio site.

[Live Demo](https://hugo-hero.netlify.com/)

![Hugo Hero Theme screenshot](https://github.com/JugglerX/hugo-hero-theme/blob/master/images/screenshot-with-border.jpg)

## Theme features

### Content Types

- Services (Markdown)
- Work/Portfolio (Markdown)
- Features (Data)
- About (Single Page)

### Features

- Full-width/full-height hero images as a partial. Partial accepts a background-image, no background-image, background-image with blue overlay or just a blue color background.
- Fixed height hero images as a partial
- Full width strips on homepage
- Single 'About' page with alternating full-width sections
- Portfolio pages contain a CSS only masonary image gallery

### CSS

- SCSS (Hugo Pipelines)
- Responsive design
- Bootstrap 4 grid and media queries only

### Speed

- 100/100 Google Lighthouse speed score
- 21KB without images ⚡
- Vanilla JS only

### Menu

- Responsive mobile menu managed in `config.toml`

### Content

- Robust example content included
- Royalty free images included

## Installation

Inside the folder of your Hugo site run:

```
cd themes
git clone https://github.com/jugglerx/hugo-hero-theme.git
```

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.

## Getting started

After installing the Hero theme successfully it requires a just a few more steps to get your site finally running.

### Adding example content

The fastest way to get started is to copy the example content. Copy the contents of the `exampleSite` folder to the root folder of your Hugo site. This theme comes with content for the following content types: `services` and `work`. The `about` us page is a single page with alternating fullwidth sections. It includes JSON data for `features` and `contact`. It also includes the `config.toml` file which has an example menu.

### Edit config

After you copy the `config.toml` into the root folder of your Hugo site you will need to update the `baseURL` and the `themesDir`

```
baseURL = "/"
themesDir = "themes" // you can also remove this line
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
