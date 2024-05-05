
## AutomationML Editor Release Notes

### [Version 6.2.4](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.2.4) 

#### Note
If your previous version is 6.1.x or older, please also read the detailed release notes for version [6.2.1](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.2.1) before installing this version.

#### Bug-Fixes
- Fixed an issue where exchange of unverified libraries raised an exception.
- Fixed an issue where derivation of an attribute type in the find online dialog failed to get the correct CaexPath.

#### Changes
- Status Message in the FindOnline Dialog is made more noticeable
- Folder location in server configuration are always editable
- FilePath of current selected server profile is shown in status line of server configuration window.

### [Version 6.2.3](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.2.3) 

#### New Features
- The 'Find class online dialog' contains a new option to define an inheritance relation between the selected class and the class found.
- The 'Find class online dialog' contains a new option to define a semantic reference when the dialog is called from a selected attribute type.
- The 'Add Reference ... dialog' contains a new option to create new versions for all libraries contained in the referenced document.
- A Semantic reference to an AutomationML attribute provides a new button/ method to lookup the attribute definition.
- It is now possible to create versions for classes and attribute types without a drag/drop operation if the containing library is already modeled as a new library version.

#### Bug-Fixes
- Fixed an issue where online search of existing classes throw an exception.
- Fixed an issue where excluded instance hierarchies are still be included in the outsource dialog.
- ExternalReference Path editor allows selection of files from local storage.
- Fixed a bug in the outsourcing dialog
- Fixed a bug in publishing dialog
- Fixed a bug in undo/redo methods when a transaction includes multiple documents
- The error that the help pages were no longer offered has been fixed.
- ExternalReferences which are no more used after outsource was successfull will be deleted.
- It is no more possible to add references to multiple versions of the same library to the same document.

#### Changes
- Attribute Types in published libraries must have a unique ID assigned
- Library dependency view needs to be activated by clicking a button to show the dependency graph.
- ExternalReferences used for version relations are distinguished from ExternalReferences used to access external model objects.
- ExternalReferences which are no more used after outsource was successfull will be deleted.
