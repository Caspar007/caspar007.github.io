### Adding add-ons to your repository

#### For ease of updating included add-ons, the recommended method of doing this is via [Git Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules), 
#### Example for VSCode: 
Open the repo sub folder in the code explorer, run in the terminal:

`git submodule add https://github.com/jurialmunkey/plugin.video.themoviedb.helper.git`

The `_repo_xml_generator.py` script included in this repository will build `.zip` files for each included add-on, as well as generating the necessary `addons.xml` and `addons.xml.md5` files, so that Kodi can infer the contents of the repo. 

----

### Make your repository zip installable inside Kodi
Copy the zip file of your repository, located at:

 `repo/zips/repository.caspar007/repository.caspar007-VERSION_NUMBER_HERE.zip`,

and paste it into the root folder. Rename the file and remove the version number!

Here is your zip file:

`https://caspar007.github.io/repository.caspar007`
