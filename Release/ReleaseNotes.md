
## AutomationML Editor Release Notes

### [Version 6.4.1.3](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.4.1) 

#### Bug Fixes
- Fixed a bug that caused an exception when an existing document that was opened when the application was started was immediately replaced by a new document.
- Fixed a bug where a missing or incorrect version number of a class or type was not reported as a recommendation violation when publishing a library.
- Fixed a bug that caused an exception when a deleted library file should be restored from the library space backup folder.

#### Changes
- Violations of the naming conventions of a class can lead to several repair requests with different causes. However, a correction now only needs to be carried out once.


### Version 6.4.1.2 

#### New Features

Several new functions have been added to the relationship view for libraries. This is intended to facilitate the traceability of dependencies for extensive library relations.  

- A new distance slider in the libraries dependencies view allows to expand and shrink the range of the related libraries of a selected library.
- The tooltip for a library node in the libraries dependencies view has been redesigned. The tooltip popup supports highlighting of related libraries, allows to extend the distance to view all related libraries, can be moved by dragging the title bar and stays open until it is closed.
- The libraries dependencies view automatically scales the content to fit if it is resized.

#### Changes
- The overview plus details pane in the library dependencies view is initially visible.

#### Bug Fixes
- Fixed a bug that caused an incorrect validation result when a class tree was duplicated.
- Duplicate entries in tooltips in the library dependencies diagram have been removed.


### Version 6.4.1.1

#### New Features
- The previously added feature to add a duplicate of the selected element to the selected sequence is now available in the context menu and via a short cut Ctrl+D.

#### Changes
- Terms of use need not to be accepted again if a new version is installed and it was accepted already for a previous version.
- The version number of the editor is now added to the error-log file entries.
- The search tools in tree views are visible in the overflow area of the tree view toolbar.
- Some visual styles in dark and light modes as in the library dependency view have been improved.
- Moving of diagram nodes in the library dependency view has been improved.
- Layouts of some dialogs as the SI-Unit dialog have been improved.


### Version 6.4.1.0

#### New Features
- A new button is added to the tree view toolBar which allows to add a duplicate of the selected element to the selected sequence.
- InternalLinks are validated if assigned category or direction constraints are violated. Violations are also visualized in the tree view.


### [Version 6.4.0.30](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.4.0) 

#### Changes
- The text editor control used for editing `AdditionalInformation` elements accepts return and tab input.
- Initial expansion of value collections in property views is redefined.
- The visualization of cardinality constraints at `ExternalInterface` elements has been modified.
- The attribute value of an attribute instance is set to the default value of the attribute type if it exists.
- The input element for editing boolean values in attribute windows is provided with 3 states, so that the assignment of zero values is also possible. 
- Attribute Table view only supports editing of Name, Value, DefaultValu, Unit and DataType. Other fields have been removed.
- The editor dialog to edit date time values of an attribute is initialized with the current date and time. 

#### Bug Fixes
- Fixed an issue where the input element for the attribute value was not adapted to the attribute datatype, when the attribute data type was changed in an attribute type.
- Fixed an issue where the attribute value editor did not accept null values.
- Some errors that prevented attributes from being edited in the table view have been fixed.

### Version 6.4.0.29

#### BugFixes
-  Fixed an issue where the undo and redo feature was disabled after a new document version was created.

### Version 6.4.0.28 

#### Changes
- Modification of the New Feature introduced in version 6.4.0.27


### Version 6.4.0.27 

#### Changes
- The restrictions on the use of the AutomationML prefix for naming libraries are less strict.
- Attributes cannot define multiple semantic references defining the same AMLID. 

#### New Features
- If a new attribute type is derived from an existing untyped attribute, other identical attributes can be found and automatically transformed into instances of the new attribute type.


### Version 6.4.0.26

#### BugFixes
- Fixed a bug, related to reference external attribute types when instances of external classes are created.
- A bug has been fixed that could affect the visibility of plugins.

#### New Features
- Edit description dialog shows the name of the modified object. 


### Version 6.4.0.25

#### BugFixes
- Fixed a bug, related to merging and redirection of references.
- Fixed a bug, that could cause an exception when restoring a backup file from the library space.


### Version 6.4.0.24

#### BugFixes
- Fixed a bug that left the main window minimized when the splash screen was closed.
- Fixed an error where a plugin update could not be installed.

### Version 6.4.0.23 

