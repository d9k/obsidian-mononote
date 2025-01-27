# Mononote

This plugin ensures each note occupies only one tab. If a note is already open, its existing tab will be focussed instead of opening the same file in the current tab. Works for opening notes via links, menus, hotkeys.


## Scenarios

As an example, assume these open tabs:
- Tab 1 containing Note A
- Tab 2 containing Note B

What's changed:
- In Note B (Tab 2), clicking a link to Note A will focus Tab 1, and Tab 2 will continue to show Note B.
- In Note B (Tab 2), attempting to open a link to Note A in new tab will focus Tab 1, no new tab will be opened.

What's not changed:
- In Note B (Tab 2), clicking a link to Note C: Note C will be opened as usual.
- Tab splitting
- Clicking links in Graph view


## Bug Reports & Discussions

For bug reports please use this repo's Issues section — thank you!

I've moved all plugin **discussions** to the ActionsDotWork Forum which is a hub for both my Obsidian plugins and the macOS/iOS productivity apps I'm building: [Carlo's Obsidian Plugins - ActionsDotWork Forum](https://forum.actions.work/c/obsidian-plugins/8).

The forum supports single-sign-on via GitHub, Apple and Google, meaning you can log in with your GitHub account.


## Known Issues

When a pinned note is focussed, it might be opened again in another tab. For example, if the current daily note is focussed and pinned, using its hotkey will open it in another tab. For some reason, the `onFileOpen` event is not always triggered when a pinned tab is in front. My working theory is that this is a bug in Obsidian; I'll keep an eye on it.


## Installation

**2023-06-09: The plugin is not yet available via Community Notes, so these instructions don't work just yet!**

1. Search for "Mononote" in Obsidian's community plugins browser. ([This link should bring it up.](https://obsidian.md/plugins?id=zottmann))
2. Install it.
3. Enable the plugin in your Obsidian settings under "Community plugins".

That's it.


## Installation via <abbr title="Beta Reviewers Auto-update Tester">BRAT</abbr> (for pre-releases or betas)

1. Install [BRAT](https://github.com/TfTHacker/obsidian42-brat).
2. Add "Mononote" to BRAT:
    1. Open "Obsidian42 - BRAT" via Settings → Community Plugins
    2. Click "Add Beta plugin"
    3. Use the repository address `czottmann/obsidian-mononote`
3. Enable "Mononote" under Settings → Options → Community Plugins


## Development

Clone the repository, run `pnpm install` OR `npm install` to install the dependencies.  Afterwards, run `pnpm dev` OR `npm run dev` to compile and have it watch for file changes.


## Author

Carlo Zottmann, <carlo@zottmann.co>, https://zottmann.co/, https://github.com/czottmann


## Disclaimer

Use at your own risk.  Things might go sideways, hard.  I'm not responsible for any data loss or damage.  You have been warned.

Always back up your data.  Seriously.


## License

MIT, see [LICENSE.md](LICENSE.md).
