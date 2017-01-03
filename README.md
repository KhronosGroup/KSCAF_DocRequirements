# SCAP-Requirements
Safety Critical Advisory Panel’s minimum requirements for developing a safety critical technology specification.

### Khronos SCAP document layout

4 types of document that make up the SCAP principle, requirement and guidelines documentation and the files that represent them. The term document here means the finished document, the output result. Files, the .adoc type, contain text that is included in a document. The following patterns in file names means the following:

* File suffix .adoc is an Asciidoc file type
* - Prefix common to .adoc files - files that belong to one document
* - No prefix - files common to many documents
* Resultant output file e.g. .pdf

Chapters or sections in a document is designated by numbers following the prefix document name. This is followed by a title or description. The title is followed if present by the Khrono SCAP Bugzilla issue number where the subject matter originated and is tracked.  

DocumentName | Section/chapter | Section title/description | [Bugzilla #xxxx].adoc

#### To see the document
Install Asciidoc Editor FX then double click on the file *Requirements_0_MainTopLevelAllIncludes.adoc*. Should see the document rendered.

#### Status of documents in this directory
1/12/2016 The documents have been created using soley Asciidoc Editor FX, have not using the Asciidoctor executeable. The majority of the Asciidoc formatting works ok, some parts like to the TOC work with quirks, some Asciidoc attributes do not appear to work. It may be running the documents through Asciidoctor will activate the non work attributes. This will need to be done at some points as Khronos will no doubt use the Asciidoctor method. The Asciidoc Editor FX was quicker to get of the ground without having fuff installing and setting up stuff. Also wanted on the fly see what you get as you edit. All very suck it and see approach. A great foundation to base your documentation tool chain on. 

#### What does not work with Asciidoc attributes and AsciidocEditorFX
* toc::[] not rendered in a specificied place
* docdate and locatedate date format could not change using i.e *locatedate: {sys: +%d-%m-%Y}*
* Not able to customise header and footer. May be a post .yml CSS thing as the document is rendered to the relevant back end. Asciidoctor?
* docinfo: not working
* styledir:, styleinfo:, linkcss: not working
* table formatting could not change
* text alignment does not work using *[center/left/right]*
