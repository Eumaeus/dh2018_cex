# CITEApp Download

This directory includes compiled, optimized versions of the CITEApp, including all necessary CSS and  javascript in a single `.html` file.

## Running

- Double-click on `cite-VERSION.html` to open it in a browser.
- If there is an active internet connection, the app will automatically fetch a digital library in `.cex` form.

## Running (Offline)

- Prepare a `.cex` file to load, or get sample `.cex` libraries from [here](https://github.com/Eumaeus/cts-demo-corpus/tree/master/CEX-Files).
- Double-click on `cite-VERSION.html` to open it in a browser.
- Use the `Choose File` button at the to select and open a `.cex` file.


## What Editions of the Matthew Fragment are in the CEX Library?

- XML Edition (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_xml:`): A CEX edition keeping the TEI-XML markup *internal* to each citable passage. See the file `XML/MSS2017-091.xml` for the file from which this was derived.
- Diplomatic Edition (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_dipl:`): A plain-text (no markup) edition derived from the XML. `<supplied>` text replaced with `…`; abbreviations left un-expanded; non-standard orthography or spelling mistakes left as on the manuscript; `<unclear>` text presented.
- Normalized Edition (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_normal:`): A plain-text (no markup) edition derived from the XML. `<supplied>` text present *when it filles partial lacunae in otherwise expected words; `<supplied>` text replaced with `…` *when it represents a whole word or phrase missing from the manuscript*; abbreviations expanded; obvious spelling or copying errors fixed; syntactically invalid forms left as on the manuscript.
- Literal Translation (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_newland_hedden:`): A literal translation of the *recto* of the fragment, by Janey Capers Newland and Gunner Hedden.
- Westcott and Hort Edition (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_fuwh:`): The 1885 Greek edition of the verses represented on the fragment.
- Reina–Valera (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_furv:`): The 1602 Spanish translation of the verses represented on the fragment.
- King James Version (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_fukjv:`): The 1611 English translation of the verses represented on the fragment.

## What are *Exemplars*?

In addition to the *editions* and *translations* mentioned above, the CEX Library includes some *analytical exemplars*. These are versions of the text that are…

1. Derived from specific editions or translations.
1. Transformed according to some scholarly principle.
1. Citable at an additional level of detail.

In this case, the *exemplars* are specific tokenizations of specific editions. While the New Testament is canonically citable by chapter+verse, these tokenizations are citable by chapter+verse+token, allowing precise identification of words under consideration.

The Exemplars in the library are:

1. A Tokenization of the diplomatic edition of MS 2017-091: (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_dipl.tokens:`)
1. A Tokenization of the Wescott and Hort Greek edition: (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_wh.tokens:`)


## Reference

This app is based on the [CITE Architecture](http://cite-architecture.github.io), a protocol for identification and retrieval of data via machine-actional canonical citations in URN format.

CITE/CTS is ©2002–2017 Neel Smith and Christopher Blackwell. This implementation of the CITE data models was written by Neel Smith and Christopher Blackwell using <a href="https://www.scala-lang.org">Scala</a>, <a href="http://www.scala-js.org">Scala-JS</a>, and <a href="https://github.com/ThoughtWorksInc/Binding.scala">Binding.scala</a>. Licensed under the <a href="https://www.gnu.org/licenses/gpl-3.0.en.html">GPL 3.0</a>. Sourcecode on <a href="https://github.com/cite-architecture/ScalaJS-CITE-Environment">GitHub</a>.
