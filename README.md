### Adding add-ons to your repository
---
To build the repository, first place the add-on source folders for whichever add-ons you'd like to be contained in your Kodi repo inside this repository. 
For ease of updating included add-ons, the recommended method of doing this is via [Git Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules), which are supported by many Git clients, as well as the Git terminal. 
Example for VSCode: in the repo folder, run in the terminal: ['git submodule add https://github.com/jurialmunkey/plugin.video.themoviedb.helper.git']

The `_repo_xml_generator.py` script included in this repository with build `.zip` files for each included add-on, as well as generating the necessary `addons.xml` and `addons.xml.md5` files, so that Kodi can infer the contents of the repo. It is designed to handle multiple versions of Kodi (for example, to serve different add-ons to Leia than are served to Matrix), and single repositories that serve the same add-ons to all Kodi versions.

##### Same add-ons to all versions (default)
---
Place your add-on source folders in the `repo` folder of this repository.
---
After adding your source folders, simply run `_repo_generator.py`. This will create `.zip`s of all of the desired add-ons, and place them in subfolders called `zips`, along with the generated `addons.xml` and `addons.xml.md5`. As of version 3, this script can create distributions for Krypton, Leia, Matrix, and Nexus, as well as the generic "repo", which is intended to serve to any version (like for the repository itself, or any cross-version libraries and dependencies).

### Make your repository zip installable inside Kodi
---
Copy the zip file of your repository, located at `repo/zips/repository.caspar007/repository.caspar007-VERSION_NUMBER_HERE.zip`,
and paste it into the root folder. Rename the file and remove the version number!

Here is your zip file:
`https://caspar007.github.io/repository.caspar007`
