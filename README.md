# PlayerPrefs Editor & Utilities

[![openupm](https://img.shields.io/npm/v/com.sabresaurus.playerprefseditor?label=openupm&registry_uri=https://package.openupm.com)](https://openupm.com/packages/com.sabresaurus.playerprefseditor/) [![GitHub](https://img.shields.io/github/license/sabresaurus/PlayerPrefsEditor)](https://github.com/sabresaurus/PlayerPrefsEditor/blob/master/LICENSE.md) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blue.svg)](http://makeapullrequest.com)

<img align="right" src="https://user-images.githubusercontent.com/17784523/154849207-15bf8111-fa6c-401f-8b7d-4bed69520216.png" width="400" />

PlayerPrefs Editor & Utilities provide an easy way to see what PlayerPrefs your game is using and change them at run-time. It also includes encryption support to protect your player prefs from casual hacking and has additional support for more data types.

Editor features include:
- list all active PlayerPrefs and EditorPrefs
- search for prefs to refine results
- change pref values at run-time
- add new prefs
- delete prefs
- quick delete all button
- import prefs from another project
- supports working with the encryption features added in the utilities

Utilities features include:
- set and get the built in PlayerPref types using an encryption layer - plain text values are transparently converted to encryption so that the PlayerPrefs are protected in the device data stores
- set and get Enum values
- set and get DateTime values
- set and get TimeSpan values
- set and get Bool values

This package was originally sold on the [Unity Asset Store](https://www.assetstore.unity3d.com/en/#!/content/26656), but as of 29th April 2017 has been open sourced under the MIT License (see LICENSE for details). It is now maintained on this [Github repository](https://github.com/sabresaurus/PlayerPrefsEditor).

For a more comprehensive quick start guide and API documentation please go to http://sabresaurus.com/docs/playerprefs-editor-utilities-documentation/


## PlayerPrefs Editor

To open the PlayersPrefs Editor go to Window -> PlayerPrefs Editor

This will open an editor window which you can dock like any other Unity window.


### The Player Prefs List

If you have existing saved player prefs you should see them listed in the main window. You can change the values just by changing the value text box, you can also delete one of these existing player prefs by clicking the X button on the right.


### Search

The editor supports filtering keys by enterring a keyword in the search textbox at the top. As you type the search results will refine. Search is case-insensitive and if auto-decrypt is turned on it will also work with encrypted player prefs.


### Adding A New Player Pref

At the bottom of the editor you'll see a section for adding a new player pref. There are toggle options to determine what type it is and a checkbox for whether the player pref should be encrypted. Once you've selected the right settings and filled in a key and value hit the Add button to instantly add the player pref.


### Deleting An Existing Player Pref

To delete an existing player pref, click the X button next to the player pref in the list. You can also delete all player prefs by clicking the Delete All button at the bottom of the editor.


## PlayerPrefs Utilities

IMPORTANT: If using encryption, make sure you create a custom key under More Options, this will make sure your key is unique and make the protection stronger.

In PlayerPrefsUtility.cs you'll find a set of utility methods for dealing with encryption and also new data types. There is documentation within this file explaining how each method works. There is also additional documentation at http://sabresaurus.com/docs/playerprefs-editor-utilities-documentation/

# License

Licensed under MIT, see **LICENSE** for details.

# Installation

<details>
<summary>Add from OpenUPM <em>| via scoped registry, recommended</em></summary>

This package is available on OpenUPM: https://openupm.com/packages/com.sabresaurus.playerprefseditor/

To add it the package to your project:

- open `Edit/Project Settings/Package Manager`
- add a new Scoped Registry:
  ```
  Name: OpenUPM
  URL:  https://package.openupm.com/
  Scope(s): com.sabresaurus
  ```
- click <kbd>Save</kbd>
- open Package Manager
- click <kbd>+</kbd>
- select <kbd>Add from Git URL</kbd>
- paste `com.sabresaurus.playerprefseditor`
- click <kbd>Add</kbd>
</details>

<details>
<summary>Add from GitHub | <em>not recommended, no updates through UPM</em></summary>

You can also add it directly from GitHub on Unity 2020.3+. Note that you won't be able to receive updates through Package Manager this way, you'll have to update manually.

- open Package Manager
- click <kbd>+</kbd>
- select <kbd>Add from Git URL</kbd>
- paste `https://github.com/sabresaurus/PlayerPrefsEditor.git`
- click <kbd>Add</kbd>  
**or**  
- Edit your `Packages/manifest.json` file to contain `"com.sabresaurus.playerprefseditor": "https://github.com/sabresaurus/PlayerPrefsEditor.git"`,
  
To update the package with new changes, remove the lock from the `Packages/packages-lock.json` file.
</details>

To open the window go to `Window → PlayerPrefs Editor`