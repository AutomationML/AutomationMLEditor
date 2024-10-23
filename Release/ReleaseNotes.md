
## AutomationML Editor Release Notes

### [Version 6.3.9](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.3.9) 

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
