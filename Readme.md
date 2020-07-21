# Pelican-Attila-X
This is a modified version of the [Pelican](https://github.com/getpelican/pelican) [attila](https://github.com/arulrajnet/attila) theme by Arulraj V. [Original theme](https://github.com/zutrinken/attila) is made for the Ghost blogging platform by Peter Amende.

## Demo
* [My website](https://vimaltech.com)
* [Skyrocket](https://skyrocket.vimaltech.com) — template based on this theme


## Features
- Responsive
- Automatic **dark mode**
- Detailed information in **author profiles** including links to social media accounts
- **Social media integration** — support for Twitter, Facebook, GitHub, GitLab and Mastodon links in author profile and navigation
- **Cover image** support for home page, article, page and templates
- Can be configured to support **comments**, **email newsletter** and a **contact form**
- **Syntax highlight** for code samples
- **Next** and **Previous** posts beneath blog posts (requires the neighbors plugin)

## Installation
1. Unzip theme
2. Update `pelicanconf.py`:
   
       THEME = 'themes/pelican-attila-x'
       
## Configuration
The following settings can be added to **pelicanconf.py** in addition to the ones supported by Pelican (`SITENAME`, `SITEURL`, `AUTHOR` etc.,)

### SITE_LOGO
`string`

Path to website's logo relative to the `content` directory, for example `images/logo.svg`.

### AUTHORS
`dict`

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

### SOCIAL
`tuple` of tuples

Links to social media accounts for this website:

```python
SOCIAL = (
    ('Twitter', 'https://twitter.com/'),
    ('Facebook', 'https://facebook.com/'),
    ('Mastodon', 'https://linuxrocks.online/')
)
```

### MENUITEMS
`tuple` of tuples

Links to appear in site navigation:

```python
MENUITEMS = (
    ('Home', '/'),
    ('About', '/about'),
)
```

**Note:** If `FORMSPREE_ID` is set, a contact page is automatically added to site navigation.

### COVER_IMAGES
`dict`

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

### COLORS
Use an alternate color scheme. `primary` is used for links and `primary-active` is used for link hover state.

```
COLORS = {
    'primary': '#e63946',
    'primary-active': '#457b9d' 
}
```

### FONTS
`dict`

Use Google fonts 

**Note: This needs more testing**

Theme includes (and uses) these fonts by default:
* Lato (for headings)
* Merriweather (for text)
* Inconsolata (for code)

If you prefer to use alternative fonts, you can set them here:

```
FONTS = {
    'sans': 'Roboto',
    'serif': 'Lora'
}
```

---

> The following settings can be added to **publishconf.py**

---
### DISQUS_SITENAME
If you wish to use Disqus comments, uncomment and set this value to your site name

```
#DISQUS_SITENAME = ''
```

### ENABLE_COMMENTO
Alternatively, if you use commento for comments, uncomment this setting

```
#ENABLE_COMMENTO = True
```

### GOOGLE_ANALYTICS
If you wish to use Google Analytics, uncomment and set this value to your Google analytics ID i.e., UA-XXXXXXX

```
#GOOGLE_ANALYTICS = 'UA-XXXXXX'
```

### FORMSPREE_ID
To enable contact form, uncomment and set this value to your Formspree form ID

```
#FORMSPREE_ID = 'abcdefg'
```

### MAILCHIMP_URL, MAILCHIMP_USER and MAILCHIMP_FORM_ID
To enable users to subscribe to your blog using Mailchimp, uncomment this block and set `MAILCHIMP_URL` to the URL corresponding to your signup form. If you get errors while parsing `MAILCHIMP_USER` and `MAILCHIMP_FORM_ID`, please set
these variables manually.

```
## START MAILCHIMP BLOCK
#
#MAILCHIMP_URL = 'https://example.us4.list-manage.com/subscribe/post?u=1234567893d86023b9abcd&amp;id=6185580190'
#
#m = re.match('^https.+u=([0-9a-z]+)&amp;id=(\d+)$', MAILCHIMP_URL)
## User is the string after u= i.e., 1234567893d86023b9abcd in this example
#MAILCHIMP_USER = m.groups(0)[0]
#
##Form ID is the string after id= i.e., 6185580190 in this example
#MAILCHIMP_FORM_ID = m.groups(0)[1]
#
## END MAILCHIMP BLOCK
```

## Support Development
If you would like to support development of this theme, you can consider purchasing [Skyrocket](https://gumroad.com/l/pelican-skyrocket) — a ready to use template for a Pelican based website with added features and sample content.

## License
MIT

