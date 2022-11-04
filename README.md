This is a fork of the [Apache PDFBox](https://pdfbox.apache.org/) project.

# Objective
In Alfresco 5 and some other versions, changes have been made to the PDFBox library in order to address issues that are commonly encountered by Alfresco's use of the library for extracting plain text from PDF documents. For PDFBox 1.8, the latest patched version was 1.8.16. The changes are described [here](https://artifacts.alfresco.com/nexus/content/repositories/public/org/apache/pdfbox/pdfbox/1.8.16-alfresco-patched/pdfbox-1.8.16-alfresco-patched-diff.diff). 

Using this library provided by Alfresco, a number of transformation issues may still occur that were addressed by PDFBox 1.8.17 ([Release Notes](https://www.mail-archive.com/announce@apache.org/msg07575.html)). This last release of PDFBox 1.8 was never patched by Alfresco.

This repo replays the Alfresco Patches on the last version of PDFBox 1.8 and yields significantly improved results when performing plain text transformation (and subsequently, Solr indexing) on Alfresco 5 environments.

The actual meat of this repo is in the [1.8.17-alfresco-patched](https://github.com/MarkTielemans/pdfbox-alfresco-patched/commits/1.8.17-alfresco-patched) tag, specifically in [this](https://github.com/MarkTielemans/pdfbox-alfresco-patched/commit/44f5d32daadaec05ac6a84163a4c99a17da531b3) commit.

# Notes
For convenience, compilation targets modern JDKs. For this reason, unnecessary modules that rely on older libraries and-/or plugins have been disabled in the parent/pom.xml. Only pdfbox and fontbox are required.