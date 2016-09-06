# ansible-libreoffice

Install LibreOffice via the Mac App Store or Homebrew.

Note that if installed via the Mac App Store, the app name is "LibreOffice Vanilla". This is near-identical to the Homebrew distribution, except for a popup directing first-time users to the LibreOffice website.

## Role Variables

* `prefer_mas_over_homebrew`: Defaults to `false`.

## Dependencies

* [icopp.mas-cli](https://github.com/icopp/ansible-mas-cli), but only if `prefer_mas_over_homebrew` is `true`.
* [icopp.homebrew-cask](https://github.com/icopp/ansible-homebrew-cask), but only if `prefer_mas_over_homebrew` is `false`.

## Example Playbook

```
  - hosts: all
    roles:
      - role: icopp.libreoffice
```

```
  - hosts: all
    roles:
      - role: icopp.libreoffice
        prefer_mas_over_homebrew: true
```

## License

MIT
