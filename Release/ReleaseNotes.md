
## AutomationML Editor Release Notes


### [Version 6.3.5](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.3.5) 

#### Bug Fixes
- When creating an instance from an external class, the CAEX path for the reference to the class was not formed correctly. This error has been fixed.
- Fixed an issue where the override method of inherited elements, which are inherited from external elements, results in an invalid caex reference.
- Fixed an issue where the editor terminates with an exception when no internet connection was available.
  
### [Version 6.3.4](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.3.4) 

#### Changes
- If the `Unique` option is selected in the paste dialog, inserted elements are always get a unique name, even if no uniqueness is required by the standard.
- No InternalLink connections between inherited interface objects are displayed in the inheritance view.

#### Bug Fixes
- Fixed an issue where the producer and domain field in the document identification of the publishing dialog were not editable.
- Fixed an issue where a version reference was published which could not be resolved.
- Fixed an issue where a version reference to an incorrect version was created.
- Fixed an issue where the version reference was not displayed in the dependency diagram.

### Version 6.3.3

#### New Features
- Newly created libraries are automatically assigned an `ID`.
- If a class is selected in the library view of an external document, the relation view also shows the classes derived from it, including the derived classes of the main document.
- `ExternalReferences`, classified as version references also contain a `Version` element, defining if the reference links to a new Version (forward) or old Version (backward).
- If three consecutive unauthorized login attempts have been made to an AutomationML file provisioning service, no further attempts will be made by the editor. Otherwise there is a risk that the IP address will be blocked by the server. The editor informs the user that the number of unauthorized login attempts has been exceeded. The login block remains in place even after the Editor is restarted. The editor will not attempt to log in again until the user releases the lock.  This is possible when executing the connection check in the configuration dialog of the service. However, this should only be done if the login information is correct.

#### Changes
- If a new document version is published that contains versioned classes or libraries, but these classes or libraries are not contained in the published previous version, the version references of these classes are deleted in the new version. This can happen if intermediate versions are involved.

#### Bug Fixes
- Fixed an issue where a new version document, created from a local copy of a published version, did not create a forward veresion reference in the published version.
- Fixed an issue where the merge service failed to correctly classify an imported external reference as a version reference.
- The problem that publishing a new document version to a local file system did not create a version reference has been fixed.

### Version 6.3.2

#### New Features
- The servicename of the selected active external AutomationML file server is shown in the top right main window header. The displayed name can be clicked to open the service configuration dialog.
- The verification icon for signed libraries provides the service name of the verification source in its tool tip.
- Server addministration allows to update key files used for library signing.
- Adding an AutomationML ID as a semantic reference to attributes is an additional paste option when pasting external attribute type references.

#### Changes
- The feature to automatically create an inheritance relation for child classes has been removed. It is recommended to model classes preferably in libraries as a flat list structure and not artificially reproduce the inheritance hierarchy.
- Due to an update in the modeling conventions for AutomationML libraries, classes and types are checked to contain a description.
- The dialog for moving an external AutomationML file distributor to another server has been modified. It is started via the configuration dialog of the new server.
- Library versionnumbers for exended versions of libraries or new editions do not require a higher version number for delta extensions.
- New document and library editions do not automatically increase the version number of classes.
- Dialogs for server administration have been redesigned for better feedback.
- The External Reference Assignment dialog has been modified and shows the already used references of the current document.

#### Bug Fixes
- Solved some issues regarding possible deadlocks when an external file sever could not be connected.
- Fixed an issue where undoing would leave an invalid document status and a subsequent check would cause a crash. 
- Fixed an issue where copying a class with a base class reference from an external document creates an invalid base class reference in the copied object.


### Version 6.3.1

This version of the editor facilitates the creation and publication of AutomationML library and document versions. It supports collaboration in the development of new versions and their distribution. The editor offers new functions for managing content, hosted on an AutomationML file server, such as withdrawing documents that have been published erroneously or incorrectly.  **A valid editor license is required** to use all functions in this context.

#### New Features

##### File Service Configuration
- It is now possible to configure **multiple file service profiles** for the same host. This allows to use a release configuration and a development configuration using the same hosting server. The different configurations are to be named with a unique service name.
- The file service configuration allows to define a **new backup data profile**. The backup profile is used to save documents, which are removed from the hosting file server. Backed up files may be restored.
- There is a new dialog for the **administration of a configured file server**. This makes it possible to withdraw published documents and renew the registration of classes and libraries. File transfer to a new server address with URL redirection can also be organized here.  The dialog can be started via the server configuration dialog when authorized write access to a server is defined. 
- **Withdraw a published document:** Published example and library collection documents can be removed from a publishing location at any time. Under certain circumstances, it is also possible to remove a published library document from the publication location. In this case, all entries made by the publication are reversed. If a backup data profile exists, the removed document is saved and can be restored.
- **Restoration of backed up files:** All backed up files may be restored to their original location. For backed up library documents the publication process is repeated. A backed up file can also be deleted permanently.
- **Recalculation of library and class catalogs:** If conflicts arise during the publication of documents, it may be necessary to recalculate the library and class catalogs. When recalculating the library catalog, all published libraries must be re-signed if the signature was contained in the library catalog.
- **Server file transfer:** All documents provided on a server can be transferred to a new provisioning location if a corresponding service profile is configured for the new location. If the transfer is successful, a redirection table is created, which can be used to redirect the now unreachable document addresses to the new addresses.
- The editor loads redirection tables from its local configuration folder or also from its public **`GitHub`** repository. If a redirection table is provided on **`GitHub`**, the URL redirection is set up for all users of the editor. If redirects are not to be used, the redirect files must be deleted manually. 

