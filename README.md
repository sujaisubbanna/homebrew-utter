# Homebrew tap for utter

Homebrew formulae and cask for [utter](https://github.com/sujaisubbanna/utter-assistant) —
a local, offline, context-aware voice to desktop-action assistant.

## Install

```bash
brew tap sujaisubbanna/utter
brew install utter          # CLI + launchd service (macOS)
brew install --cask utter   # GUI app (macOS)
```

- `brew install utter` installs the Python assistant into Homebrew's `libexec`, links
  `utter` and `utter-runner` into `$(brew --prefix)/bin`, and installs the launchd service
  templates. Start the background daemon with:

  ```bash
  brew services start utter
  ```

- `brew install --cask utter` installs `utter.app` (GUI settings app) from the GitHub
  release. On first launch, clear Gatekeeper once with `xattr -cr /Applications/utter.app`.

Both require macOS. The formula depends on `python@3.12` and `portaudio`.

## Upgrade

```bash
brew update
brew upgrade utter          # CLI
brew upgrade --cask utter   # GUI
```

## Uninstall

```bash
brew services stop utter
brew uninstall utter
brew uninstall --cask utter
brew untap sujaisubbanna/utter
```

## Feedback

Issues and pull requests: <https://github.com/sujaisubbanna/utter-assistant/issues>.

## License

Apache-2.0. See [LICENSE](LICENSE).
