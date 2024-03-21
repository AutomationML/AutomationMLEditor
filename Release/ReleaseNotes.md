
## AutomationML Editor Release Notes


### [Version 6.2.1](https://github.com/AutomationML/AutomationMLEditor/releases/tag/v6.2.1) 

With version 6.2, the AutomationML Editor offers more **support for the management and creation of AutomationML class libraries** according to [Conventions for the modelling of AutomationML libraries](https://www.automationml.org/wp-content/uploads/2023/11/Conventions-for-modelling-AutomationML-libraries-V1.0.0-external.pdf) in addition to continuous bug fixing.  The new functions are activated by default, but they can be deactivated via the options dialog.  

The most important improvement in version 6.2 is the distribution of AutomationML libraries via a publicly accessible file server and the integration of the libraries via external references. The editor contains a preconfigured access to the **AutomationML NextCloud** as a file server. However, it is also possible to use a company-owned or privately used file server as long as it is accessible via the WebDAV/Https network protocol. All configured servers can also be used in parallel.

As the AutomationML NextCloud server could be replaced in the future, the URLs of the integrated external references for accessing the libraries would have to be changed in this case. However, when a new server is introduced, the editor will provide a feature, to redirect and update the external addresses automatically.

You can find detailed instructions on how to use the new features in the wiki on the following topics:
- [Using external Sources](https://github.com/AutomationML/AutomationMLEditor/wiki/UsingExternals)

- [External Source Windows](
  https://github.com/AutomationML/AutomationMLEditor/wiki/Layout#External-source-windows)

- [Preview Windows](https://github.com/AutomationML/AutomationMLEditor/wiki/Layout#Preview-windows)

- [Publishing](https://github.com/AutomationML/AutomationMLEditor/wiki/Publish)

Version 6.2.1 is published for the [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/8.0).

#### Options to activate library management
- Select the **Access External AutomationML Files** in the options dialog or from the editors main tool bar to get access to external AutomationML files from the AutomationML file server (currently the NextCloud; Internet access is required). Please note that by enabling this feature, the former provided import function from the AutomationML website will be disabled.
- Select the **Save Externals** in the options dialog to enable the local storage of referenced external libraries when saving the document. This means that all referenced external libraries, as well as their dependencies are stored to the documents relative folder '**_AMLExternalLibraries**' and are available offline for the current document.
- Edit or configure access profiles for file servers from the options dialog.

#### New functions for library management 
- The *File menu* contains the new **Add Reference** function. This allows the content of an AutomationML file from an external source, either from the AutomationML server or a company's own source, to be integrated into an existing document as an ExternalReference. All libraries from the external AutomationML file are displayed in separate windows ('External Views'). This function is only available if the **Access External AutomationML Files** option is selected.
- The *File menu* contains a new method **Outsource Libraries**. This function can be used to outsource the libraries contained directly in the document. Libraries that are published on the AutomationML library server are integrated as external sources, other libraries are outsourced to locally saved documents.
- The *File menu* contains the new **Publish** function. This function displays a dialog for publishing the currently edited AutomationML document to the activated library server. In order for a document to be published, the libraries it contains must fulfill the published conventions. When a library document is published to the AutomationML file server, all libraries are automatically signed. For user defined libraries, published to different target locations, the signing is optional.
- When library modelling conventions are reviewed the result is visualized. Specific **repair dialogs** are offered to repair failures to comply with mandatory conventions. 
- The *Open menu* provides the new **External Collections** function to load AutomationML defined library collections from the AutomationML file server or any other configured server. A collection contains preselected external references supporting specific modeling aspects. This function is only available if the **Access External AutomationML Files** option is selected.
- The *Open menu* provides the new **External Examples** function to load AutomationML defined examples from the AutomationML file server or any other configured server. Example models can contain class libraries which are not published and may contain InstanceHierarchies. AutomationML published class libraries are included using external references. This function is only available if the **Access External AutomationML Files** option is selected.
- The *View menu* provides the new **View Externals** function to open external referenced files and display the contained libraries in extra windows. 
- A new dialog has been added to browse the AutomationML file server to select libraries, models or example files. It is possible to enter filter criteria and to preview selected files. The dialog is viewed, when one of the mentioned referencing functions is called.
- A new dialog has been added to add and edit **access profiles for a file server** to provide libraries, models or example files. If write access rights are defined, a server can also used to publish documents.
- A **library dependency graph** is shown as a new relation window. Library dependencies are defined by versioning relations between libraries and class to class relations. 
- All external referenced files and their dependencies are automatically saved to a local folder, named **'_AMLExternalLibraries'** when a document is saved. The locally saved libraries enable the usage of the contained classed when the editor is used in offline mode.  This behavior is activated if the **Save Externals** option is selected.

#### New Features
- Support to dragg libraries and to paste them into the library container is added.
- "Create Version" is added as a new paste option for dragged libraries. Library versions can be marked as extensions.
- "Create Version" - dialog supports to edit a version number.
- Version information is shown behind the library name in tree views.
- Revision links are updated with alias references if the related version is external.
- Problem report dialog contains a new button to open the folder, containing the error log.
- New method to naviagte to all referenced role classes from systemUnit classes and InternalElements

#### Changes
- The function to create new documents initialized with AutomationML standard libraries has been removed. Standard libraries can only be used by referencing the external sources.
- The function to import AutomationML files from the AutomationML website has been removed. If the **Access External AutomationML Files** option is not selected, the import from AutomationML is still available.
- The menu item **Tools** has been renamed **Extras**.
- The menu item **Settings** has been removed. Settings can now be made in a new dialog, accessible under **Extras->Options...**. Options are grouped in categories.
- Backup file restoration dialog window can now be closed without restoring the file. Selected files are only restored, when the OK button is pressed.
- The naming for backup files has been changed. The current file name is included.
- Document version headers are not inserted into a document when no document versions are defined.
- AutomationML editor does not automatically adds a *SourceDocumentInformation* object to a modified document if a *SourceDocumentInformation* already exists.
- Split always creates an external reference into the remaining document, also when no classes of the splitted libraries are referenced.
- External reference path are created as relative paths when the location of the external document is relative to the edited document.
- Allowing references to external sources from documents, contained in an AutomationML container.
- Facet-Names of sibling facet-elements are checked to be unique.

#### Bug-Fixes
- Fixed an issue where opening settings threw an exception.
- Fixed an issue where the expansion state of properties was not maintained when the view changed.
- In the file-name attribute of a CAEX-Document no longer the complete file path is stored but only the filename. 
- Fixed an issue where the name of the backup file was shown as the file-name attribute instead of the document filename.
- Fixed an issue where documents in the document version collection of an AML File were deleted.
- Fixed an issue where expanded collection in views could not be closed.
