# Release Notes

This is the version history with some release notes.

## Version 1.3.4: Media Library

_Release date: 07.04.2020_

Version 1.3.4 introduces a new media-library for images and files.

The release includes:

* Media: A brand new media library that can be opened when working with images or files in the content page.
* Media: Completely refactored the image model.
* Media: A new upload component for download-files in the visual editor.
* Media: You can upload a logo for your website in the settings now and use it in your theme.
* Media: You can upload a favicon now and use it in your theme.
* List Pages: You can now list pages for each folder in frontend with the new twig-tag `getPageList(navigation, path-to-folder, base_url)`
* Fix: Hopefully fixed a super annoying bug where the wrong content opens in a block. Should be fixed by disabling drag&drop for blocks if they are opened and a wrong logic when publishing image-blocks.
* Themes: Published the [emergency theme](https://themes.typemill.net/emergency) some days ago.

## Version 1.3.3: Pages and Posts

_Release date: 27.02.2020_

Version 1.3.3 introduces posts for news- or blogs-sections. Please update the system folder.

The release includes:

* Posts: You can change the content of a folder from pages to posts now. Posts are sorted by date (manual date or created at) in descending order. Typemill will even change and rewrite the existing content within a folder. Pretty awesome!!!
* Navigation: The file name and the name in the navigation are completely decoupled now, which means you can use special characters like in french language for navigation titles now.
* Themes: There is a brand new knowledge theme!!!
* Fix: Problem with & in title is fixed now.
* Fix: Duplicate files and folders are checked now.
* Fix: Folders with published pages cannot be deleted anymore.
* Fix: Introduced field-attribute "fieldsize" with values "full", "half" and "quarter" for a better field layout (e.g. theme-settings).

## Version 1.3.2: Rename and hide navigation

_Release date: 21.01.2020_

Version 1.3.2 improves the meta-information again and enables authors to rename and hide items in the navigation. Please update the system folder and the theme folder.

The release includes:

* Internationalization: JavaScript strings are now translated (vue.js).
* Meta: Rename navigation items. This required a lot of new logic and a static file structure-extended.yaml in cache folder.
* Meta: Hide item from public navigation (note, that it is only hidden from main-navigation, not from sub-navigation)
* Meta: Filter the active meta-information for each page, so that no metas from disabled plugins are visible.
* Themes: You can add fields to the standard-meta-tab with the themes yaml-file now.
* Themes: You can now add your own CSS to each theme. Very handy to individualize a theme while keeping it updated.
* Themes: Added a dev-theme to the theme-directory as a starting point for frontend-developers.

## Version 1.3.1: Improved Meta and Internationalization

_Release date: 09.01.2020_

Version 1.3.1 improves the meta-information. Please update the system folder and the theme folder. Version 1.3.1 was updated again in the evening of 09.01.2020 with internationalization.

The release includes:

* Internationalization: Select italian or english language for the author dashboard.
* Meta: Meta-tabs are added to raw mode now.
* Meta: Create new meta-tabs with a plugin (read the docs for details).
* Meta: All field-types are implemented for meta-tabs now (with some limitations).
* Meta: Created date is added as standard meta.
* Meta: Select a manual date for the article.
* Meta: New logic for author field is implemented (account name of the logged in user with a fall back)
* User: You can add a first and last name that can be used in themes for the author name.
* UX: Configuration forms for plugins are not validated in frontend anymore. Required fields are only validated if plugin is activated.
* Bug: Folder-scan is improved so that it does not render an empty list-item for an unpublished folder.
* Documentation is updated and forms are described in a separate chapter.

## Version 1.3.0: Meta Information

_Release date: 01.01.2020_

Version 1.3.0 introduces meta-information for pages. As of version 1.3.0 Typemill will be delivered without plugins. You can download plugins and themes from the new plugin and theme-pages.

The release includes:

* Pages have meta information like title, description and author now.
* Pages can be created in base folder now.
* Changed standard content for new pages (title instead off "add title")
* New theme download page https://themes.typemill.net
* New plugin download page https://plugins.typemill.net
* Updated Typemill Theme (cover page will display the title of the content page instead of the typemill title now)
* New theme "learn" (ported from GRAV CMS)
* New theme "personal".
* Cookie-consent plugin is deleted (not dgpr-compatible).
* New GitHub repository https://github.com/typemill-resources for plugins and themes

## Version 1.2.19: Modular Editor

_Release date: 24.11.2019_

This is the final 1.2.X release and it has some implication on your website. First of all you have to update the 

* The system folder
* The theme typemill
* The math plugin

In version 1.2.19 the settings for the startpage (display as special cover page) has been moved from system settings to the theme settings. To restore the startpage design, go to settings, themes and open the typemill theme-settings. There you can activate the option "special design for startpage" again.

This release also includes:

* Visual Editor: Activate and deactivate each format button in the system settings.
* Visual Editor: The editor is now modular and can be extended by components and plugins.
* Plugins: The math plugin is the first plugin that extends the visual editor now.
* System: Moved cover page settings from system to theme settings
* Themes: Adjusted typemill to the new theme settings.
* System: Switched from font-icons (fontello) to svg-icons (icomoon).
* Themes: Ported the learn-theme from GRAV to Typemill (not published yet).
* Fix: Themes can be changed now again.
* Fix: Default theme settings are loaded now if system has not been setup yet.
* Fix: Long inline code has line breaks now and does not destroy mobile view.
* Fix: Redirect to the correct editor mode after login

## Version 1.2.18: Discard Changes

_Release date: 11.11.2019_

This release includes:

* Visual Editor: Discard changes and set page back to published version.
* Visual Editor: Inline formats for links and inline math.
* Visual Editor: Decouple markdown/component detection.
* Fix: mod_rewrite is not checked anymore.

## Version 1.2.17: Inline Formats

_Release date: 03.11.2019_

This release includes:

* Visual Editor: Format text as strong, emphasis or inline code.
* Fix: Copyright and year are stored in settings now.
* Fix: Error message when author deletes a folder with a folder in it.
* Fix: Logout user if he deletes his own account.
* Enhancement: Added more system checks for system setup.
* Enhancement: Added cypress-tests for theme options.

## Version 1.2.16: Footnotes and Search

_Release date: 22.10.2019_

This release includes:

* Visual Editor: Footnotes are now included and editable
* Events: Added events for publish, depublish, delete and sort a page.
* Themes: Added Axios (ajax calls) as an asset that can be activated for themes.
* Themes: Added Tachyons (atomic CSS library) as an asset that can be activated for themes.
* Themes: Added a simple widgetized zone for a theme that can be used by plugins.
* Plugin: Added a search plugin.

You should update the system and the theme.

## Version 1.2.15: Math Refactored

_Release date: 05.06.2019_

This release includes:

* Visual editor: A new math component.
* Parsedown: Changed syntax for math (see below).
* Navigation: Introduced status modified.
* Navigation: Change color of item on the fly according to status: published (green), modified (orange), not published (red).
* Navigation: Fixed homepage item, so that status and active is visible.
* Settings: Whitelisted settings in settings.yaml, so no pathes are stored (produced error when moved typemill to other folder). 
* Login: Changed color of link.
* Videos: refactored video embed script and changed link to youtube-nocookie.com.
* Testing: Added cypress tests for system settings.

The syntax for math changed, so the old backtipp-syntax for inline math and display math is not valid anymore. The new syntax is compatible to pandoc and many other systems. Check the details on the markdown test page: https://typemill.net/info/markdown-test 

## Version 1.2.14: Magic Table of Contents

_Release date: 18.05.2019_

This release includes:

* Visual editor: New Table of Contents component that updates on the fly.
* Visual editor: Fixed some html errors.
* Design: The admin area got a facelift, switched to green instead of red.
* Improved some stuff in background to show status of pages in admin (edited/published)
* Login: Saves timestamp of last login now
* Login: Added hint to bookmark the login page
* Errors: Added error reporting, so that no errors are displayed by default. Use DisplayErrorDetails: true to switch on.
* Created a new multi-step build script to improve deployment.
* First automated tests with cypress.io.

## Version 1.2.13: Definition lists and horizontal lines

_Release date: 04.05.2019_

This release includes:

* Visual editor: A new component for defintion lists.
* Visual editor: A new component for horizontal lines.
* Visual editor: Improved headline component
* Visual editor: some design fixes for components (borders)
* Visual editor: removed initial overlay on pageload
* Visual editor: fixed bug with wrong data after drag & drop
* Visual editor: refactored drag & drop for content blocks
* Refactored definition lists in backend code
* Fixed error with update notice
* updated all javascript libraries
* created a new landing page for typemill.net

## Version 1.2.12: Content Blocks Everywhere

_Release date: 13.04.2019_

The visual editor was a bit limited till now: You could only add new content blocks at the end of the page and after that move the paragraph via drag and drop to the right spot. With version 1.2.12 we eliminated this important limitation and now you can add new content blocks everywhere!!! All changes of this version:

* Visual editor: Add content blocks everywhere.
* Visual editor: Adjusted to vue logic, html- and markdown-content is loaded as JSON and bound to the DOM.
* Visual editor: improved design.
* min- and max-attributes are added to field-builder
* The TYPEMILL-documentation is now a public github-repository: https://github.com/typemill/docs/

## Version 1.2.11: Table Component

_Release date: 19.02.2019_

Version 1.2.11 introduces an table component for the visual editor. Please update the system folder and the theme folder. These are all changes:

* A component for tables.
* Optimized list component (recognizes `-` and `+` as list-symbols now)
* Error messages in editor are improved now
* Plugin load system has been improved
* Theme has an edit button for github now
* Theme has option to show chapter numbers in navigation now.
* New E-Mail plugin (not published yet). 

## Version 1.2.10: New Editor Components

_Release date: 26.01.2019_

Many new content components are shipped for the visual editor with Version 1.2.10, among them:

* A component for headlines.
* A component for code-blocks.
* A component for quotes.
* A component for ordered lists.
* A component for unordered lists.
* All components have the same design with icons now.
* All components have a load spinner when saving content now.
* The size for new text-components is fixed now.

There are some other fixes and improvements like:

* Preview link to page is added to the publish controller
* Error with transparent pngs is fixed, but you cannot add a height attribute for images in plugins now.
* Navigation items and titles follow the file-naming now and are not uppercased automatically anymore. You have to change you change your file-names if you want to uppercase anything.
* Error with footnote-links is fixed, but you cannot use footnotes in visual mode for now.
* Attributes like width for images are working now, but you can only add them with raw mode right now.
* When user tries to store content but is logged out, an error message pops up.
* Error while parsing markdown blockquotes if fixed.
* Modal windows for delete users is fixed
* Google reCaptcha is added for public forms.
* Security when user updates settings is improved (origin checked).
* htaccess is extended a bit.
* some other minor fixes...

## Version 1.2.9: Add Videos and Public Forms

_Release date: 03.01.2019_

With Version 1.2.9 authors can add videos from YouTube to the visual editor. The version also introduces public forms in the frontend (undocumented right now).

* Add YouTube videos with a simple link to the visual editor. More options like vimeo will follow.
* Create frontend forms like contact forms. This is experimental and undocumented right now.
* Fixed table of contents (absolute links and base url).
* Fixed some usability problems with visual editor (data got lost when clicked twice on input fields).
* Fixed bug with resize of text-fields when writing.
* plugin for contact form (not published right now).
* plugin for job-listings (not published right now).

## Version 1.2.8: Image Management

_Release date: 04.12.2018_

With Version 1.2.8 authors can upload images to the visual editor in a WYSIWYG-Mode.

* Upload, edit or remove images in the visual editor.
* Edit image alternative, image title, image caption and image link.
* Open and close block for editing with one click.
* added back-link to login-screen

## Version 1.2.7: Reorder Content Blocks

_Release date: 10.11.2018_

Version 1.2.7 enables authors to reorder content blocks in the visual editor with drag & drop.

* Reorder content blocks with drag & drop.
* New template tag `markdown()` to render markdown content in themes.
* Fixed bug with headline when delete content in the visual editor.
* Added missing image in the html-meta (first image).
* New startpage for the typemill documentation website.

## Version 1.2.6: Visual Editor

_Release date: 30.10.2018_

Version 1.2.6 introduces a visual editor as an alternative mode to the raw markdown editor. The visual editor is experimental and works with markdown blocks.

* Switch between the visual editor and the raw editor
* Edit existing markdown blocks
* Add new markdown-blocks
* Delete a block
* change default editor mode in the system settings.

## Version 1.2.5: Create New Pages Online

_Release date: 07.10.2018_

Version 1.2.5 is a simple system update, so you only have to delete the system folder and upload the new system folder of version 1.2.5. The main changes are:

* Create new folders and files.
* Mark drafted and unpublished pages in navigation.
* Add internal 404 page for the author panel.
* Improve delete pages (redirect and subfolder).

## Version 1.2.4: Refactoring and Browser Support

_Release date: 22.09.2018_

Version 1.2.4 is a small update with some improvements like browser-support and optimizing some themes and plugins, so please update the system folder, the plugin folder and the theme folder.

- Tested and optimized the admin panel with Firefox, Chrome, Edge and IE11.
- Add an individual info-link for the cookieconsent plugin.
- Redesigned and enhanced author info, share-links and date for standard theme.
- Fixed: Get error message if session is out when saving changes in the editor.
- Fixed: Get error message if try to move a page with unsafed changes.
- Fixed: Optimized logic if moved file with live, draft or json version.
- Fixed: Saves changes first before page is unpublished.

## Version 1.2.3: Reorder Pages

_Release date: 14.09.2018_

**Important: Upgrade to PHP 7**: With version 1.2.3 TYPEMILL requires PHP Version 7.0 or higher. This is due to a library (CSRF-protection), that uses a PHP7 function that is not supported by PHP 5.6. PHP 5.6 and PHP 7.0 will run out of life cycle in december 2018, so you should upgrade your server to PHP 7.1 or PHP 7.2 anyway. 

Wow!! More than six weeks and only one feature: As of version 1.2.3 you can re-order your existing content. To do so, simply drag&drop the items in the new navigation of the author panel. It looks so easy, but it was so complex in the background!!

Follow the instruction for simple updates in the [documentation](/gettings-started/update) and simply update the `system` folder.

Be aware, that all existing content-files will be renamed if you reorder a file, because we add a new order-prefix to the file name. And be aware of some rules and limitations:

* You can move files to any other folder.
* Only folders are allowed at the first level.
* Folders can be reordered within the same level.
* But a folder can not be moved to another folder or another level.

Here is the reason for the last restriction: If you move a folder to another folder, then the adress (url) will change for the whole folder and all its content (pages). It is a nightmare for your readers and for google.

If you really want to reorder your content completely, then you have to do it on the file system for now. In version 2.3.5 you will be able to create new folders and files in the author system, so you can create a new folder and move all files to the new folder manually.

## Version 1.2.2: Draft Management

_Release date: 24.07.2018_

Version 1.2.2 introduces a draft management. Follow the instruction for simple updates in the [documentation](/gettings-started/update), so update the `system` folder and please also update the theme `typemill`.

The changes are:

- Safe a draft.
- Publish a page.
- Depublish a page.
- Delete a page.
- All buttons for editing are fixed at the bottom of the page now.
- Created a new shared contentController for the whole page management.
- Extended the content-api with update, depublish and delete functionalities.
- Converted markdown to json for edit- and draft-management (stored as txt).
- Extended the vue-js for the editor.

## Version 1.2.1: Improved editor and fixes

_Release date: 06.07.2018_

** Version 1.2.1 has an important security-update, so please switch to version 1.2.1 asap. Follow the instruction for simple updates**  in the [documentation](/gettings-started/update), so update the `system` folder and please also update the theme `typemill`.

The changes are:

* Fixed soft linebreaks in markdown. Now you can add two spaces at the end of a line and you will get a soft linebreak with `<br/>`.
* Fixed navigation-error. The navigation will work now if the content starts with multiple nested folders.
* Links on startpage are now displayed correctly.
* You can now position your images with three classes `.left`, `.right`, `.middle`. Check the markdown test in the documentation for more info and examples.
* Added markdown example for linked image in documentation.
* Maximum lenght of title in editor is now 100 characters instead of 40.
* All redirects to the author panel go to content now instead of settings.
* Added error message, if file is not writable.
* Added csrf-check and more security to the content-api.
* Massively improved vue-code for the editor. Now it is vue.js logic and not vanilla script.
* Massivley reduced and cleaned up custom code for parsedown-extension.

## Version 1.2.0: Introducing a Basic Content Editor

_Release date: 25.06.2018_

**Please follow the instruction for simple updates**  in the [documentation](/gettings-started/update), so simply update the `system` folder.

Version 1.2.0 introduces a very basic content editor and is a major milestone for the developement of TYPEMILL as a full CMS. With the editor, the author can only edit existing content with markdown syntax right now. It is not possible to delete content or to create new content. These features will be added very soon.

There are quite a lot of changes in the background:

* IMPORTANT: HTML and other code is now completely disabled. All code is disallowed in the content editor and all code-syntax will be escaped in the frontend. You can use markdown syntax for fenced code blocks and for inline code to display code-examples on pages.
* Vue.js is added.
* A content navigation is added.
* Save functionality is added with ajax.
* API-routes are added for managing content.
* The content of the editor is validated (might cause problems with lot of code-syntax).
* Errors are displayed in frontend.
* Appropriate server status is send.
* The twig-cache is disabled again. It might become an optional feature in future.
* URL for xml-sitemap is displayed correctly now.

## Version 1.1.7: Improved Session Management

_Release date: 04.06.2018_

**Please follow the instructions for simple updates** in the [documentation](/gettings-started/update). Please also update the Typemill theme.

- URL to google sitemap is not displayed in settings.
- Session Cookies are only set when authentication is required.
- Added security headers for content security policy, refferers, strict transport.

## Version 1.1.6: Refactoring

_Release date: 22.05.2018_

**Please follow the instructions for minor updates** in the [documentation](/gettings-started/update). Please also update the Typemill theme and the plugins.

* Added security headers.
* Added a temporary ip-blocker if login fails 3 times.

- Added fieldsets for configuration fields of themes and plugins.
- Added logic for user roles.
- Changed url-structure from `tm-author` to `tm`.
- Activated twig cache.
- Started to refactored css for author panel.

## Version 1.1.5: Typemill Learns Math

_Release date: 10.05.2018_

**Please follow the instructions for minor updates** in the [documentation](/gettings-started/update). Please also update the Typemill theme and the plugins.

With version 1.1.5 Typemill learns math. There is a plugin called "math" that you can activate in the author panel. you can choose between MathJax and KaTeX. For the syntax to write math in markdown, please check the [markdown reference page](/info/markdown-test). Here are the details of this version:

* Extend markdown to support latex syntax.
* New plugin to activate MathJax or KaTeX.
* Highlight for code blocks is now a plugin.
* Share buttons for twitter, facebook and xing can be added to the TYPEMILL theme.
* Optimized mobile startpage.
* Table of content has now permanent ids and anchors (headline) instead of dynamic numbers. 

## Version 1.1.4: Refactoring

_Release date:  (30.04.2018)_

**Please follow the instructions for minor updates** in the [documentation](/gettings-started/update). Please update the Typemill theme, too.

Version 1.1.4 is mainly an optimization and refactoring of the author panel released in version 1.1.3. Some details of the changes:

* Length of description is optimized for SEO now.
* You can display a last modified date on each page now (update the TYPEMILL theme for that).
* Optimized mobile version of the author-panel navigation.
* Form rendering is now done in a seperate form template.
* SettingsController is deeply refactored and some bugs are fixed.
* FormModel partly fixed and refactored.
* ValidationModel fixed.
* Update notifications for system, themes and plugins are completely refactored and unified.
* Welcome page is fixed, so that the linked themes- and plugin settings show the initial values now.
* Settings functions for plugins and themes are cleaned up and unified.
* Design is partly fixed and unified (open-close icons and more).
* User documentation has been enhanced and corrected.

## Version 1.1.3: The Author Panel

_Release date:  19.04.2018_

**Please follow the instructions for major updates** in the [documentation](/gettings-started/update).

Version 1.1.3 introduces an author panel. Now you can authenticate, configure the system, themes and plugins and manage users. This is the first step towards a full authoring panel that helps you to manage, create and edit everything online.

* Author panel.
* Authentication.
* Configuration of the system, the theme and the plugins.
* User management (create update and deleted).
* Bugfix: Footnotes in Markdown didn't work due to parsedown library. Fixed in the new library version.

## Version 1.1.2: Improved Setup

_Release Date:  15.03.2018_

With version 1.1.2 we added the possibility to configure the theme in the setup a bit more. We also fixed a bug in the htaccess. So next to the "system"-folder, you should also update the theme-folder and the htaccess-file. As always, backup your settings.yaml-file, then delete it and setup your website again (visit /setup).

* Added configurations for themes in the setup.
* Improved update check for themes, plugins and base app.
* optimized design of setup.
* Added language selection to setup (used only for lang-attribute right now).
* Updated typemill theme accordingly
* Bugfix: Index.php is not reachable anymore, prevents duplicate content. Please update htaccess-file. 

## Version 1.1.1: Refactoring

_Release date: 25.02.2018_

Version 1.1.1 is mainly an improvement and some refactoring for the plugin release.

* Added new plugin "analytics" for integration of Matomo/Piwik and Google Analytics.
* Theme "TYPEMILL": Design refresh.
* Theme "TYPEMILL": Added cannonical url.
* Theme "TYPEMILL": Added meta tags for social sharing including image reference.
* Increased length of meta-description for google.
* Fixed error with field builder (getAttributeValues).
* Fixed error with static functions in settings (added declaration as static).
* Added documentation for plugin developers.

## Version 1.1.0: Introduce Plugins

_Release date: 05.02.2018_

Version 1.1.0 introduces plugins to typemill. And because of the GDPR, the first plugin is an implementation of the famous cookieconsent. So heads up, you can publish GDPR-compliant websites with typemill now! 

All plugins are in the "plugin"-folder, and I can't wait, that this folder will be stuffed with cool extensions.

To update the system, please delete, replace and upload

* the "system" folder and
* the "theme" folder.
* the "plugin" folder (new).

Then backup and delete your settings.yaml in the settings-folder. 

Now visit your startpage and click on the new setup-button. The button will direct you to the new setup page, where you can configure the basic system and the new cookieconsent-plugin.

Plugins are easy to use for writers, but a plugin system is pretty complex to implement for a developer, so there is a lot of new code. For now, there is no documentation for developers, but it will follow, soon.

Also introduced with 1.1.0 :

* Field Builder
* CSRF-Protection
* Input Validation
* Version Check for Plugins, Themes and Core-System
* Simple Asset Manager
* Twig Extensions

## Version 1.0.5: Table of Contents

_Release date:  30.11.2017_

- Improvement: Character encoding for the navigation has improved. You can try to use other characters than english for your file names now, but there is no garanty for it. If the characters do not work in the navigation, please use english characters only.
- Improvement: A [TOC]-tag for generating a table of contents is now implemented. You can use the tag anywhere in your text-files, but please use a separate line for it. Update the theme for stylings.

## Version 1.0.4: Bugfixes

_Release date:  17.11.2017_

- Bugfix: Settings file was generated after a page refresh, this is fixed now.
- Improvement: Cleaned up the load and merge process for settings, managed in a new static class now.

## Version 1.0.3: Getting Slim

_Release date:  14.11.2017_

Main improvement is a litte build process, that strips out all developer related files and reduces the size of typemill dramatically from 2.5 MB to less then 1 MB (gzipped).

- Bugfix: Deleted a config-file in the download-version, that broke the setup url.
- Improvement: Meta-title is now created with the first h1-headline in the content file. File-name is used as fall back. **Please update the theme-folder with the theme-folder of version 1.0.3!!!** This will improve SEO.
- Improvement: Stripped out all developer files in the download-version. This reduced the size of the zip-download from 2.5 MB to 800kb.
- Improvement: Changed Namespace from "System" to "Typemill".

## Version 1.0.2: Bugfix

_Release date:  02.07.2017_

- Bugfix: The theme can now be changed in the yaml-file again.

## Version 1.0.1: Google Sitemap

_Release date: 01.05.2017_

- Bugfix: Index file in the content folder won't break the building of the navigation tree anymore. 
- New Feature: Added a google sitemap.xml in the cache folder.
- New Feature: Added a version check, an update message can be displayed in theme now.

## Version 1.0.0: Hello TYPEMILL!
_Release date:  13.04.2017_

The first alpha version of typemill with all basic features for a simple website:

- **Content** with Markdown files and folders
- **Settings** with YAML and a setup page
- **Themes** with Twig and six theme variables
  - {{ content }}
  - {{ description }}
  - {{ item }}
  - {{ breadcrumb }}
  - {{ navigation }}
  - {{ settings }}

