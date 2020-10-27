---
title: Sync vscode settings between computers with git
published: true
---

If your favourite IDE/TextEditor is vscode/vscodium and if you have multiple devices then you may want to have same settings and extensions for vscode in all your devices. There are 1 or 2 ways you can do that but we will try the easiest and the most reliable one.

there is an extension for syncing/uploading/downloading your vscode settings extensions via a github repository called [`Syncify`](https://marketplace.visualstudio.com/items?itemName=arnohovhannisyan.syncify). I personally have been using this extension for almost a year.

To use Git, you must first configure it by providing your name and email. To do this, run the following in your terminal, replacing the placeholders with the corresponding values.

```
git config --global user.name "<Your Name>"
git config --global user.email "<Your Email>"
```

# Installation

## Using Extension Panel

1. Open the extensions panel: Ctrl+Shift+X (⌘ on Mac)
2. Type syncify
3. Click Install

## Using Command Palette

1. Open the command palette: Ctrl+P (⌘ on Mac)
2. Type ext install arnohovhannisyan.syncify
3. Press Enter to install

<br>

The extension provides us with two types of syncing **repo sync** nad **file sync**, here we don't need **file sync** so we will leave it for now. the repo sync method allows us to sync the settings and extensions by creating a private github repo.

# Setup

## Automatic Setup using OAuth

This method requires Syncify to ask for full control over your public and private repositories, however, this is a limitation of the APIs provided by GitHub, GitLab, and BitBucket. If you are worried about security, feel free to manually set up Syncify using SSH.

Open the Command Palette (`Ctrl+Shift+P`) and run `Syncify: Upload`.
Click the login button for your preferred provider (`GitHub`, `GitLab`, or `BitBucket`).
Authorize Syncify to access your repositories.

<br>

### If this is your first time using this extension:

Choose the name of your new settings repository by entering it in the first text box.
Click Create to create it and click Close to return to VSCode.

<br>

### If you have already uploaded our settings before:

Click the List Repositories button to get a list of your repositories
Click the Use This button next to the repository you would like to register.

Finally, open the Command Palette (`Ctrl+Shift+P`) and run `Syncify: Upload` if you just created a repository, or `Syncify: Download` if you've already uploaded your settings before.

<br>

# Manual Configuration

The URL to the repository can also be the path to a local git repository.

## Using the GUI

Run `Syncify: Open Settings` in the command palette
Enter the URL of your desired repository into the File Syncer -> File Export Path field

## Manually

Run `Syncify: Open Settings` in the command palette
Click `Open file in editor`
Set the value of the `repo.url` property to the URL of your desired repository

Example snippet from settings file:

```json
{
    "repo": {
        "url": "git@github.com:arnohovhannisyan/code-settings"
    }
}
```
<br>

# Profiles

## Creating New Profile

## Using the GUI

1. Run `Syncify: Open Settings` in the command palette
2. Scroll down to the `Repo Syncer` -> `Profiles section`
3. Click the `+` button to create a new profile
4. Fill in the branch and name fields

## Switching the Current Profile

Run `Syncify: Switch profile` in the command palette Select the profile you want to switch to

After switching the current profile using the command, Syncify will prompt you to download the new settings.

### Example Configuration

```json
{
    "syncer": "repo",
    "repo": {
        "url": "...",
        "profiles": [
            {
                "branch": "master",
                "name": "main"
            },
            {
                "branch": "react",
                "name": "react-tools"
            }
        ],
        "currentProfile": "react-tools"
    }
}
```
## Manually

Run `Syncify: Open Settings` in the command palette
Click `Open file in editor`
Add a new object to the `repo.profiles` array with the following format

```json
{
    "branch": "[BRANCH]",
    "name": "[NAME]"
}
```

`[BRANCH]` is the Git branch that will be used to store your settings, while `[NAME]` is the name of the profile.

## Switching the Current Profile

Run `Syncify: Switch profile` in the command palette Select the profile you want to switch to

After switching the current profile using the command, Syncify will prompt you to download the new settings.

### Example Configuration

```json
{
    "syncer": "repo",
    "repo": {
        "url": "...",
        "profiles": [
            {
                "branch": "master",
                "name": "main"
            },
            {
                "branch": "react",
                "name": "react-tools"
            }
        ],
        "currentProfile": "react-tools"
    }
}
```
<br>

# Final Notes

The `Syncify` is the best and reliable way I have tried to sync my settings and extensions for vscode. And this also works for the open source alternative of the vscode, [vscodium](https://vscodium.com/).

<br>

## References

Documentation: <https://arnohovhannisyan.space/vscode-syncify/><br>
Github: <https://github.com/arnohovhannisyan/vscode-syncify><br>
Spectrum: <https://spectrum.chat/vscode-syncify><br>
Discord: <https://discord.gg/DwFKj57><br>