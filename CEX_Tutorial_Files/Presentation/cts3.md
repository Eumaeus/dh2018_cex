
# CITE & CTS

## Identification, retrieval, & analysis of citable data

C. Blackwell, University College Cork, April 2018


--------------


# CTS (and then CITE)

Canonical Text Services (CTS) is a framework for **identifying and retrieving passages of text by means of machine-actionable canonical citation.**

CITE (for “Collections, Indices, Texts, and Extensions”) is an application of the principles of CTS to other kinds of data.

<p class="cwbNote">Developed for *The Homer Multitext*, Casey Dué and Mary Ebbott, edd., The Center for Hellenic Studies of Harvard University.</p>


-----------

#The Homer Multitext

--------------

#The Question

There is formulaic language in the *Iliad* and *Odyssey*.

How did it work?

--------------

#The Path to an Answer

- Hundreds of manuscript folios
- Thousands of images
- Scores of discrete texts—versions of the *Iliad* and commentary texts
- Graphical elements
- Language problems: meter, orthography, morphology, syntax, 

--------------

![Figure: Venetus A, *Marcianus Graecus* Z.454](images/VA012RN-0013.jpg)

--------------

![Figure: Venetus A, Book 8 (Θ) Subscription ](images/subscription.jpg)

--------------

CITE has evolved as our approach to this problem.

- Over 16 years of close work
- 100+ editors
- Several generations of technology (Perl, SGML, TEI-XML, XSLT, eXist, Google BigTable, PostgreSQL, Java/Groovy, RDF & Fuseki, Scala)

--------------

# Do *You* Want to Use CTS?

The following image is a test.

If it is horrifying, you do not want to use CTS.

If it interesting, you may want to use CTS.

--------------

![Thomas Jefferson’s Bible: His intellectual project required disaggretation of a book.](images/jefferson_sliced.jpg)

--------------

# The Aspirations of CITE

- Separation of Concerns, or, Avoiding the Instrumentalist Fallacy

- Declarative (not Procedural) Scholarship

<p class="cwbNote">The 2018b release of HMT data at <a href="https://github.com/homermultitext/hmt-archive">https://github.com/homermultitext/hmt-archive</a> contains work done in 2007 under a completely different toolchain.</p>

--------------

# The Instrumentalist Fallacy

Confusing the *tool* for the *job.*

Forcing a new technology to imitate an old technology.

--------------

![Figure: Codex Sinaiticus (4th c. CE)](images/sinaiticus.jpg)

--------------

The Venetus A (*Marcianus Graecus* Z.454)

![Figure: Venetus A](images/VA012RN-0013.jpg)

--------------


# The Job & the Tools

For a thousand years, the scholar’s best tool was the book.

Its job was to integrate and organize information in a portable and economical package.

(It is possible that its job has been superceded.)

--------------

# A Job

For 21st Century scholars, sometimes the job is to reproduce the appearance of a Physical Object, as an historical artifact.

