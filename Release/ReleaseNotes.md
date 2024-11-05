
## AutomationML Editor Release Notes

### [Version 6.3.11](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.3.11) 

#### New Features
- If an extension is selected in the add reference dialog, the original document version is marked with a map marker. 

#### Changes
- Increment minor version always sets the patch version to 0.
- The version upgrade assistent has been modified. If the current file has unsafed modifications it can be saved before the upgrade. The upgraded file can be saved to a new file.
- Extenal referenced files which are local files are no longer copied to the _AMLExternalLibraries folder.
- Alias names are editable in the upgrade version dialog.
- When a new version or extension of a document is created the referenced documents in the new version are checked for updates. If old versions are referenced the upgrade dialog is showed.
- Generated Aliasnames for extensions will contain the extension text.
- An informational message in the dialog to transfer server data has been modified.

#### BugFixes
- Fixed a bug, where a SupportedRoleClass gets an invalid path reference when created from an external RoleClass
- Fixed a bug, where a Path to an external AttributeType was not marked as invalid, when it could not be resolved to an external AttributeType.
- Fixed a bug, where invalid alias names were not listed in the validation report.
- Fixed a bug, where the switch of the signature validation from off to on could raise an exception.
- Fixed a bug, where an internal link, defined in a class was not copied to a class instance.
- Fixed some issues related to instance creation, where ID references wer not updated to there corresponding instance elements.

### [Version 6.3.10](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.3.10) 

#### New Features
- The Service Configuration Dialog provides a new command button to open the profiles folder of the editor.

#### Changes
- The menu items to open external files and collection have been moved from the `File->Open` menu item to a new `File->Load` menu item.
- Increment minor version and patch version options for classes, used in the version creation dialog, also change the document and library version numbers.

#### Bug Fixes
- Fixed an issue where a modified class name was not propagated to the class children, when the children were derived from the changed class.
- Fixed an issue where the creation of an instance of an external class failed to create valid class references.
- Fixed an issue where a valid name of an attribute, shown in the header editor, was marked as invalid.
- Fixed an issue where the close button in the outsource dialog has no effect.
- Fixed an issue where the preview window for external documents could raise an exception when internal links are expanded.
- Fixed an issue where the resizing of the server administration dialog left blank spaces in its window.
- Fixed some issues with bad text colours when the dark mode is used.
- Fixed an issue, where the settings icon in the right window command button was invisible in some themes.
- Fixed an issue, where references to document versions could defined with an not unique alias name.
- Fixed an issue, where the selected dependency relation was not updated in the dependency diagram.

### Version 6.3.9

#### Changes 
- The dialog shown to upgrade an old version of a referenced external file to a new version has been modified and offers additional options. 
- The feature to automatically create an inheritance relation for child classes has been removed in release version 6.3.2. This feature has been reactivated. To use the feature, it has to be enabled in the settings.

#### New Features
- The feature to check the availability of new versions for referenced external files can be called from the Files menu, even if this option is disabled in the settings.

#### Bug Fixes
- Fixed an issue where the application of the assign reference paste method could cause an exception.


### Version 6.3.8

#### Bug Fixes
- If the size of the transfer dialog is changed, the displayed content is adjusted.
- If a document was published for which there are several unpublished previous versions, incorrect version references were created. This error has been fixed.
- An error in the recognition and display of backup files has been fixed.

#### Changes
- After the successful transfer of server data, a note on the use of the source and the redirection table is displayed.
- Before transferring server data to a new server, a warning is displayed if no anonymous read access exists for the new server. As a result, login information in the new document URLs would be readable.

#### New Features
- There is a new button on the right-hand side of the main window frame for editing and viewing the editor's configuration files.
- The publication dialog shows when a document is published as a branch version.
- The publication of versions of local documents is not permitted if a newer version of the locally saved document has already been published.

### Version 6.3.7

#### Bug Fixes
- Fixed a problem when publishing an AutomationML document where an incorrect error message was displayed regarding a disallowed file URI.
- Fixed an issue where a missing OriginID in a SourceDocumentInformation could raise an exception. All added SourceDocumentInformation get a unique OriginID as default now.
