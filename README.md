# Markdown Browser Preview

Preview Markdown in the browser with the shortcut <kbd>⌘R</kbd>.

This bundle depends on two variables:

  - `TM_MARKDOWN`

    It must be set to a pipeline accepting a file as stdin and printing
    valid HTML on stdout. Examples:

        /usr/bin/markdown
        /usr/local/bin/cmark --smart
        /Users/Johnny/bin/pandoc --from markdown_strict
        /usr/bin/smartypants | /usr/bin/markdown  # this works, too

  - `TM_BROWSER`

    If set, it’s assumed to contain either the name or the path of a browser’s
    application bundle (.app) — basically, anything accepted by `open -a`.
    Examples:

        Safari
        Firefox
        Google Chrome
        /Applications/Safari
        /Applications/Safari.app
        /Users/Johnny/MyApps/Google Chrome

Variables can be set:

1.  from the Variables tab in TextMate’s preferences,
2.  in a `.tm_properties` file, or
3.  in this bundle’s settings (as name–value entries in `shellVariables`).

### But…

This bundle works {best,only} with Safari. Safari doesn’t open a file twice, it
simply reloads the page. Other browsers don’t. And there’s nothing I
{can,want to} do about it.
