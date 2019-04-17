# Hugo Hero Theme

Hero is a multi-page, multi-purpose theme with fullscreen hero images and fullwidth sections.

[Live Demo](https://hugo-hero.netlify.com/) |
[Zerostatic Themes](https://www.zerostatic.io/theme/hugo-hero/)

![Hugo Hero Theme screenshot](https://github.com/JugglerX/hugo-hero-theme/blob/master/images/screenshot-full.jpg)

## Theme features

### Content Types

- Services (Markdown)
- Work/Portfolio (Markdown)
- Features (Data)
- About (Markdown, Single Page, Shortcodes)
- Homepage (Markdown, Single Page, multiple .md files in one layout)

### Content Management

- This themes content is now all editable via markdown files.
- Includes examples where multiple .md files are sourced in a single layout to create fullwidth sections that have different locations in the HTML.
- The "Home" page uses multiple markdown files for the different homepage sections. It uses **headless bundles**.
- The "About Us" page uses multiple markdown files for its different sections. It uses **leaf bundles** and **shortcodes**.
- "Services" & "Work" use markdown files with layouts for list, single and summary views.

### Features

- Full-width responsive design
- Full-width/full-height hero image partial. Partial arguments include background-image, no background-image, background-image with overlay or just a solid color background.

### SCSS

- SCSS (Hugo Pipelines)
- Responsive design
- Bootstrap 4 grid and media queries
- The rest of the Bootstrap library is commented out by default but is ready to be @imported in the `style.scss`

### Speed

- 100/100 Google Lighthouse speed score
- Vanilla JS only
- Minified CSS under 20KB
- Minified JS under 20KB

### Menu

- Responsive mobile menu managed in `config.toml`

### Content

- Robust example content included
- Royalty free images included

# Install Hugo

To use this theme you will need to have Hugo installed. If you don't already have Hugo installed please follow the official [installation guide](https://gohugo.io/getting-started/installing/)

### Check Hugo version (Hugo 0.51+ Extended is required)

This theme uses [Hugo Pipes](https://gohugo.io/hugo-pipes/scss-sass/) to compile SCSS and minify assets. Please make sure you have the **Hugo Extended** version installed. If you are not using the extended version this theme will not not compile.

To check your version of Hugo, run:

```
hugo version
```

This will output the currently installed version of Hugo. Make sure you see `/extended` after the version number, for example `Hugo Static Site Generator v0.51/extended darwin/amd64 BuildDate: unknown` You do not need to use version v0.51 specifically, you can use any version of Hugo above 0.51. It just needs to have the `/extended` part

### Create a new Hugo site

```
hugo new site mynewsite
```

This will create a fresh Hugo site in the folder `mynewsite`.

# Install Theme

You may download and extract this theme or git clone this theme into the sites themes folder `mynewsite/themes`

#### Install with Git

```
cd mynewsite
git clone https://github.com/jugglerx/hugo-hero-theme.git themes/hugo-hero-theme
```

#### Install from .zip file

You can download the .zip file located here https://github.com/JugglerX/hugo-hero-theme/archive/master.zip.

Extract the downloaded .zip inside the `themes` folder. Rename the extracted folder from `hugo-hero-theme-master` -> `hugo-hero-theme`. You should end up with the following folder structure `mynewsite/themes/hugo-hero-theme`

### Update example content

Copy the entire contents of the `mynewsite/themes/hugo-hero-theme/exampleSite/` folder to root folder of your Hugo site, ie `mynewsite/`

To copy the files using terminal, make sure you are still in the projects root, ie the `mynewsite` folder.

```
cp -a themes/hugo-hero-theme/exampleSite/. .
```

### Update config.toml

After you copy the `config.toml` into the root folder of your Hugo site you will need to update the `baseURL`, `themesDir` and `theme` values in `mynewsite/config.toml`

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

# Configuring Theme

### Homepage meta tags

Often a homepage requires special meta tags such as a meta description or og meta data for twitter, facebook etc. You can configure these values in the `config.toml`

```
// config.toml
...

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

### Set meta tags on a per layout basis

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

### Google Analytics

Add you google analytics ID to the `config.toml`

```
// config.toml
[params]
  google_analytics_id="UA-132398315-1"
```

### Menu

You can edit and add main menu links in the `config.toml` under `[[menu.main]]`

# Deploying to Netlify

This theme includes a `netlify.toml` which is configured to deploy to Netlify from the `exampleSite` folder. See this discussion on how to deploy your site on Netlify from the `exampleSite` folder - https://discourse.gohugo.io/t/deploy-your-theme-to-netlify/15508

Most likely if you are deploying to Netlify and created a new Hugo site or added this theme to an existing Hugo site then you are not deploying from the `exampleSite` directory and you can delete the `netlify.toml` file.