##### Document Version Management
- When a new library version is created and not defined as an extension, all classes in the new library version are also versionized. The user selects whether the minor version or patch version of the previous version is incremented. An automatic increment of the major version for all classes is not supported. 
- If a previous version does not have a version number, version 1.0.0 for the previous version is assumed.
- It is possible to create a new version of an already versioned document. This makes it possible to **create different branches for versioning**.
- It is now possible to create a new document version of the actual edited document by selecting the `Create new version Menu` in the main edit menu.
- It is now possible to create **a new version for a higher AutomationML edition**. A CAEX schema transformation is carried out for the new document and an attempt is made to swap external references for existing versions of the higher edition. Attributes of classes are extended with references to existing attribute types if possible. If no attribute type can be found for a class attribute, a new attribute type is created and referenced. With this procedure, it can happen that class references can no longer be resolved and manual reworking is required.
- If external documents are referenced, the user will be informed if new versions of the external document are available. The desired version can be selected and exchanged in a dialog that opens.  This feature must be activated in the document preferences settings.

##### Document Publishing
- Recommendations for the naming of classes are checked, when a document is published. Names can be edited using the repair function.
- If the data type of an attribute is ‘`xs:string`’ or the attribute is a structure attribute such as a list attribute, the system checks whether the unit is empty.
- If the data type of an attribute is a numeric data type, **the system checks whether an attribute unit is defined**. As repair method is offered for missing units.

##### General
- Attributes can now also be added via the Add button in each window of an element tree if an element with attribute assignments is selected.
- In the drop-down menu of the ADD button, you can now either create a new element without a type reference (as before) or **an instance of an external class or type**. Necessary references to external documents are added automatically. The drop-down menu contains an additional button for this purpose.
- A **new dialog is available** which opens when the ADD from externals button in the drop-down menu of the Add button is clicked. The dialog allows to navigate all classes of all external documents shared by a file server. The classes are represented as the normal library order tree or alternativly as an inheritance tree. 
- It is possible to capture an image of the dependency diagram for libraries and save it in the clipboard.
- The used UNECE code table defining units of measure has been updated to [revision 17](https://unece.org/trade/documents/2021/06/uncefact-rec20-0).  A new selection dialog allows to filter and navigate listed quantities and units. It is also possible to select the unit common code or alternatively the unit symbol as an attribute unit. The preference can be selected in the attribute editor settings. 

#### Changes

##### Document Publishing
- Fixed an issue where a forward version reference was not created when the name of the new version object has been changed.
- The publishing dialogue only shows the publishing locations for which write access is configured.
- Changing the publication target in the publishing dialogue will invalidate the conformance conventions that have already been positively validated.
- The standard file extension for key files for signing is "`.key.json`". However, existing files with the extension "`.key`" can also be read in.
- Fixed an issue where publishing a new document version to a target location that is different from the source location was rejected due to a local URI in a version reference.
- Version references between new version and previous version documents are automatically created when the new version is published.
- Forward Version references relating a previous version with a new version are not created, when no previous version is already published at the selected publishing location.
- Already published libraries are allowed to be published again when a different file server profile is selected.
- A `SourceDocumentInformation`, defined and inserted by the `AMLEditor`, is deleted when a document is published with a new Document Identification.

##### Document Version Management
- The creation of extensions in the `Create Version dialog` has been changed. Extensions may contain the classes of the previous version or may be defined as delta extensions without containing any previous library versions.
- When a new document version is created, document version forward references are not saved to the locally saved external source version. The version references are only generated when the new version is published.
- Names describing extended versions of documents are checked to contain only allowed characters.
- The numbering of extension versions can start from the beginning, if the extension is marked as delta.
- Description text of `ExternalReference` defining a version reference is changed to '`VersionRef`'.

##### File Service Configuration
- Library Server configuration can be directly called from the Extras-Menu without showing all options.
- Additional folder profiles **can not be added** in the Library Service configuration dialogue, if all access opportunities are already defined.
- Adding multiple folder profiles for the same document type and AutomationML Edition is rejected in the service configuration dialogue.
- The configuration dialogue for the shared file service has been further revised. Validity checks and some other information have been added.

##### General
- The dependency diagram for libraries has been revised, filenames are shown in node displays and arrow directions are normalized. 
- `SaveAs` for documents shows the filename of an existing file as the default name
- Adding a local file as an `ExternalReference` the reference path is set to a relative URI if the local file can be located in the same directory or any sub directory as the current file. 
- When a new expandable item has been added to a collection in the side view, the new object is expanded by default.
- Fixed an issue where the computation of the string, used to calculate the signature, provides different results for the same `caex` element when called from different locations. This resulted in an unverified state for signed objects.
- An empty Attribute Datatype assignment is shown as "Null" in the selection menu and property field. 
- Maximize- and minimize-buttons in dialog windows have been removed.
- The start time of the editor could be accelerated slightly.
- Introduction notes have been updated.
- A new Application logo is shown on the splash screen. The image is shown before any .net dlls are loaded.
- The windows registration of file types and file associations has been changed and is now better integrated with windows shell and windows explorer. The registry is executed once when this version is started. 
- Separate icons have been designed for the different document types.
- A new Application Icon has been designed.
- The About Dialog has been modified.

#### Bug Fixes
- Fixed an issue with selecting the start page to be shown when the editor has started.
- Fixed an issue related to the facet editor showing an invalid error message when an existing facet name is edited.
- Problems with the reaction of the expansion indicator during selection and with restoring the last state after changing the selected property or attribute item in the side views have been fixed.
