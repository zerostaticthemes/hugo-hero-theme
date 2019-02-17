# Hugo Hero Theme

Hero is a multipurpose theme with fullscreen hero images and fullwidth sections. It contains content types for a business or portfolio site.

[Live Demo](https://hugo-hero.netlify.com/) |
[Zerostatic Themes](https://www.zerostatic.io/theme/hugo-hero/)

![Hugo Hero Theme screenshot](https://github.com/JugglerX/hugo-hero-theme/blob/master/images/screenshot-full.jpg)

## Theme features

### Content Types

- Services (Markdown)
- Work/Portfolio (Markdown)
- Features (Data)
- About (Single Page)
- Homepage (Single Page)

### Content Management
- This themes content is now all editable via markdown files.
- The "Home" page uses multiple markdown files for the different homepage sections. It uses **headless bundles**.
- The "About Us" page uses multiple markdown files for its different sections. It uses **leaf bundles** and **shortcodes**.
- "Services" & "Work" use markdown files with list, single and summary views.

### Features

- Full-width responsive design
- Full-width/full-height hero image partial. Partial arguments include background-image, no background-image, background-image with overlay or just a solid color background.

### SCSS

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

# Installation

To use this theme you will need to have Hugo installed. If you don't already have Hugo installed please follow the official [installation guide](https://gohugo.io/getting-started/installing/)

### Check Hugo Version

This theme uses [Hugo Pipes](https://gohugo.io/hugo-pipes/scss-sass/) to compile SCSS and minify assets. Please make sure you have the `Hugo Extended` version installed. If you are not using the extended version this theme will not not compile.

```
hugo version
```

### Create a new Hugo site

```
hugo new site mynewsite
```

This will create a fresh Hugo site in the folder `mynewsite`. 

### Install theme

Copy or git clone this theme into the sites themes folder `mynewsite/themes`

#### Install with Git

```
cd mynewsite
git clone https://github.com/jugglerx/hugo-hero-theme.git themes/hugo-hero-theme
```

#### Install from .zip file

You can download the .zip file located here https://github.com/JugglerX/hugo-hero-theme/archive/master.zip.

Extract the downloaded  .zip inside the `themes` folder. Rename the extracted folder from `hugo-hero-theme-master` -> `hugo-hero-theme`. You should end up with the following folder structure `mynewsite/themes/hugo-hero-theme`

### Add example content

Copy the entire contents of the `mynewsite/themes/hugo-hero-theme/exampleSite/` folder to root folder of your Hugo site, ie `mynewsite/`

To copy the files using terminal, make sure you are still in the projects root, ie the `mynewsite` folder.

```
cp -a themes/hugo-hero-theme/exampleSite/. .
```

### Update config.toml

After you copy the `config.toml` into the root folder of your Hugo site you will need to update the `baseURL`, `themesDir` and `theme` values in  `mynewsite/config.toml`

```
baseURL = "/"
themesDir = "themes"
theme = "hugo-hero-theme"
```

### Run Hugo

After installing the theme for the first time, generate the Hugo site.

You run this command from the root folder of your Hugo site ie `mynewsite/`

```
hugo
```

For local development run Hugo's built-in local server.

```
hugo server
```

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.


# Configuring theme features

### Homepage meta tags

Often a homepage requires special meta tags such as a meta description or og meta data for twitter, facebook etc. You can configure these values in the `config.toml`

```
// config.toml
[params]
  google_analytics_id=""

  [params.homepage_meta_tags]
    meta_description = "a description of your website."
    meta_og_title = "My Theme"
    meta_og_type = "website"
    meta_og_url = "https://www.mywebsite.com"
    meta_og_image = "https://www.mywebsite.com/images/tn.png"
    meta_og_description = "a description of your website."
    meta_twitter_card = "summary"
    meta_twitter_site = "@mytwitterhandle"
    meta_twitter_creator = "@mytwitterhandle"
```

### Set meta tags on a per template/page basis

You can set meta tags on a per template basis using a block. For example, you might want to write a custom meta description for the `/services` page. You can insert any valid HTML meta data inside the `{{ define "meta_tags }}` block at the top of a template.

```
// layouts/services/list.html
...

{{ define "meta_tags" }}
    <meta name="description" content="We offer a variety of services in the finance industry" />
{{ end }}

{{ define main }}
...
```

# Deploying to Netlify

This theme includes a `netlify.toml` which is configured to deploy to Netlify from the `exampleSite` folder.  See this discussion on how to deploy your site on Netlify from the `exampleSite` folder - https://discourse.gohugo.io/t/deploy-your-theme-to-netlify/15508

Most likely if you are deploying to Netlify, you are including the entire Hugo site, so you can delete the `netlify.toml` file.



