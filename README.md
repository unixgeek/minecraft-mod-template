# Template Usage
This section describes the initial steps to setting up the template. It should be deleted afterwards.

## GitHub Setup
These steps are needed to configure the automatic release creation when a tag is created in GitHub.
1. In GitHub click your _Profile_ then _Settings_.
2. Click on _Developer settings_ in the menu.
3. Click on _Personal access tokens_ in the menu.
4. Click _Generate new token_ and choose _repo_ access and any other settings you want.
5. Click _Generate token_.
6. Copy the token.
7. Navigate back to this repository.
8. Click _Settings_.
9. Click _Secrets_ then _Actions_ in the menu.
10. Click _New repository secret_.
11. Choose `CUSTOM_GITHUB_TOKEN` as the name.
12. Paste your token as the value.
13. Click _Add secret_.

## MCreator Setup
1. Launch MCreator.
2. Click _Clone remote_.
3. Set _Remote Git repository HTTPS URL_.
4. Set _Your Git account username_.
5. Paste your token in _Your Git account password/access token_.
6. Click _Setup remote workspace_.
7. Wait for MCreator to build.
8. In the menu click _Workspace_ then click _Workspace settings_.
9. Update fields as appropriate and click _Save changes_.
10. Project may need to be rebuilt, so click _Yes, refactor workspace_ if prompted.

## Local Files Setup
1. Update NAME_PLACEHOLDER and DESCRIPTION_PLACEHOLDER below.
2. Update NAME_PLACEHOLDER in LICENSE file.
3. Remove this line and everything above it.

# NAME_PLACEHOLDER
DESCRIPTION_PLACEHOLDER

## Requirements
* [Minecraft: Java Edition 1.18.2](https://www.minecraft.net/en-us/store/minecraft-java-edition)
* [Minecraft Forge 1.18.2](https://files.minecraftforge.net/net/minecraftforge/forge/index_1.18.2.html)
* [MCreator 2022.1 (Only for Development)](https://mcreator.net/)

## Installation
Copy the mod jar file to the mods directory `${HOME}/.minecraft/mods` or `${HOME}/AppData/Roaming/.minecraft/mods` for Windows.

## Development

### Setup
1. Launch MCreator.
2. Click _Clone remote_.
3. Set _Remote Git repository HTTPS URL_.
4. Set _Your Git account username_.
5. Paste your token in _Your Git account password/access token_.
6. Click _Setup remote workspace_.

### Committing Changes
To commit your changes click _Remote workspace_ in the menu then click _Sync local changes with remote workspace_.

### Creating a Release
1. In the menu click _Workspace_ then click _Workspace settings_.
2. Update the _Mod version_ field to the desired version.
3. Click _Save changes_.
4. In the menu click _Build & run_ then click _Build workspace_.

This template uses a GitHub Action to create a release any time a tag is created. Unfortunately, MCreator doesn't 
have an option to create a tag, so you will need to do that from the command-line.
1. Create a tag, set the version as appropriate: `git tag 1.0.0`
2. Push the tag to GitHub: `git push --tags`

In GitHub, you should see the Action triggered. Once it is complete, a new release will have been created.