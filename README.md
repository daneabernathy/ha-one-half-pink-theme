# One Half Pink

A dark [Home Assistant](https://www.home-assistant.io) theme: neutral
dark greys with hot pink (`#F92672`) for the primary colour, accents and
active states. Started from the One Half Dark colour scheme, then made
darker and less blue.

<!-- Screenshot: add images/screenshot.png and link it here -->

## Status

| Check | Result |
| --- | --- |
| Theme file parses as YAML | ✅ |
| HACS validation (GitHub Actions) | ❌ Not run yet |
| Installed and checked in Home Assistant | ❌ Not tested in this version |

`primary-color`, `accent-color` and the `state-*` variable pattern are
checked against the Home Assistant documentation; the other variable
names come from common theme practice and haven't been individually
confirmed.

## Install with HACS

1. In Home Assistant, open **HACS**, then the three-dot menu, then
   **Custom repositories**.
2. Add `https://github.com/daneabernathy/ha-one-half-pink-theme` with
   type **Theme**.
3. Find **One Half Pink** in HACS and download it.
4. Make sure your `configuration.yaml` loads themes from the `themes`
   folder, then restart Home Assistant:

   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```

5. Open your **profile** and choose **One Half Pink** under **Theme**.

## Install manually

1. Copy [themes/one_half_pink.yaml](themes/one_half_pink.yaml) into
   `/config/themes/` on Home Assistant.
2. Add the `frontend:` lines above to `configuration.yaml` if they
   aren't there, then restart Home Assistant. After that, the
   `frontend.reload_themes` action picks up theme changes without a
   restart.
3. Choose **One Half Pink** in your profile.

## Customising

The theme is a list of Home Assistant CSS variables. Change a hex value
and run `frontend.reload_themes` to see it. The `modes: dark:` block at
the end tells Home Assistant to build on its dark defaults; without it,
dialogs and some controls come out light.

## Contributing

Issues and pull requests are welcome. The GitHub Actions workflow runs
the HACS validation on every change.

## Acknowledgements

Designed by Dane Abernathy with help from
[Claude](https://www.anthropic.com/claude) (Anthropic), used through
Claude Code to draft the theme file and documentation. Commits Claude
helped write carry a `Co-Authored-By: Claude` trailer. Every change is
reviewed by the maintainer.

## License

[MIT](LICENSE)