#### BugFixes
- Fixed a bug that caused a crash when opening the PluginManager.
- Fixed a bug that prevented some dialog windows from opening.
- An error where a contained class reference was not redirected when creating an instance of an external class has been fixed.


### [Version 6.4.0](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.4.0) 

#### Major Changes
- This version introduces a **new licence model** for the Editor. 
    1. As before, there is an AutomationML Editor Free version without a licence file. It contains all the basic features and functions, but with some function and model limitations.
	2. A new AutomationML Editor Plus version is available with an extended range of functions and fewer functional restrictions.
	3. The full version is the AutomationML Editor Premium version with the full range of functions without model limitations.
  
  Please note, that the feature restrictions for the free version have changed.

- The method for integrating editor plugins has been changed. Existing versions of already loaded plugins must be replaced by new versions. To do this, all plugins must be manually uninstalled and reinstalled using the editor's plugin manager. Corresponding new versions are available for the plugins offered by the AutomationML Association. Self-developed plugins must be converted to the new method. The procedure is described on the development page for plugins.
- The function for deactivating the aml file service has been removed. It is no longer possible to import AML download resources from the AML website.

#### Changes
- When a new version of a library, class or attribute type is created, the new version will keep the ID of the original version. 
- An InternalElement or ExternalInterface can be moved interactively, even if there are InternalLink relations to the moved element.  
- When an attribute type instance is created, no header data of the type is transferred to the attribute.
- When saving a document, local file paths in external references are changed to relative or absolute file urls depending on where the file is saved.
- When loading a document, it is checked whether paths in external references are redirected to new addresses. If redirected addresses exist, the external references are changed and a message is displayed in the status information.
- If an external reference to a local automationml file is inserted which is an extension, a reference is also added to the extended document.
- If an AutomationML object is created whose class is not found in a referenced library, such as when creating a group, a dialog is displayed to select the library version in which the class is defined.  
- If an edited library is a new version of a library, names and IDs of classes can only be edited, if the version is defined as a new major version.
- If a library extension is referenced and a new version of an extended library is found an upgrade option for the extended library version is not notified.
- The nameing consistency rule defined for consistent document and library names has been changed. The '.' character is allowed, i.e. to classify a domain with a sub domain. 
- The AutomationML library server has been renamed to AML library space.
- When an AttributeType is derived from a base Type, the datatype of the base type is also assigned to the derived type.
- CAEXPath characters, used to mark escape sequences in a path are omitted from class- and role- reference representations in tree views.

#### New Features
- When no document is loaded, all tree view backgrounds change to a light gray color.
- The publication consistency check results protocol provides new options for filtering results according to result type. 
- A new option in the Document References can be used to set that all externally referenced documents are always opened when opening a document.
- Additional consistency checks related to versioning rules and type references are executed when a library is published.
- Find Online Dialog and External Class Reference Dialog provide additional information about selected classes.
- The Attribute Tree View Add-Button allows to reference external attribute types.
- It is now possible to add multiple extended versions of the same library to an extension document. The method is provided in the context menue of a library tree view pane.
- New consistency rules for the naming of extension versions of libraries have been added.

#### BugFixes
- If an element is selected in the tree view which can not have assigned attributes (as for example InstanceHierarchies), the attribute view switches to an empty view.
- When a class was moved in the class tree, not all references to the class were always updated. This bug has been fixed.
- The UNDO operation for move operations had left an inconsistent model in certain cases (e.g. with master objects). This error has been fixed.
- If an InternalElement is affected by a split operation, mirror references to outsourced elements have not been changed correctly.
- The title of the Header Editor did not always display the name of the edited object. This error has been fixed. 
- If a mirror attribute is located in a different attribute tree than its master element, the target is now visualized and correctly selected when navigating to the master element via 'Goto Master'.
- Fixed some issues related to the handling of double click events on tree view items
- Fixed some issues related to the presentation of the paste dialog and the selection of options.
- In the attribute editor, when changing the selected object with attributes, the previously selected attribute was still displayed in the editor, although no attribute was selected from the newly selected object for editing. This error has been fixed.
- Fixed the editor property view of the nominal scaled constraint editor.
- Fixed an issue in the paste dialog where the optional paste properties were not visible or editable.
- Library Relation Diagram will only show related libraries of the selected type when dependency relations are not selected.
- It is allowed, to create multiple new versions of a single class or type.

