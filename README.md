# SCAP-Requirements
Safety Critical Advisory Panel’s requirements for developing a safety critical technology specification.

### Khronos SCAP document layout information

4 types of document that make up the SCAP requirements and guidelines documentation and the files that represent them. The term document here means the finished document, the output result. Files, the .adoc type, contain text that is included in a document. The following patterns in file names means the following:

* File suffix .adoc is an Asciidoc file type
* - Prefix common to .adoc files - files that belong to one document
* - No prefix or 'cmn_' - files common to many documents
* Resultant output file e.g. .pdf

Chapters or sections in a document is designated by numbers following the prefix document name. This is followed by a title or description. The title is followed if present by the Khronos SCAP Git issue (or Bugzilla) number where the subject matter originated and is tracked.  

The aim of the file formatting shown here is to automatically order the document section in the order they would appear in the final document. There is a one to one relation between the file on the subject chapter. This makes it easier to locate a file and match to the Git issue number. File name formatting:
DocumentName | Section | chapter | [Git issue number #xxx] | Section title/description.adoc

The aim is to order the document files in the order the content would appear in the rendered document again to make it easier to locate particular content. The method used is not perfect but generally does work. Please do use this system when creating new document content.

Files that are common are duplicated in other SCAP documents like SCAP-Requirements (in a file system they would be shared for many documents).

#### To see the document
Install Asciidoc Editor FX then double click on the file *Requirements_0_MainTopLevelAllIncludes.adoc*. Should see the document rendered.

#### Status of documents in this directory
3/10/2016 The documents have been created using Asciidoc Editor FX and the Asciidoctor executable. The majority of the Asciidoc formatting works ok using the when using the Editor FX, some parts like to the TOC work with quirks, some Asciidoc attributes do not appear to work. Using Asciidoc Editor FX is quicker to get off the ground without to much bother and automatically shows an HTML preview. Also an  added bonus is you are able to export from within the Editor both PDF and HTML documents. AsciidocEditorFX is available on most platforms. The editor contains everything including fonts, styles and themes. But it is broken on the Mac OSX High Sierra. This is still broken as off 14/02/2018.

An alternative is to use the editor Atom with the following packages installed:

* markdown-writer
* linter-markdown (and linter)
* markdown-scroll-sync
* acsciidoc-assistant
* language-asciidoc
* autocomplete-asciidoc
* asciidoc-preview
* asciidoc-image-helper
* zen
* auto-soft-wrap
* linter-write-good
* status-stats-jbrains

Using Atom means you also need to do a few things manually to enable your work flow. You also need to provide the Asiidoc theme file. From the command line your bring all the elements together to either render a PDF or HTML:

asciidoctor -r asciidoctor-pdf -b pdf -a pdf-style=themes/default-theme.yml Requirements_0_MainTopLevelAllIncludes.adoc

Not all Asciidoc layout features are available to embed in the document and therefore means editing the theme file. The theme file is copied from asciidoctor-pdf Git repository and edited a little to try and match the output PDF rendered document with that produced by the Editor FX.

#### What does not work with Asciidoc attributes and AsciidocEditorFX
* PDF style themes are ignored it seems (works when generating the PDF from the command line)
* toc::[] not rendered in a specified place
* docdate and locatedate date format could not change using i.e *locatedate: {sys: +%d-%m-%Y}*
* Not able to customise header and footer. May be a post .yml CSS thing as the document is rendered to the relevant back end. Asciidoctor?
* docinfo: not working
* styledir:, styleinfo:, linkcss: not working
* table formatting could not change
* text alignment does not work using *[center/left/right]*

