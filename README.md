# UniExtract
Universal Extractor 2 or Universal Extractor (Bioruebe version) as it is also called to avoid confusion is an unofficial updated and extended version of the [original UniExtract by Jared Breland](http://legroom.net/software/uniextract). As the development of the original version has stopped and no update has been published for years, many forked (modified and maintained by the community) Universal Extractors have arised. This is the most advanced and the only one with a fully transparent development using a public GitHub-powered source code repository.

## New features

- Batch mode
- Scan only mode to determine file types without extracting
- Built-in updater
- 100+ new supported file types
- Audio and video extraction for multimedia files
- Cascading context menu
- Support for password list for common archives
- Improved optional status box with progress indicator
- Better and faster file analysis
- Support for some extractors not shipping with UniExtract as plugins
- Silent mode, not showing any prompts
- Many interface improvements and redesigned dialogs
- Resource usage/speed improvements, lots of fixes
- Auto-using 64 bit versions of extractors if supported by OS

See the changelog for a complete log of all improvements.

## Download
Get the latest version [here](https://github.com/Bioruebe/UniExtract2/releases)

Virus alert? - Universal Extractor does not contain any malware. Some anti-virus software occasionally misdetects files inside UniExtract's program directory. (You know, better warn too much than let any malware slip through.) But you can be sure that this is a so-called false positive, an error - if you downloaded UniExtract from the official source at `https://github.com/Bioruebe/UniExtract2`. If you encounter a false positive, please report it [here](https://github.com/Bioruebe/UniExtract2/issues/78).

'Windows protected your PC'? - Modern versions of Windows have a feature called SmartScreen, which warns about unknown files. This means software without a big company behind it and/or a huge userbase produces a warning. Don't panic! Mostly this happens after a new version of UniExtract has been released. After enough users updated their installation, the warning might vanish, because it now has reputation. If you see a SmartScreen warning, you can safely click 'More info', then 'Run anyway'.

## FAQ

#### Is there a portable version?

Universal Extractor itself is completely portable, with some exceptions:
- Enabling context menu entries will create registry entries
- To extract a wide variety of file types more than 50 different extractors are used. Some of them might leave traces on the system. For the most common archives and installers extraction can be considered portable, for others probably not.
- Storing Universal Extractor in a directory without write access (e.g. C:\Program Files) enables multi-user mode. This results in configuration files being stored in the %APPDATA% directory (C:\Users\YourUsername\AppData\Roaming\Bioruebe\UniExtract).
  See issue [#20](https://github.com/Bioruebe/UniExtract2/issues/20) for more information.

#### Why are there many different versions/modifications/repacks of Universal Extractor?

When the original developer of UniExtract stopped working on it, many people from around the world continued to update and improve the program. Some 'only' updated the tools Universal Extractor uses, others added great features. As a result all versions differ in terms of supported archives and features added.

This version is the only 'real' open-source one, with a central repository on Github everyone can contribute to. Over the years I fulfilled many user requests, added support for files the community wanted to decompress and implemented a lot of convenience functions. Many volunteers help translating UniExtract, finding bugs, discussing improvements and respond to other user's questions.

However, Universal Extractor 2 may fail to unpack files, which other versions of this tool can extract. If you *really* need to access the contents of an archive, you may have success with one of the other UniExtracts. Alternatively, you can also ask for support here. It might take a while until I can answer, though.

#### Can UniExtract (re)compress files?

No. This tool was designed as an extraction utility. A counterpart (*"UniArchive"*) is out of scope - at least for me. (Read about the reasons [here](https://github.com/Bioruebe/UniExtract2/issues/87#issuecomment-409806225).) Feel free to create it! 

## Nightly Builds

You can opt-in to receive the most current development build of Universal Extractor 2. Simply open the preferences dialog (from 'Edit' menu) and check `Install beta updates`. The next time you search for updates, you will receive the development build instead of the release version. After disabling the option again you can go back to the latest stable version by simply updating.

## Reporting bugs
Did you encounter a problem with UniExtract? Please report what went wrong to us. There are differnet ways to do so:
- If you have a Github account, you can **[open an issue](https://github.com/Bioruebe/UniExtract2/issues)**. This is the prefered way for **feature requests**, **suggestions** and **general technical problems**.
- From within Universal Extractor: select **'Give feedback'** from the **'Help' menu**. This is the prefered way to submit **failed extractons**. If UniExtract was not successful, it will automatically ask you to send feedback (can be disabled from the options). This type of feedback includes a log with several debug information, which could help fixing the problem.
- Direct contact via **[email](https://bioruebe.com/blog/contact/)**. This can be used if you do not have an account at Github. Many users, who created translations for UniExtract, like to send updated files per email. (Others open [pull requests](https://github.com/Bioruebe/UniExtract2/pulls) instead.)

## Building from Source

1. Download and install [AutoIt](https://www.autoitscript.com/site/autoit/downloads/)
2. Download and install [SciTE](https://www.autoitscript.com/site/autoit-script-editor/downloads/) (Optional)
3. Clone this repository **or** download a snapshot and unpack into a folder of your likings
4. Open UniExtract.au3 in SciTE and hit `F5` to run in debug mode; `F7` to build an executable file **or** run UniExtract.au3 through Aut2Exe (look [here](https://github.com/Bioruebe/UniExtract2/issues/72#issuecomment-313288728) for more information about Aut2Exe)
5. ~Download the latest release version and unpack into the same directory to install additional program files not included in the source distribution. Do not overwrite files.~ Beginning with RC 1, this has been simplified: just run the updater after building. All neccessary files are downloaded automatically. Make sure to not overwrite UniExtract.exe: if the update message says an update for Universal Extractor is available select no, then answer with yes when being notified about 'Universal Extractor program files'.

## Contributions

Any contribution in form of ideas, bug reports, code commits, documentation improvements, etc. is welcome. Help is currently needed in updating the translations for many languages. If you are able to translate into another language, take a look at the corresponding issue (#2) or open the language file in the `/lang` subdirectory and check for empty strings. English and German language are always up-to-date and can be used as a reference.

Feel free to submit bug reports or feature requests using the issues tab or the built-in feedback window in Universal Extractor, accessible via the 'Help' menu. Refer to Github's issue page for planned features and problems to be fixed in future versions. The file `todo.txt` is a leftover from the original Universal Extractor and only used for personal development thoughts and notes.

## License

Universal Extractor is licensed under GPLv2. See LICENSE for the full legal text.
Code (functions, UDFs, etc.) written from scratch by me (which are not under copyleft) can also be used in your own projects under the terms of a BSD 3-clause license.

Universal Extractor uses [TrIDLib by Marco Pontello](http://mark0.net/code-tridlib-e.html) and many other great tools and libraries to support as many file formats as possible. A detailed list can be found [here](https://github.com/Bioruebe/UniExtract2/blob/master/helper_binaries_info.txt).
