# Qute Start

A barebones home page/new tab page for Qutebrowser that is friendly to light or dark modes.

Made for personal use and sharing across my own computers.

## Purpose

I wanted a simple, minimal homepage that opens quickly, shows some links and includes a few notes.

I also wanted to move away from home page extensions that seem to be dominated by large clocks and landscape photography.

## Using

To start `git clone` the repo.
The `index.html` is **my** homepage.
You will probably want to create your own.
If so, delete mine and rename `template.html` to `index.html`.

In your `config.py` for Qutebrowser include the following lines, adding the link to the index.html on your system:

```
c.url.default_page = 'file:///home/user/yourpathto/qute-start/index.html'
c.url.start_pages = 'file:///home/user/yourpathto/qute-start/index.html'
```

Note: a `.woff` file is included in the repo for the default font.

## Limitations

This does **absolutely nothing fancy**.

There are not editable text fields, javascript interactivity or configuration files.

If you want to customise something just change the `.css` and `.html` in the index file. 

You can submit fancy suggestions as pull requests if you like.

## Credit

The `.html` and `.css` is heavily based on the Pico-8 online manual.
