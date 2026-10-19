# Syslog Watcher Manager translations

Each `<code>.txt` file in this repository is one user interface language for
Syslog Watcher Manager. The installer copies the `.txt` files (not this
README) into a Translations folder next to `SW7Manager.exe`. At startup, 
Manager lists every file found here under **Manager Properties > UI language**. 
A new language takes effect after Manager is restarted.

Any string that is missing from the file, or marked with `#`, is shown in
English.

## Branches

Each Syslog Watcher version has its own branch: `7.0`, `7.1`, and so on. Send
changes to the branch of the version you are translating.

## File format

UTF-8 text, one entry per line:

```
0 "Deutsch (German)"
// Manager Settings 12000
// a note from the translator
//ORI "Syslog Watcher Manager"
12000 "Syslog Watcher Manager"

//ORI "Behavior"
12002 "Verhalten"

//ORI "Auto-connect to local server"
#12004 "Automatisch verbinden"

//ORI "Admin"
10717 "Admin" // user role; also in the window caption "(As Admin)"
```

- `0 "..."` is the language name shown in Manager. It is required; a file
  without it is ignored.
- `<ID> "<text>"` is a translated string. The text uses the same escapes as
  the English `.rc2` file: `\n`, `\r`, `\t` and `\\`, and `""` for a quote.
  Keep placeholders such as `%s`, `%d` and `{}` exactly as they are in the
  English text.
- `//ORI "..."` is the English text that the translation was made from.
  Do not edit it.
- `#<ID> "..."` needs review: the string is new, or its English text changed.
  Manager shows English until the `#` is removed.
- `// ...` after the text on an entry line is a hint copied from the English
  file. Do not translate it; an update replaces it when the English hint
  changes.
- Other lines starting with `//` are comments. Your own comments go on lines
  of their own.

The file name without `.txt` is the language code saved in the Manager
settings, so do not rename a file after it has been released.

## Contributing

1. Edit a `.txt` file and send a pull request to the version branch.
   Translate the text and remove the `#` from each entry you reviewed. Do not
   change IDs, `//ORI` lines or the hints after the text.
2. To add a language, open an issue. The file is created from the English
   string table, so every string starts as the English text.

New strings, changed English text and removed strings are applied by EZ5
Systems when the English text changes. Your translations, comments and blank
lines are kept.

## License

The translation files are published under the MIT No Attribution License
(see [LICENSE](LICENSE)). By sending a pull request you agree that your
contribution is licensed under the same terms.
