# Markdown2Dir

This package adds a feature to Sublime Text that makes it easier to manage Markdown files containing code blocks by allowing seamless extraction and reinsertion of those blocks to and from the file's parent directory.

Its home is here on [GitHub](https://github.com/JohhannasReyn/Markdown2Dir/).

## Features

- **Directory to Markdown**: Extract code blocks from a Markdown file and save them as separate files in the same directory.
- **Markdown to Directory**: Update the Markdown file with code from corresponding files in the directory.
- Configurable file naming conventions.
- Options to ignore specific blocks or handle file conflicts gracefully.

## Installation Options

- <strike>From within Sublime Text's Package Control: Install Package, search for Markdown2Dir, select and hit enter.</strike>
  - **NOTE**: This plugin is not yet featured in the Subline Text Package Manager Repo. Follow instructions below to install. It's both safe and functional. (Read `Usage Options` [below] prior to first use)
- Download this repository, save it with the extension ".sublime-package" (i.e., "Markdown2Dir.sublime-package") in your "\Sublime Text\Installed Packages\" directory.
  - On Windows, this is usually "C:\Users\<UserName>\AppData\Roaming\Sublime Text\Installed Packages\".
    - If Sublime Text is already open, and you don't see it listed under:
      *Preferences* -> *Package Settings*, then you'll need to restart Sublime Text.

- Download the zipped project from this repo, extract `Markdown2Dir.sublime-package` that's inside of `Markdown2Dir-main` to  'C:\Users\<UserName>\AppData\Roaming\Sublime Text\Packages'
- **Name should be `Markdown2Dir.sublime-package`**
- For setting up the menu options, key-commands, or context menu entries, open the appropriate file that corresponds with the feature you wish to enable. (i.e. "Context.sublime-menu" for the context menu options, "Main.sublime-menu" for the main menu options which, when enabled, are found in the menu bar, under > "Tools". As for the keymaps, if you wish to configuree -> select the one for your operating system only. -- e.g. Default (Windows).sublime-keymap for Windows, etc.)
- Follow the instructions in each file you wish to enable which will instruct you on where to place the single '/' to enable the feature.

## Usage Options

- ***Adjust the plugin settings first!*** (Refer to the settings file, or doc, for details)
  - ***NOTE***: You **MUST** configure the plugin before your first use (and ideally before each build out), or you may encounter unexpected/undesirable results.

- ***Configuration***
  - Options can be configured in Markdown2Dir.sublime-settings. Access via: *Preferences* -> *Package Settings* -> *Markdown2Dir-Settings*.

- ***Enable plugin commands***:
  - To enable the context menu options, key-combinations, or menu entries for this plugin, open the corresponding file(s) in this plugin's folder, and follow the instructions.
  - The hard part has already been done, you simply need to comment out a single line in each of the files to enable its features.  

- **PROCEED ONLY AFTER THE SETTINGS HAVE BEEN CONFIGURED**

- ***To: BUILD FROM MARKDOWN***
  - Open a Markdown file (.md, .markdown) to build out a directory/project folder from markdown

- ***To: BUILD MARKDOWN FROM DIRECTORY***
  - Create a markdown file in the root of a project directory.
    - Best if the created markdown file has the same name as the project folder it resides in, i.e: <your-project>/<your-project>.md

    ```Example Directory Structure
    MyProjectFoo
    ├── src/
    │   ├── main.foo
    │   ├── index.bar
    ├── MyProjectFoo.md   <-- You Create This File
    └── MyProjectFoo.sublime-settings   <-- This file will be created for you 
    ```
- ***Notes Regarding Plugin Settings***:
  - The generated `*.sublime-settings` file is built using the settings you have defined in your `Packages\Markdown2Dir\Markdown2Dir.sublime-settings` file. (Previously configured if you followed steps above)
  - The `*.sublime-settings` file is generated in **EITHER** use case. (when building out a directory **OR** when building an `*.md` file from a directory)
  - This file is referenced first, (given the highest priority) when building out a project.
    - This is so you don't have to adjust your packahge settings for each project. (Each project's settings persist independently for convenience)
  - There is an additional 'settings' generated inside the markdown file built from a `Directory-2-Markdown` operation that is given the second highest prescedence.
    - This is so the genreated markdown file can be moved independently to any other location and build out a complete project directory using the same config that it was built from.
  - ***NOTE***: If you wish to reset the settings of an inproperly configured build-out, if you only delete your project's `*.sublime-settings`, and leave the code fence untouched, the previous settings will still be applied.
    - This is likely undesired if you intentionally deleted the 'sublime-settings' file, if this is the case, you will also need to remove the `# Directory Settings` section in the markdown like
    - ***NOTE***: Be sure to save the file after editing it in order for the changes made to be applied.
    - By default this is the second code fence inside the generated markdown file, (the first if you set: `"output_directory_tree"` to `false`)

- ***The Generation/Build-Out***
  - Via the Right-click Context Menu (if enabled) select *Directory to Markdown* or *Markdown to Directory*.
  - Via the Menu Bar (if enabled): *Tools* -> *Markdown2Dir* -> *Build Directory from Markdown* or *Build Markdown from Directory*.
  - Via Key Bindings (if enabled): Use the defined key-mapping specified in the sublime-keymap file. Suggested mappings:
    - `Ctrl+Alt+M` for *Directory to Markdown*.
    - `Alt+Shift+M` for *Markdown to Directory*.

## License

Markdown2Dir is available under two licenses:

- **Standard User License (Free)**: For personal and non-commercial use. [View License](LICENSE)
- **Commercial License**: For commercial use, including collaboration features and priority support. [View Commercial License](COMMERCIAL_LICENSE)

For commercial inquiries, please contact [John@DreamEmbedded.com](mailto:John@DreamEmbedded.com)

## Support

- For general questions and discussions, open an [issue](https://github.com/JohhannasReyn/Markdown2Dir/issues)
- For commercial support, contact [John@DreamEmbedded.com](mailto:John@DreamEmbedded.com)
- Check the [documentation](https://github.com/JohhannasReyn/Markdown2Dir/wiki) for detailed information

---
Made by Johhannas Reyn
