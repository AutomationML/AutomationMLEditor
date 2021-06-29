## AutomationML Editor

### Version 5.5.4

##### Changes

The AutomationML Association renews its web representation. This also makes some resources used by the editor temporarily unusable. Before a new permanent solutionis implemented, the editor uses a resource library provided on GitHub.  This is used temporarily to install program updates and publish news. For future use of modeling resources, it is required that you update your AutomationML Editor version by **July 19 at the latest.**


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
