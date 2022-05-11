
## AutomationML Editor

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
