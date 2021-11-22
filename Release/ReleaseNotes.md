## AutomationML Editor


### Version 5.6.6

### Issues Addressed in this Release

- Allowing to add "Sub Attributes" of AttributeTypes using the '+' button.
- Allowing to edit "Sub Attributes" of AttributeTypes when they are selected in the library treeview.

### Version 5.6.5

### Issues Addressed in this Release

- Library import from AutomationML provides new items
- The included AutomationML Standard libraries Edition 2.10 have been exchanged for the versions offered on the AutomationML site.
  Please be aware, that the AutomationML Standard AttributeTypeLib has been updated.
- Layout Improvements in Start Page
- Layout Improvements in Import Libraries Dialog
- **Collapse All** method for expanded tree views added

### Version 5.6.4

### Issues Addressed in this Release
- Fixed an issue where navigation to a base class raised an exception when the class reference could not be resolved to an existing class.
- A new option **Resolve External References** allows references to classes in external documents to be taken into account when creating instances and visualizing inheritance.
- Fixed an issue where visualising inherited attributes does not show any items.


### Version 5.6.2

#### Issues Addressed in this Release
- Fixed an issue where loading an AML file would fail with a double click from the explorer window.



### Version 5.6.1

- When an AutomationML container is opened and modified, the Editor doesn't operate on the original source but on a
backup copy of the container file. The original container file will only be modified if the edited content is saved.

- This version uses the Aml.Engine v1.6.4 and Aml.Plugin.Contract v2.5.0.

### Version 5.6.0

##### Bug Fixes

- Fixed an exception in AML Editor 5.5.3 when exchanging root document in AMLContainer.
- Fixed an issue, when trying to add an AML file as “additional Content”. One could select
in the next dialog that this is a “library”. But then the tool refuses to add the file with some strange error message.
- It is possible now to edit the URL of a content part (like /sub/content.aml) to place content in a subfolder of a container.

##### Changes

- The folder browser dialog has been exchanged.


##### Updates
- AutomationML editor uses **Aml.Engine v1.6.2**
 

### Version 5.5.6

##### Changes

1. During document validation, Object IDs that are not implemented as GUIDs are no longer reported as incorrect formats. The implementation of IDs as GUIDs according to RFC4122 
is a recommendation and may be handled differently by other tools. If the GUID format is not used it may be difficult to 
distinguish a name reference from an ID reference in certain situations.

2. Minor Changes in the Model and News explorer should improve the look and feel.

### Version 5.5.5

##### Changes

1. The editor now offers the possibility to download AutomationML libraries and
models directly from the new AutomationML download page.

2. In addition, the model explorer has been adapted and the AutomationML models
and examples linked via the AML book have been integrated. 
For this purpose, the referencing scheme for the model page and the news
page has been adapted.

3. The included AutomationML Standard libraries Edition 2.1 
have been exchanged for the versions offered on the automationml site.



### Version 5.5.4

##### Changes

The AutomationML Association renews its web representation. This also makes some resources used by the editor temporarily unusable. Before a new permanent solutionis implemented, the editor uses a resource library provided on GitHub.  This is used temporarily to install program updates and publish news. For future use of modeling resources, it is required that you update your AutomationML Editor version by **July 12 at the latest.**


### Version 5.5.3

##### Bug Fixes

1. Attribute Editor switched to disable mode for attribute mirrors if a wrongly referenced attributetype was identified as an attribute master.
2. Fixed a bug creating SystemUnitClasses from InternalElements, when the InternalElement has InternalLinks.

### Version 5.5.2

##### Bug Fixes

1. Editing of AttributTypeLibraries is enabled again.
2. Vertical Scrollbars in library views are only visible if needed. This affects the capture dialog, too.
3. The default name for all new aml files is "newfile.aml"
4. Saving a new aml file as a container will change the name of the new aml file to the name of the container.


### Version 5.5.1

##### Bug Fixes

AMLFile properties could not be edited if no object was selected before.

##### Added Feature

ID and IDRef XS-Datatypes are editable as normalized strings when used as
AttributeDataTypes in Attribute definitions.

### Version 5.5.0

##### Changes

In this version of the editor, the appearance of the editor has been 
changed a little. A slightly improved icon library is used to 
represent the AutomationML objects, in which the icons have been
made slightly more readable and the display efficiency has been optimized. 
This library is publicly available via the AutomationML website.

Attributes are now also displayed in the tree view of the attribute type library. 
This simplifies the construction of an attribute type library by making it easier 
to copy attributes back and forth between attribute types. 

##### Notes to plugin developers
This Version supports a new Plugin Interface *INotifyAMLDocumentSaved*. Plugins, implementing this
interface get a notification when an AMLFile has been saved by the AutomationML Editor.
The Plugin contract has to be updated to version 2.4.0 to use this interface.