[This absolutely beautiful version of Linnaeus’ *Species Plantarum* from Project Gutenberg](http://www.gutenberg.org/files/20771/20771-h/20771-h.htm) has values for which CTS would not be helpful.

For art historians, codicologists, bibliographers, the book *is* the job.

For these scholars, CTS may not be a useful tool.

HTML, or TEI-XML do the job.


--------------

# CITE is Another Tool

A tool that may help fulfill the promise of digital libraries *for philologists*…

- Access
- Reproducibility
- *Analysis & Synthesis*
- *Integration*

--------------

We want to pull apart out data, transform it, and put it back together, while *always being able to say what we are talking about.*

------------

# Declarative Scholarship

Running computational process is part of the process of research.
 
So is reading.

The results of those processes and readings becomes *scholarship* only when we can *cite* them.

------------

# `⌘-f` is not a Footnote

The “final mile” of any computer-mediated humanist scholarship is taking the results of our analyses and turning them into something specific and concrete, that we can share, *independent of any particular technology.*

Historical practices give us the solution: *Canonical Citation*


------------

# Citation

- We can name what we are talking about,
- As precisely (John 3:16; *Iliad*, edition of T.W. Allen, 2.1) or as imprecisely (*Iliad* Books 9 and 10) as we need,
- We can “quote” (reproduce the text under discussion, and only the text under discussion),
- And always have access to the larger context, what comes next, what came before.


------------

# Canonical Citation

- Not necessary “traditional citation”.
- Unique unambiguous citation values
- Immutable
- Independent of technology or format
	- physical books
	- digital texts, regardless of format

------------

# Canonical Citation

- Ideally capturing the semantics of a text
	- **citation hierarchy**
	- **bibliographic hierarchy**
	- (more on this shortly…)
- Ideally
	- concise & human-readable
	- machine-actionable

------------

# Canonical Citation

In many cases, particularly with old and cherished texts, tradition has given us a good basis for canonical citation.

- Homer, *Iliad* 1.1
- Sophocles, *Oedipus at Colonus* 1
- New Testament, *Luke* 2.1
- Euclid, *Elements of Geometry*, Book 1, Common Notions, 3

------------

# Canonical Citation

- Some texts do not have an accepted, traditional scheme of citation.
- Some texts do have a traditional scheme of citation, but it does not work as *canonical citation* as defined above.

------------

![Athenaeus, *Deipnosophistae* 13c, according to Causabon’s scheme of citation. ](images/Causabon_1.3c.jpg)

Causabon’s citation assumed the (imprecise) perception of a human eye on a physical page. But where does **b** end and **c** begin?



------------

# Canonical Citation

An editor can assert a citation scheme.

- Athenaeus, *Deipnosophistae*, 1.4 (Kaibel’s citation scheme of Book + Section)
- Anne Frank, *Het Achterhuis* 19420614.p1
- Eibhlín Dhubh Ní Chonaill, “Caoineadh Airt Uí Laoghaire” 1.1.1


------------

# An Abstract Model

CTS is based on an *abstract model* of “text” that is based on canonical citation.

It works *only* with implementations of that abstract model.

Definition:

> An ordered hierarchy of **citation** objects (OHCO<sup>2</sup>)

<p class="cwbNote">N. Smith, G. Weaver. “Applying domain knowledge from structured citation formats to text and data mining: Examples using the CITE architecture” <i>Text Mining Services</i> (2009).</p>

------------

# OHCO<sup>2</sup>: Citation Objects

A text consists of citation-objects, “citable nodes”.

- *Iliad* 1.1
- *Oedipus at Colonus* 1
- *Luke* 2.1
- *Elements of Geometry*, Book 1, Common Notions, 3

------------

# Why “Citation” Objects?

The original OHCO attempted to define a text as an “ordered hierarchy of **content** objects.”<sup>1</sup>

This immediately ran into problems in the digital realm. What is content?

<p class="cwbNote">DeRose, Stephen, David Durand, Elli Mylonas, and Allen Renear. “What Is Text, Really?” <i>Journal of Computing in Higher Education</i> 1, no. 2 (Winter 1990): 3–26.</p>

------------

# OHCO<sup>2</sup>: Citation Objects

By defining a text as an ordered hierarchy of *citation* objects, we are free to do what we want with the *textual content*.

------------

Homer, *Iliad*, Perseus Digital Edition, 1.1

~~~ XML
    <l n="1"> Μῆνιν ἄειδε θεὰ Πηληϊάδεω Ἀχιλῆος </l>
~~~

------------

Or…

~~~XML
    <l n="1">
		Μῆνιν ἄειδε θεὰ
		<persName n="urn:cite:hmt:pers.pers1">Πηληϊάδεω
		Ἀχιλῆος</persName> </l>
~~~

------------

Or…

`	Μῆνιν ἄειδε θεὰ Πηληϊάδεω Ἀχιλῆος`

------------

Or, in addition, *e.g.*, Homer, *Iliad*, Perseus Digital Edition, metrical analytical exemplar, 1.1:

`    ¯˘˘ | ¯˘˘ | ¯ ⋮ ¯ | ¯˘˘ | ¯˘˘ | ¯¯`

------------

# OHCO<sup>2</sup>: Ordered…

”Ordered”, because the sequence matters in a text.

------------

# OHCO<sup>2</sup>: …Hierarchy…

“Hierarchy”, because the text may be organized by containing elements.

The Homeric *Iliad* Book 1 (often) contains 611 citation-objects (lines).

Rajmund Kunić’s *Ilias* (a Latin translation of the *Iliad*) has 732 lines in Book 1.

------------

# OHCO<sup>2</sup>: …Hierarchy…

The hierarchy may be only one level deep, or may be many levels deep.

Different sections of a text may have citation-hierarchies of differing depths.

The Homeric *Iliad* has a two-level hierarchy throughout.

Kunić’s *Ilias* is two levels deep except at the end of Book 2, where it is 3 levels deep.

------------

# There are Many Ways to Implement OHCO<sup>2</sup>

~~~ XML

<TEI>
 <text>
  <body>
   <div n="19420614">
    <head id="1" n="h1">
      Zondag, 14 Juni 1942
    </head>
    <p id="2" n="p1">
    Vrijdag 12 Juni was ik al om 6 uur wakker en dat is heel begrijpelijk,
		daar ik jarig was. Maar om 6 uur mocht ik toch nog niet opstaan, dus
		moest ik mijn nieuwsgierigheid bedwingen tot kwart voor zeven. Toen
		ging het niet langer, ik ging naar de eetkamer, waar ik door Moortje
		(de kat) met kopjes verwelkomd werd.
    </p>
    <p id="3" n="p2">
    Om even na zevenen ging ik naar papa en mama en dan naar de huiskamer,
		om mijn cadeautjes uit te pakken. Het was in de eerste plaats jou die
		ik te zien kreeg, wat misschien wel een van mijn jnste cadeau's is.
		Dan een bos rozen, een plantje, twee takken pinkster-rozen, dat waren
		die ochtend de kinderen van Flora, die op mijn tafel stonden, maar er
		kwam nog veel meer.
    </p>
   </div>			
  </body>
 </text>
</TEI>

~~~

------------

# But “Format” ≠ “Model”

There are many ways to create valid TEI-XML that do not implement OHCO<sup>2</sup>.

------------

# CTS: Bibliographic Hierarchy

A text belongs to a TextGroup. *E.g.*

- “Thucydides”
- “New Testament”
- “Homeric Epic”
- "Anne Frank"
- "Michigan Papyri"
- "*Inscriptiones Graecae* II<sup>3</sup>”

------------

# CTS: Bibliographic Hierarchy

A text is an instantiation of a notional Work. *E.g.*

- “Homer, *Iliad*”
- “New Testament, Luke”
- “Anne Frank, *Het Achterhuis*”
- “*IG* II<sup>3</sup> 1-879”

------------

# CTS: Bibliographic Hierarchy

A text may be a Version of a notional Work. Versions are *real things that you can read*.

- Pope’s English translation of the *Iliad*
- Villoison’s edition of the *Iliad* according to the Venetus A Manuscript.

------------

# CTS: Bibliographic Hierarchy

An **Edition** is a Version in the language of original composition.

A **Translation** is a Version in another language.

<p class="cwbNote">The distinction between *edition* and *translation* can be fluid; CTS does not really care: they are all *versions*.</p>

------------

# CTS: Bibliographic Hierarchy

Or, a text may be an **Exemplar**, a specific example of, or derivative from, a particular **Version**.

- Thomas Jefferson’s personal copy of Villoison’s edition of the *Iliad*.
- The *HMT*’s normalized *Exemplar* of the *Iliad* derived from the *HMT*’s diplomatic Edition.
- The *HMT*’s *Exemplar* of the *Iliad*, transformed specifically for the purpose of topic-modeling, derived from the *HMT*’s diplomatic Edition.

Exemplars might become more clear during the Workshop.

------------

# CTS-URNs

A CTS URN captures the OHCO<sup>2</sup> model’s semantics:

`TextGroup.Work[.Version[.Exemplar]?]?:[N[.N]*]?`

------------

# A CTS URN

<img src="https://latex.codecogs.com/gif.latex?\dpi{150}&space;\fn_phv&space;\large&space;$\underbrace{\underbrace{urn:cts:greekLit}_\text{namespaces}:\underbrace{tlg0012}_\text{Homeric Epic}.\underbrace{tlg001}_\text{Iliad}.\underbrace{msA}_\text{Version}:\underbrace{1.1}_\text{citation}}_\text{cts-urn}$" title="\large $\underbrace{\underbrace{urn:cts:greekLit}_\text{namespaces}:\underbrace{tlg0012}_\text{Homeric Epic}.\underbrace{tlg001}_\text{Iliad}.\underbrace{msA}_\text{Version}:\underbrace{1.1}_\text{citation}}_\text{cts-urn}$" />

------------

# Some Examples

(Based on the *Iliad*, which consists, generally, of 24 poetic books, each containing several hundred poetic lines.)

In the `greekLit` namespace<sup>1</sup>:

- `urn:cts:greeklit:tlg0012` is the TextGroup-identifier for “Homeric Epic”
- `urn:cts:greeklit:tlg0012.tlg001` is the Work-identifier for “Homeric Epic, *Iliad*”

<p class="cwbNote"><sup>1</sup> The <code>greekLit</code> namespace is controlled by the Center for Hellenic Studies of Harvard University, maintaining a unique catalog of TextGroups and Works for texts in Greek dating earlier than 1453 BCE, preserved through manuscript transmission.

------------

# CTS in Action: Some Live Demos

![Cillian Murphy is not afraid of live demos.](images/dunkirk.jpg)

[Link](cite1.html)

------------

A work-level leaf-node citation:

[`urn:cts:greekLit:tlg0012.tlg001:1.1`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001:1.1)

Identifies every version of *Iliad* Book 1 line 1.

<p class="cwbNote">Some versions of the <i>Iliad</i> will not have a Book 1, Line 1; the citation above does not identify them.</p>

------------

A version-level leaf-node citation:

[`urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1)

Identifies *Iliad* 1.1 in a particular version.

------------

A (version-level) range.

[`urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1-1.10`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1-1.10)

All citation objects, in sequence, between 1.1 and 1.10 in this version, inclusively.

*N.b.* The result may well not be ten leaf-nodes, depending on the text.

<p class="cwbNote">Some Versions of the <i>Iliad</i> may lack a 1.1 or a 1.10, or 1.10 may come <i>before</i> 1.9. For such a version, this would be an invalid citation.</p>

------------

A version-level containing element.

[`urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1)

All citation objects contained by Book 1, in this version of the *Iliad*.

(In this one, there are 610.)

------------

A range of containing elements.

[`urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1-2`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1-2)

Every citation object in Books 1 and 2 of this edition of the *Iliad*.

------------

A mixed range.

[`urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.600-2`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.600-2)

In the `msA` version of the *Iliad*, from Book 1, line 600 through all of Book 2.


<p class="cwbNote">It is worth emphasizing that “line 600” is not necessarily the 600th line, but merely the line whose ID happens to be “600”.</p>

------------

CTS-URN subreferences. Identifying contents.

[`urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1@μῆνιν[1]`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1@μῆνιν[1])

[`urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1@ν[2]`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1@ν[2])

[`urn:cts:….perseus_grc2:1.1@μῆνιν[1]-1.2@οὐλομένην[1]`](http://localhost:9000/texts/urn:cts:greekLit:tlg0012.tlg001.perseus_grc2:1.1@μῆνιν[1]-1.2@οὐλομένην[1])

<p class="cwbNote"><b>N.b.</b> At least in the HMT implementations of CTS, <i>retrieval</i> happens at the citation-level only. And there are better ways to do this…</p>


-------------

# CITE: For Everything Else

CTS is for identification and retrieval of citable passages of text.

CITE is for everything else.

-------------

# CITE2 Model

In the CITE2 model, citable objects are modelled as unique objects in versioned collections.

Each *object* is the sum of its *citable properties*.

<p class="cwbNote">From 2007 until 2017, Neel Smith and I used an earlier model of Collections, with different semantics. Those were cited with <code>urn:cite:…</code>. In 2017 we recognized our error and redefined the semantics for collections. CITE2 URNs reflect this new understanding.</p>

# CITE2 Model: Collections

A collection may be referred either in the abstract as a notional collection, or concretely as a specific version of a notional collection.

# CITE2 Model: Versions and Properties

Each version of a collection defines a set of properties which may or may not be identical across versions, but apply to all objects within a given version.

All Objects in a Version of a Collection share a set of Properties.

Each Object in a Version of a Collection has a uniquely citable set of Properties.

Distinct objects may have identical contents, but within in a collection, each object is uniquely identified.

For this reason, individual objects may be canonically cited either as part of a notional or concrete collection, but individual properties can only be cited as part of a specific version of a collection.

# CITE2 Model: Ordered and Unordered Collections

Collections may or may not be intrinsically ordered. The relation of citable objects in ordered collection is analogous to the relation of citable passages in a citable text: it is possible to make statements about ordered relations at the notional level, but the ordering of citable units in individual versions are not guaranteed to agree with a notional ordering. 

For example, the Venetus A Manuscript has been rebound several times in its history. Each rebinding has put the folios of the front matter (before the actual *Iliad* text) in a different order. A notional "Collection of Venetus A Folios" might contain the same Objects, but different versions will put those objects in different sequences.

So the *notional* collection has no sequence, but each *version* does.


# A CITE2 URN

<img src="https://latex.codecogs.com/gif.latex?\dpi{150}&space;\fn_phv&space;\large&space;$\underbrace{\underbrace{urn:cite2:hmt}_\text{namespaces}:\underbrace{msAfolios}_\text{collection}.\underbrace{v1}_\text{version}.\underbrace{seq}_\text{property}:\underbrace{12r}_\text{object}}_\text{cite-urn}$" title="\large $\underbrace{\underbrace{urn:cite2:hmt}_\text{namespaces}:\underbrace{msAfolios}_\text{collection}.\underbrace{v1}_\text{version}.\underbrace{seq}_\text{property}:\underbrace{12r}_\text{object}}_\text{cite-urn}$" />

A Version of a Collection, then, is essentially a Vector of citable, typed property values.

One property can be identified as the “ordering property”.

-------------

# CITE2: Collection Example

We want to identify a collection of physical folio-sides of the Venetus A manuscript. So we make a collection:

`urn:cite2:hmt:msA.v1:`

-------------

# CITE2: Defining a Collection 

To define a versioned collection, we need only a little information:

| Property           | Value                            |
|:-------------------|:---------------------------------|
| URN                | `urn:cite2:hmt:msA.v1:`          |
| Description        | Venetus A  folio-sides           |
| Labelling Property | `urn:cite2:hmt:msA.v1.label:`    |
| Ordering Property  | `urn:cite2:hmt:msA.v1.sequence:` |
| License            | CC-attribution-share-alike       |


-------------

# CITE2: Defining Properties for a Version 

The Version of the Collection is defined by its Properties.

For the purposes of the HMT, we do not need to say much about each folio-side. 

| Property                         | Label          | Type     | Authority list |
|:---------------------------------|:---------------|:---------|:---------------|
| `urn:cite2:hmt:msA.v1.urn:`      | URN            | Cite2Urn |                |
| `urn:cite2:hmt:msA.v1.sequence:` | Page sequence  | Number   |                |
| `urn:cite2:hmt:msA.v1.rv:`       | Recto or Verso | String   | recto,verso    |
| `urn:cite2:hmt:msA.v1.label:`    | Label          | String   |                |
| `urn:cite2:hmt:msA.v1.image:`    | Image          | Cite2Urn |                |

-------------

# CITE2: An Object…

…in a Versioned Collection is defined by its property-values:

| Property                         | Value 
|:---------------------------------|:-------------------------------------------------|
| `urn:cite2:hmt:msA.v1.urn:`      | `urn:cite2:hmt:msA.v1:12r`                       |
| `urn:cite2:hmt:msA.v1.sequence:` | 23                                               |
| `urn:cite2:hmt:msA.v1.rv:`       | recto                                            |
| `urn:cite2:hmt:msA.v1.label:`    | Venetus A (Marciana 454 = 822), folio 12, recto  |
| `urn:cite2:hmt:msA.v1.image:`    | `urn:cite2:hmt:vaimg.2017a:VA012RN_0013`         |


-------------

# CITE2: An Object & its Properties

The CITE2 URN lets us cite objects and their properties specifically and unambiguously.

`urn:cite2:hmt:msA.v1:12r` → the object `12r` and *all* its properties

`urn:cite2:hmt:msA.v1.sequence:12r` → the value of the `sequence` property for `12r`

`urn:cite2:hmt:msA.v1.label:12r` → the value of the `label` property for `12r`

-------------

# CITE2: Versions

We now can identify an object: `urn:cite2:hmt:msA.v1:12r`

A conservator or codicologist might want to say *much* more about “Venetus A (Marciana 454 = 822), folio 12, recto”.  She could create another version of the Collection, with different properties, and cite:

`urn:cite2:hmt:msA.CODICOLOGISTVERSION:12r`

**But** we can all be assured that the *notional* citation to…

`urn:cite2:hmt:msA:12r`

…is talking about the same object.



-------------

# Relations: The “I” in CITE

With CTS and CITE2 URNs, we have a framework for *citable scholarly primitives* that lets us identify the objects of study.

**CITE Relations** the (**I**ndices in the CITE acronym) are relations between pairs of citable objects.

Borrowing from RDF, these are “subject-verb-object” relationships. The *verb* is an Object identified by a CITE2 URN, with  properties assigned to it as seems useful.

| Subject           | Verb      | Object           |
|-------------------|-----------|------------------|
| CTS or CITE2 URN  | CITE2-URN | CTS or CITE2 URN |

-------------

# Data Models: The “E” in CITE

The “E” in CITE stands for “Extensions”. 

All CITE Objects are, generically, the same, and they can be treated as such.

But some represent special types of data that require or afford special treatment:

- Binary Images
- Documented Scholarly Relations objects
- Commentary objects

CITE includes a provision for *discoverable data models* that handle these cases.


-------------

# CEX: CITE Exchange Format

A plain-text, straightforward way to capture CITE data.

A complement to other serializations:

- JSON
- RDF
- XML
- RDB Schemas
- &c.


-------------

# Code Libraries

- `xcite` Constructing, validating, and parsing CTS and CITE2 URNs
- `ohco2` Corpora of texts (CTS stuff)
- `citeobj` Collections of CITE Objects
- `citeimg` Extending a CITE collection of “objects” that are images
- `citerelations` Arbitrary relations among URN-citable data
- `scm` Managing libraries of CITE/CTS data; defining data-models.
- `cex` Serializing CITE data to a plain-text format; parsing that format
- `citejson` Unmarshalling JSON expressions of CITE data to Scala objects

-------------

# Apps & Tools

- `CiteApp` A “zero-configuration” web-application for interacting with CITE data.
- `Scala Cite Services Akka (scs-akka)` A microservice delivering CITE data (as JSON) over HTTP
- `Server CiteApp` [in development] A version of `CiteApp` that hand processing over to `scs-akka`
- `ICT2` (Image Citation Tool 2) A Javascript application for creating CITE2 URNs + ROIs for citable binary images.

-------------

# Go raibh maith agaibh

https://github.com/cite-architecture

christopher.blackwell@furman.edu
