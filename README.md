# shared-hugo-theme

This is a child theme for [Hugo Simple](https://github.com/maolonglong/hugo-simple) that includes customizations and shared components we reuse for some of our various Hugo projects.

It requires Hugo Simple as a base theme, as this isn't a full theme in itself.

## Installation

This assumes you already have Hugo and Hugo Simple installed in an existing Hugo site, and that you want to use git submodules to manage your themes.

1. Navigate to the base of your git repo
2. Run the following command to add this theme as a submodule:

   ```
   git submodule add -b https://github.com/PossumNet/shared-hugo-theme.git your-website/themes/shared-hugo-theme
   ```
3. Add the shared theme to your hugo.toml file:

   ```toml
   theme = ["shared-hugo-theme", "hugo-simple"]
   ```

### Updating git submodules

To update the submodules, run:

```
git submodule update --remote --recursive
```

## What it includes

This adds the following to Hugo Simple:
- A css file named `css_vars.css` that can be used to define CSS variables for colors, fonts, etc.
- A blank css file named `custom.css` that can be used to add custom CSS rules and is included in new pages by default.
- Shortcode for contact email address pulled from hugo.toml
- Shortcode for latest post
- Render images as 800x800 by default
- Default privacy policy page
- Footer includes links to privacy policy and contact email
- Enable mathjax support
- Add content div tag for easier styling
- Add author and date to single and list pages
- Add summary to list pages

## Customizing and Using

### css

Copy `css_vars.css` and `custom.css` to your own assets directory.

#### css_vars.css

css_vars.css is where you can define CSS variables for colors, fonts, etc. that will be used throughout the site. 
These variables are loaded simple.css and style.css which are part of the Hugo Simple theme, and therefore will override their styles.

#### custom.css

custom.css is where you can add your own custom CSS rules for page level customizations. 
This file is included in the frontmatter of new pages by default.
