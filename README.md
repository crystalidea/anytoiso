# AnyToISO

This repository is for everything around [AnyToISO](https://crystalidea.com/anytoiso) that is not the program itself: issues, translations and the release archive. The source code of the app is not published here.

## Report an issue

Found a bug, or want a format supported? [Open an issue](https://github.com/crystalidea/anytoiso/issues).

Useful things to include: the version of AnyToISO, your operating system, what you did and what happened instead. If an image or an archive is involved, its format and size help a lot.

## Translate the app

Translations live in [languages](/languages) as plain UTF-8 XML files, one per language. They are the same files the program ships with, so a change here goes straight into the next release.

To update an existing translation, edit its file and open a pull request. To add a language, copy `English.xml`, translate it and name the file after the language in English — `Thai.xml`, `Norwegian.xml`. The program lists every `.xml` in that folder, and the file name is what people see in Preferences. You can also mail the file to support@crystalidea.com if pull requests are not your thing.

A few rules keep a translation working:

- **Keep the tags as they are.** The program looks each string up by its tag, so renaming, adding or dropping tags loses the string. Anything you leave out falls back to English, which is also a fine way to hand in a partial translation.
- **Keep `%1`, `%2`, `%s` where they belong.** They are replaced at run time: `Package %1 opened` becomes `Package firefox4pre opened`. Their order may change if your language needs it.
- **Do not translate values that are not sentences.** Some strings carry an internal marker the program matches exactly, for example the link target in
  `Click <a href="_open_local_file">here</a> to open the output folder`.
  Translate the visible words and leave `_open_local_file` alone — a translated marker turns the link into dead text.
- **Keep the file UTF-8 with LF line endings**, and feel free to put your name in the `Author` attribute at the top. Translators are credited.

## Browse the release history

The [release archive](https://github.com/crystalidea/anytoiso/releases) holds every published version with its binaries and release notes.
