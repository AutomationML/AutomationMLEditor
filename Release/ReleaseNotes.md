
## AutomationML Editor

If you have problems with the automatic update function, you can perform a manual update at any time. Use the [download link](https://github.com/AutomationML/AutomationMLEditor/releases/latest/download/Aml.Editor.zip) to do this.


### [Version 6.1.4](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.1.4) 
#### Issues Addressed in this Release

- The configuration of the context menu is corrected when the mouse cursor is positioned outside the boundaries of the selected object.
- If the *Create InternalElement* option is selected when pasting a role class into a SystemUnitClass, then the options to copy the attributes and interfaces to the InternalElement are now also displayed.
- Fixed an issue when a new external document was referenced via the *RefUri Editor* the editor crashed if the edited AutomationML document was an element of an open AML container.

### [Version 6.1.3](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.1.3) 
#### Issues Addressed in this Release

- Fixed that the application stopped responding when the InternalLink interface class selection button was pressed.
- Fixed that in the view for listing all InternalLinks of the whole document there was no reaction if no object was selected.
- Fixed a problem with entering the password in the login dialog for AutomationML members.

### [Version 6.1.2](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.1.2) 
#### Issues Addressed in this Release

- Fixed problems related to the visualization of InternalLink lines
- Fixed a problem that causes a crash when an AutomationML object was created from a class 
- Fixed a problem related to the + button to add elements when 2 clicks are needed to create the first element 
- InternalLink elements can now no longer be added via the context menu of a SystemUnitClass or InternalElement, but via the context menu of an ExternalInterface element. A dialog is opened for configuring the InternalLink.  This is an alternative to the graphical creation of an InternalLink element [(see this video on youtube](https://youtu.be/watch?v=i85Fxg8VYz0)).
- Added support for Aml.Editor.API version 2.0.1

### [Version 6.1.1](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.1.1) 
#### Issues Addressed in this Release

- Internal link connection lines could not be displayed for large distances between the interfaces,
since the position of the start and end points no longer exist for the calculation of the line coordinates.
Now the line coordinates are approximated and all connecting lines are always represented. The position of the lines
can shift however when scrolling the window contents.
- Cardinality violations for InternalLinks are now checked in the document
validation.
- If the cardinality of an ExternalInterface is changed, the display is updated now. 

### [Version 6.1.0](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.1.0) 
#### Issues Addressed in this Release

- Loading documents could take a very long time if the document references libraries that are not included in the document itself and have a lot of references on it.  The loading time has now been improved.
- A new offline mode (without internet connection) can be configured in the settings. In offline mode, libraries and models cannot be loaded from the AutomationML website. Some services that require access to the AutomationML cloud are also not available.
This mode has been added to enable the usage of the AutomationML editor for people and organizations who are not allowed to use software, which silently use internet connections. The offline mode is **not set** by default.
- The .NET 5.0 runtime has reached end of support on May 10, 2022. Microsoft will no longer provide servicing updates, including security fixes or technical support, for .NET 5.0. 
Therefore, new versions of the editor including this version are offered for the .NET 6.0 runtime only due to security considerations.
- Selecting an object with attributes automatically selects the first attribute in the Attributes view. This feature has been disabled now because this could cause problems when editing the objects header attributes.
- Saving an aml document to a container could raise an exception in some situations. This is fixed.
- Foreground colour of description area changed to a white brush when colour theme is set to a dark mode.
- Adding a show clear text button to password box in AML Login

### [Version 6.0.5](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.0.5)
#### Issues Addressed in this Release

- A new feature to support name validation has been added to the document validation service.
- A problem related to systems with English language locale is fixed.
- A .Net 6 version is available on request. The publicly distributed version is still based on .Net 5.


### [Version 6.0.4](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.0.4)
#### Issues Addressed in this Release

- The License Dialog provides a new option for the distribution of license files.
- InternalLink Line drawings respond to UI Scaling, this can avoid some visualization problems showing link lines.
- An *Open Backupfolder* - button has been added to the backup file selection dialog.
- Menu items in the context menu of tree nodes are regrouped and rearranged. 
- The Visual layout of *Attribute Tables* has been improved.
- The performance of *attribute view switching* has been improved.
- Property Description Area allows scrolling of content.
- All ***Header*** definitions of all CAEX Objects can now be edited
	- ***Constraint-Header*** (editor is started from *constraint context menu*)
	- ***RefSemantic-Header*** (editor is started from *refsemantic context menu)*
	- ***Revision-Header*** (editor is started from *revision context menu*)
	- ***ExternalReference-Header*** (editor is started from *externalreference context menu*)
	- ***CAEXFile-Header*** (editor is active when no other object is selected)
	- ***InternalLink-Header*** (editor is active, when a link line is selected)
	
- A **new Editor Update feature** and installation procedure is implemented. Future updates will no longer be published as msi-installer files. This version of the editor comes with a new embedded update feature. The next version update will be published as a self contained zip file and does not require an installer.  This version is the last version, published with an installer. You will be notified with a new update dialog, when an update is available. There are options to skip a version or to postpone the update to a later time.


### Version 6.0.3 (service release)

#### Issues Addressed in this Release

- Plugin developers can now use the [Aml.Editor.API package](https://www.nuget.org/packages/Aml.Editor.API/). This allows plugins to directly call methods of the editor even outside the classes instantiated by the editor through Composition. 
- Fixed some presentation problems related to UI command icons

### Version 6.0.2 (service release)

#### Issues Addressed in this Release

- Adaption to the new Plug-in API v3.0.5
- Capture Dialog will now copy the captured image to the clipboard while the dialogue is still open

### Version 6.0 (release scheduled for may 2022)

#### Issues Addressed in this Release

- This version requires a license to be able to use all features. Licenses for AutomationML members are provided by 
the AutomationML association. The Editor displays a dialogue for including a valid license when the menu item *Information.Registration/Licensing* is selected. 
License files are saved in the *%AppData%/AutomationMLEditor/License* folder. For a direct download of a license file, 
provided for AutomationML members, a valid account for the AutomationML cloud is needed.
- PlugIn loading mechanism changed to use the new Nuget v3 interface. PlugIns need to be updated to be compatible with this version..
- The editor will be installed with no additional PlugIns. PlugIns have to be installed using the PlugIn Manager.
- In AutomationML 2.10 documents the usage of the Standard "CARDIANALITY"-Attribute Type is supported. The modelled multiplicity of
Internal Links can be visualized and will be checked.
- In Mirror Elements the complete object tree of the referenced master element can be visualized and edited.
- AutomationML Documents, received from official AutomationML resources contain signed libraries. The validity of a signature is
marked at the library tree node. Signed libraries are not editable unless the protection mode is disabled.
- AutomationML libraries which are marked with an invalid signature can be exchanged with signed and valid versions.
- The Insertion of Mirror Elements is restricted to provide reference recursions and reference cycles.
- New Paste Action Option 'Append Derivation' added for classes
- New Paste Action Option 'Replace with new instance' added for InternalElement Targets and SystemUnitClass Source 
- New Paste Action Option 'Assign Reference' added for Instance Targets and Class Source (InternalElement, SystemUnitClass), 
(ExternalInterface, InterfaceClass) and (Attribute, AttributeType).
- New Paste Action Option 'Update Instance' added for Instance Targets and Class Source (InternalElement, SystemUnitClass), 
(ExternalInterface, InterfaceClass), (RoleRequirement, RoleClass) and (Attribute, AttributeType).
- Update Instance method added to context menu of instances and classes. 
- Capture window has new arranged capture buttons.
- ExternalDataReferences to Images using the correct MimeType are visualized using the linked external image when the linked image exists.
- The UI has been modernized and supports a new dark theme. 
- Highlight of active Selections are only visible in currently active views.
- New AutoSave mode option (set by default) added. When set, a backup of the current open document is automatically saved every minute.
- New Document Method provides options to create empty documents or documents containing libraries.
- New Document Method added as toolbar button.
- Inherited Attributes are visualized as read-only items in tabular edit mode

- **The Version 6.0 needs the .NET 5.0 runtime.**

#### Bug Fixes in this release
- Fixed an issue in the management of path references which could raise an unhandled exception. This could happen, for example, if existing libraries referencing other classes 
were overwritten during import (old version deleted and new version inserted).
- Paste Dialog Window opens correctly at the current mouse position on multiple screen configurations.
- Selection Feedback for InternalLink lines are updated correctly if a connection end is moved.
- Special Editor windows as Facet Editor and Role Instantiation window display a scroll bar when the items list doesn't fit to the screen.
- Fixed some issues related to external references to AMLContainer parts and reassignment of uri addresses to container parts.

#### Note to PlugIn developers
- With the introduction of version 6.0, only plugIns that support at least .NET 5.0 are supported. 



### Version 5.6.11 (latest release without restrictions when used without a license)

### Issues Addressed in this Service Release

- Runtime version changed to .NET Framework 4.8
- Update to last version of Aml.Engine
- Fixed an issue in the management of path references which could raise an unhandled exception. This could happen, for example, if existing libraries referencing other classes 
were overwritten during import (old version deleted and new version inserted).

### Version 5.6.10

#### Issues Addressed in this Release

- New method **Copy CAEX object ID** in context menu of tree nodes allows to copy the CAEX object ID.
- Move and Copy paste actions are defined now also for Role references (SupportedRoleClass and RoleRequirements).
- New feature in reference navigation dialogue allows to navigate forward and backward.
- New feature in paste dialogue allows to apply the paste action without closing the dialogue and to proceed with another selected target.
- New search option **Attribute value** in tree search allows to search for elements with a specific attribute value.
- Additional button in tree search control allows to reduce or enlarge the tree to display the search result.
- New navigation buttons are shown in a new pop-up window at the bottom of the search dialogue when a text is entered in the search field, F3 and shift+F3 are supported.
- The search range is defined by the selected element in a tree view, the current range is labelled in the pop up window.
- New method **Goto referenced CAEX object** added to attribute context menu if the attribute datatype is defined as **xs:IDREF** and the value is a valid CAEX object ID.


### Version 5.6.9

#### Issues Addressed in this Release

- Fixed an issue in the edit group dialogue which throws an exception when an InternalElement was added to the group
- Fixed a bug when Editor crashes on start-up if configure file setting ResolveExternalReferences is set to True.


### Version 5.6.8

#### Issues Addressed in this Release

- Fallback method added when download of WEB Resources failed.


### Version 5.6.7

#### Issues Addressed in this Release

- Adaption to new AutomationML corporate design
- Enable reload of WEB Resources when Web connection fails [(Related Information)](https://github.com/AutomationML/AutomationMLEditor/wiki/WebResources/).

### Version 5.6.6

#### Issues Addressed in this Release

- Allowing to add "Sub Attributes" of AttributeTypes using the '+' button.
- Allowing to edit "Sub Attributes" of AttributeTypes when they are selected in the library tree view.

### Version 5.6.5

#### Issues Addressed in this Release

- Library import from AutomationML provides new items
- The included AutomationML Standard libraries Edition 2.1 
  have been exchanged for the versions offered on the AutomationML site. Please be aware, that the AutomationML Standard AttributeTypeLib has been updated. 
  A minor deviation from the standard attribute type library published in the IEC 62714 standard is now fixed.
- Layout Improvements in Start Page
- Layout Improvements in Import Libraries Dialog
- Collapse All for expanded tree views added

### Version 5.6.4

#### Issues Addressed in this Release

- Fixed an issue where navigation to a base class raised an exception when the class reference could not be resolved to an existing class.
- A new option **Resolve External References** allows references to classes in external documents to be taken into account when creating instances and visualizing inheritance.
- Fixed an issue where visualising inherited attributes does not show any items.
- Reversion of version 5.6.3 due to an update error where menu entries are disabled.

### Version 5.6.2

#### Issues Addressed in this Release
- Fixed an issue where loading an AML file would fail with a double click from the explorer window.
- A new option 'Settings-Resolve External References' allows references to classes in external documents to be taken into account when creating instances and visualizing inheritance relations.

### Version 5.6.1

#### Changes

When an AutomationML container is opened and modified, the Editor doesn't operate on the original source but on a
backup copy of the container file. The original container file will only be modified if the edited content is saved.

### Version 5.6.0

#### Bug Fixes

- Fixed an exception in AML Editor 5.5.3 when exchanging root document in AMLContainer.
- Fixed an issue, when trying to add an AML file as “additional Content”. One could select
in the next dialogue that this is a “library”. But then the tool refuses to add the file with some strange error message.
- It is possible now to edit the URL of a content part (like /sub/content.aml) to place content in a subfolder of a container.

#### Changes

- The folder browser dialog has been exchanged.
