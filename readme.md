# Qute Start

A bare bones home page/new tab page that is friendly to light or dark modes.

Made for personal use and sharing across my own computers.

Developed primarily for use with [qutebrowser](https://qutebrowser.org/) but has been tested with Chrome and Firefox where it has also worked fine.

## Features

- Minimal text-based interface
- Live-editable text (_mostly_)
- Buttons to add new notes and tasks
- Quote, links, tasks and favourites sections as default

## Purpose

I wanted a simple, minimal homepage that opens quickly, shows some links and includes a few live-editable notes.

I also wanted to move away from home page extensions that seem to be dominated by large clocks and landscape photography.

## Using

To start `git clone` the repo and note the _path_ to the `index.html`.
In your `config.py` for qutebrowser include the following lines:

```
c.url.default_page = 'file:///home/user/yourpathto/qute-start/index.html'
c.url.start_pages = 'file:///home/user/yourpathto/qute-start/index.html'
```

*Note: it should be possible to do something very similar on other browsers but I have not checked in detail.*

The `index.html` is **my** homepage and you will want to customise it.
Currently, almost all text can be edited in the browser **except for links**.
When you edit a text element and re-focus on another (or click elsewhere) the current state of the page will be saved to _local storage_.
Standard shortcuts for copying/pasting, bolding/italicising, etc., should work as normal.

Buttons are included at the end of the *tasks*, *notes* and *favourites* sections.
Clicking these buttons will add a correctly formatted element that you can edit.
(You can also simply copy-paste elements if you wish.)
Again, you must defocus from any changed element for the changes to persist.

*Note: if you want to use keyboard shortcuts on the homepage (e.g., H, J, K, L movement keys in qutebrowser) you must ensure you are not focused on an editable text element.*

You will probably want to create your own page from scratch, however.
If so, delete mine and rename `template.html` to `index.html`.
This will give you a skeleton startpage with placeholder text.
Edit the new `index.html` to add different links, styles, etc.

## Warning

I wouldn't advise relying on local storage for highly sensitive notes.

For security, it might be preferable to `save as` the webpage periodically and replace the `index.html` to make the changes permanent.

~~In qutebrowser you can type `gd` to invoke the *download* command with the homepage open in the active tab.~~
~~A prompt will then ask you to find where you want to download the `index.html`.
Choose the `/qute-start/` directory and save over the original file.~~

**I'm not sure yet if this preserves local changes** and the functionality might be incorporated as a button in the future if it doesn't clutter the page.

## Limitations

Pull requests welcome.

### Live-editable links

Would be nice to have editable links but this needs to be done in such a way that the hyperlinks remain clickable.
Should not be too difficult but is not a priority right now.

## Credit

The `html` and `css` is inspired by the lovely [Pico-8 online manual](https://www.lexaloffle.com/dl/docs/pico-8_manual.html).

## Images

### Dark mode on qutebrowser

Shown with **darkmode** enabled in browser, **transparent** terminal and **default** text. 

![Dark mode on qutebrowser](dark_qute.png) 

### Light mode on Firefox

Shown with **lightmode** enabled in browser and **edited text** (title, tasks) that are **saved locally**.

![Light mode on firefox](light_firefox.png) 

## To-do

- [ ] Add instructions for setting defaults in different browsers
- [ ] Test download page functionality
- [ ] Add rich text support
- [ ] Theme support
- [ ] Updated images to capture latest changes
- [ ] Consider a readme .gif
