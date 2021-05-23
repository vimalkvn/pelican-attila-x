# Attila-X — theme for Pelican

**Warning:** Theme is being modified heavily at present. 
Things might break. This documentation is also out of date.

---

This is a modified version of the [Pelican](https://github.com/getpelican/pelican) [attila](https://github.com/arulrajnet/attila) theme by Arulraj V. [Original theme](https://github.com/zutrinken/attila) is made for the Ghost blogging platform by Peter Amende.

[Live Demo](https://vimalkvn.com)

## Features
- Responsive
- Automatic **dark mode**
- Detailed information in **author profiles** including links to social media accounts
- **Social media integration** — support for Twitter, Facebook, GitHub, GitLab and Mastodon links in author profile and navigation
- **Cover image** support for home page, article, page and templates
- Can be configured to support **comments** — currently supports Commento
- **Syntax highlight** for code samples
- **Next** and **Previous** posts beneath blog posts (requires the neighbors plugin)

## Installation
1. Unzip theme
2. Update `pelicanconf.py`:
   
       THEME = 'themes/pelican-attila-x'
       
## Configuration
The following settings can be added to **pelicanconf.py** in addition to the ones supported by Pelican (`SITENAME`, `SITEURL`, `AUTHOR` etc.,)

### SITE_LOGO `string`

Path to website's logo relative to the `content` directory, for example `images/logo.svg`.

### AUTHORS `dict`

Metadata for authors. At a minimum, there should be a single entry corresponding to the website's `AUTHOR`, for example:

```python
AUTHOR = 'Astro'

AUTHORS = {
  'Astro' : {
    'avatar': 'images/author_profile.svg',
    'website': 'https://example.com',
    'location': 'World',
    'bio': 'Astronaut · Writer',
    'twitter': 'https://twitter.com',
    'facebook': 'https://facebook.com',
    'github': 'https://github.com',
    'gitlab': 'https://gitlab.com',
    'mastodon': 'https://mastodon.social/',
    'cover_image': 'images/author.svg'
  }
}
```

### SOCIAL `tuple` of tuples

Links to social media accounts for this website:

```python
SOCIAL = (
    ('Twitter', 'https://twitter.com/'),
    ('Facebook', 'https://facebook.com/'),
    ('Mastodon', 'https://linuxrocks.online/')
)
```

### MENUITEMS `tuple` of tuples

Links to appear in site navigation:

```python
MENUITEMS = (
    ('Home', '/'),
    ('About', '/about'),
)
```

### COVER_IMAGES `dict`

Cover images to use in template pages. Keys correspond to template names.

```python
COVER_IMAGES = {
    'index': 'images/rocket.svg',
    'authors': 'images/authors.svg',
    'archives': 'images/archives.svg',
    'categories': 'images/categories.svg',
    'period_archives': 'images/period_archives.svg',
    'tags': 'images/tags.svg',
    'category': {
        'blogging': 'images/blogging.svg'
        },
    'tag': {
        'pelican': 'images/blogging.svg'
    },
}
```

### COLORS `dict`
Use an alternate color for links:

```python
COLORS = {
    'primary': '#e63946',
}
```

---

> The following settings can be added to **publishconf.py**

---
### ENABLE_COMMENTO `boolean`
If you use [Commento](https://commento.io/) for comments, uncomment this setting

```python
#ENABLE_COMMENTO = True
```

## Support Development
If you would like to support development of this theme, you can consider making a donation on
[Paypal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=NS4HREAWJGFDC&source=url)

## License
MIT

