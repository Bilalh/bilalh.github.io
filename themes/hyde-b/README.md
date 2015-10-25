Hyde-B
======

## Install

```
$ cd your_hugo_site/
$ mkdir themes
$ cd themes
$ git clone https://github.com/bilalh/hyde-b
```

See the [official Hugo themes documentation](http://gohugo.io/themes/installing) for more info.

Forked from [Hyde-Y](https://github.com/enten/hyde-y)

## Usage

The theme expects the following layout:

```
.
└── content
    ├── posts
    |   ├── post1.md
    |   └── post2.md
    ├── code
    |   ├── project1.md
    |   ├── project2.md
    ├── license.md        // this is used in the sidebar footer link
    └── other_page.md
```

Run `hugo --theme=hyde-b` to generate.

## Configuration

## Tips

* If you've added `theme = "hyde-b"` to your `config.toml`, you don't need to keep using the `--theme=hyde-y` flag!
* Although all of the syntax highlight CSS files under the theme's `static/css/highlight` are bundled with the site, only the one you choose will be included in the page and delivered to the browser.
* Change the favicon by providing your own as `static/favicon.png` (and `static/touch-icon-144-precomposed.png` for Apple devices) in your site directory.
* Hugo makes it easy to override theme layout and behaviour, read about it [here](http://gohugo.io/themes/customizing).
* Pagination is set to 10 items by default, change it by updating `paginate = 10` in your `config.toml`.


## Attribution

Base off the [Hyde-Y](https://github.com/enten/hyde-y) theme, which was based off [Hyde-X](https://github.com/zyro/hyde-x) &  [Hyde](https://github.com/poole/hyde).

## Questions, ideas, bugs, pull requests?

All feedback is welcome! Head over to the [issue tracker](https://github.com/bilalh/hyde-b/issues).

## License

Open sourced under the [MIT license](https://github.com/bilalh/hyde-b/blob/master/LICENSE).
