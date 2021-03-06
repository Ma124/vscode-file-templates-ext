# File Templates VSCode Extension

[![Build Status](https://travis-ci.org/brpaz/vscode-file-templates-ext.svg?branch=master)](https://travis-ci.org/brpaz/vscode-file-templates-ext)

[Visual Studio code](https://code.visualstudio.com) extension that allows to quickly create new files based on defined templates.

Inspired by [this Atom Extension](https://atom.io/packages/file-templates).

## Available Commands

* Create a new file from a template
* Create a new template from an existing file.

## Screenshots

![preview](images/preview01.jpg)

## Install

On Visual Studio code, Press F1 to open the command menu and type ```ext install file-templates```.

**This extension was only tested on Linux. If you have a Mac or Windows and find some issue, please create a PR.**

## Usage

* In VSCode, right click on the folder where you want to generate the new file. You should see an option "Files : New from template". 
Selecting this option a list of available templates should appear. Just select your template and the file will be created.

* You can also do the same from the Command Palette. In this case the new file will be created in the root directory of the project.

* Its also possible to do the other way around and create a template based on an open file. For that "right-click" on any opened file and you should see the option of the context menu.

## Variables

Variables can now be used in templates in the following way:

```
normal text #{variable_name}
```

When a file is created from the template, the user is prompted with a value to put here.

### Predefined variables

* `filename`: the output filename.
* `filepath`: the output filepath.
* `year`: the current year, e.g. `2020`.
* `date`: the current date, e.g. `1 Jan 2020`.
* `time:<moment.js format>`: a custom time format (for `<moment.js format>` see the [moment.js docs](https://momentjs.com/docs/#/displaying/))

## Templates Location.

By default, this extension expects the file templates to be placed at the following location, depending of your OS:

Linux:

```
$HOME/.config/Code/User/FileTemplates
```

Mac:

```
$HOME/Library/Application Support/Code/User/FileTemplates
```

Windows:

```
C:\Users\User\AppData\Roaming\Code\User\FileTemplates
```

However, you can change the default location by adding the following to your user or workspace settings:

```
"fileTemplates.templates_dir": "path/to/my/templates"
```

## Contributing

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.


