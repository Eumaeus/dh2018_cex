# CTS Workshop

Digital Humanities, 2018, Mexico City

Christopher W. Blackwell
The Louis G. Forgione University Professor
Department of Classics
Furman University
christopher.blackwell@furman.edu

## Links

- [Examples of the CITE Microservice](http://beta.hpcc.uh.edu/hmt/hmt-microservice/)
- [Server CiteApp: Homer Multitext Data](http://beta.hpcc.uh.edu/hmt/citeapp/)
- [Cite Architecture Overview](https://cite-architecture.github.io)
- [Tutorial CEX files](https://github.com/Eumaeus/CTS_Workshop_Cork)
- [CiteApp Repository](https://github.com/cite-architecture/CITE-App)
- [ICT2 (the Image Citation Tool)](http://www.homermultitext.org/ict2/)

# Tutorial Files

## Interacting with Tutorial CEX Files

1. Double-click `citeApp-1.11.0.html` to open the "zero-configuration" CEX browsing environment. By default it will load a CEX file containing the Irish text of *Caoineadh Airt Uí Laoghaire*.
1. At the top, right of the CiteApp browser window, there is a button named `Choose File` (and labeled "Choose a local .cex file"). By clicking on that button and navigatin to the `cex` directory (in this file hiearchy), you can load other CEX files and explore what they have to offer.

## The CEX Files

In the `cex` directory, there are a number of sample CEX files. The numbered ones build on each other. Taken together they show how to document a digital text, how to incorporate editions and translations, how to add paratext, how to document collections of data, how to add images, commentaries, and the Documented Scholarly Editions Data-Model.

New material is added at the **bottom** of each successive file.

### A Text-only CEX tutorial

1. `Cork_Lament_1.cex`: A single text in CEX.
1. `Cork_Lament_2.cex`: A translation of a text. Differentiated by the URN citation values.
1. `Cork_Lament_3.cex`: A text and translation aligned and integrated.
1. `Cork_Lament_4.cex`: Adding a single data-collection, a collection of "annotations" to the text.
1. `Cork_Lament_5.cex`: Adding a second data-collection: a collection of speakers in the poem.
1. `Cork_Lament_6.cex`: Adding CiteRelations, (arbitrary) associations between objects in the data-collections and passage of text.
1. `Cork_Lament_7.cex`: Formalizing some of the CiteRelations with the Commentary Data Model. `CiteApp` is aware of that data model and can annotate text-display based on it.
1. `Cork_Lament_complete.cex`: A full expression of text, translation, annotation, and commentary.

### Just for Fun

1. `jane_austen.cex`: For fun. The novels of Jane Austen, a text without a good *traditional* scheme of citation, which we have expressed in CEX by adding *machine-actionable canonical citation*. Load it in `CiteApp` and play with NGrams in the **Explore Texts** tab.

### Text, Object, Image

The `Papyrus…` files present a publication of a fragment from Herodotus' *Histories*, Book VIII on Papyrus Oxyrhynchus 2099, dated to early 2nd century AD, with alignment between a diplomatic edition, a physical artifact, and a documentary image.

1. `Papyrus_1.cex`: A short passage of Greek and its English translation.
1. `Papyrus_2.cex`: A complete edition and translation of Herodotus. Also *analytical exemplars* of passages of Herodotus, in the form of two different tokenizations of the text, citable at the token-level.
1. `Papyrus_3a_imageCollections.cex`: Adding CITE Collections documenting the physical fragment, P.Oxy.2099, and a collection of images of it (the collection contains only one image).
1. `Papyrus_3b_binaryImageDataModel.cex`: An image-collection in CITE is, first, just like any other collection. This CEX file shows how to identify a collection as offering binary image data, and how to associate it with one-or-more protocols for accessing binary image data.
1. `Papyrus_4_DSE_Relations.cex`: DSE is "Documented Scholarly Editions", an association among (1) citable passages of text, (2) a physical, text-bearing artifact, and (3) a region-of-interest on a digital image. This CEX file documents this special datamodel. `CiteApp` is aware of that datamodel and can integrate this data for display.
1. `Papyrus_Complete.cex`: The complete example of the Herodotus papyrus.

## Create Your Own CEX Files and Validate Them

The best way to start working with CEX is to use a text-editor to modify an existing, valid file.

**Validate** a CEX file by opening `CiteApp`, clicking the `Choose File` button, and selecting a CEX file. `CiteApp` uses the same libraries for transforming CEX data into CITE and CTS objects as any other tool, so it serves as a validation tool as well as a browsing environment. If a CEX file is invalid, `CiteApp` will report an error.

## Frequently Asked Questions

- **Why not just use TEI-XML?** (Answer 1) Because it does not result in a coherent text. "`ἀνα<supplied>τε</supplied>ίλ<supplied>αν</supplied>το<supplied>ς</supplied>`" is not a Greek word that can be analyzed. In order to analyze this word, you will *have* to re-edit the text. A TEI-XML-based approach would have every user re-edit that text *every time* she wants to parse, count, or read "`ἀνατείλαντος`". "Stripping the markup before searching" is a re-editing of the text! With CEX, we are simply doing that editing *once*, and capturing it in a citable *edition*. 

- **Why not just use TEI-XML?** (Answer 2) Because *composition is easier than decomposition*. A CEX file represents an aggregation of (decomposed) blocks of scholarly data. A TEI file requires *significant prior knowledge and processing* to yield discrete citable data.

- **Isn't CEX very verbose?** Maybe. It takes a lot of characters to associate a semantically rich citation with each datum that you want to cite. And there is a certain redundancy in producing, storing, and publishing (for example) a full diplomatic edition *and* a full normalized edition. But (and see above), an XML expression of this data, while (perhaps) more compact on a disk or SSD, *must be decomposed* before it can be analyzed. In our experience, storage is cheaper than CPU. And *procedural* decomposition is not citable, and therefore not scholarly.

## Rights

CiteApp is licensed under the GPL 3.0. CiteApp includes code from [OpenSeadragon](https://openseadragon.github.io), which is released under the [New BSD license](https://openseadragon.github.io/license/). The Greek text of Herodotus is in the [Public Domain](https://creativecommons.org/share-your-work/public-domain/cc0/); the remaining data related to Herodotus is licensed under a [CC-BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/us/) license. The Irish text of *Caoineadh Airt Uí Laoghaire* is in the [public domain](https://creativecommons.org/share-your-work/public-domain/cc0/). The English translation by T. Kinsella was published in *An Duanaire - Poems of the Dispossessed: an anthology of Gaelic poems*, edited by Seán Ó Tuama (Dolmen Press, Portlaoise 1981 ISBN 0-85105-363-7). It is included in this demonstration dataset under the doctrine of [Fair Use](https://www.dit.ie/media/library/documents/Copyright-Guidelines.pdf), a “reasonable portion” of a book for “research or private study”; please do not distribute this translation further.
