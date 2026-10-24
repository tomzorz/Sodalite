# Contributing

Bug reports and pull requests are welcome.

## Reporting a problem

Open an issue with your Obsidian version, your OS and a screenshot. If you use CSS snippets or plugins that change the interface, try once with them turned off, so it is clear the problem is in Sodalite.

## Changing the theme

- Test in a throwaway vault on the current Obsidian release, not in a vault you care about.
- Where Obsidian has a [CSS variable](https://docs.obsidian.md/Reference/CSS+variables/CSS+variables) for what you want to change, set the variable instead of overriding Obsidian's selectors. Obsidian has renamed classes between releases, which breaks selector overrides; the variables are the interface it documents for themes.
- When a selector is unavoidable, match the specificity of the Obsidian rule you are overriding instead of adding `!important`. The community theme scan flags every `!important`.
- Sodalite's own colors and sizes live in the `--sdlt-*` tokens at the top of `theme.css`. Add new values there.
- Note visible changes in the changelog in `README.md`.

## Releases

The maintainer bumps the version and publishes releases. The version appears in two places, `version` in `manifest.json` and the title bar text in `theme.css`, and the two have to match.
