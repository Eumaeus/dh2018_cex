# dh2018_cex
Tutoriales y demostraciones: Formato CEX, para DH 2018, Ciudad de México.

## What Editions of the Matthew Fragment are in the CEX Library?

- XML Edition (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_xml:`): A CEX edition keeping the TEI-XML markup *internal* to each citable passage. See the file `XML/MSS2017-091.xml` for the file from which this was derived.
- Diplomatic Edition (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_dipl:`): A plain-text (no markup) edition derived from the XML. `<supplied>` text replaced with `…`; abbreviations left un-expanded; non-standard orthography or spelling mistakes left as on the manuscript; `<unclear>` text presented.
- Normalized Edition (`urn:cts:greekLit:tlg0031.tlg001.fu2017091_normal:`): A plain-text (no markup) edition derived from the XML. `<supplied>` text present *when it filles partial lacunae in otherwise expected words; `<supplied>` text replaced with `…` *when it represents a whole word or phrase missing from the manuscript*; abbreviations expanded; obvious spelling or copying errors fixed; syntactically invalid forms left as on the manuscript.
- Westcott and Hort Edition (`urn:cts:greekLit:tlg0031.tlg001.fuwh:`): The 1885 Greek edition of the verses represented on the fragment.
- Reina–Valera (`urn:cts:greekLit:tlg0031.tlg001.furv:`): The 1602 Spanish translation of the verses represented on the fragment.
- King James Version (``): The 1611 English translation of the verses represented on the fragment.


## Frequently Asked Questions


- **Why not just use TEI-XML?** Because it does not result in a coherent text. "`ἀνα<supplied>τε</supplied>ίλ<supplied>αν</supplied>το<supplied>ς</supplied>`" is not a Greek word that can be analyzed. In order to analyze this word, you will *have* to re-edit the text. A TEI-XML-based approach would have every user re-edit that text *every time* she wants to parse, count, or read "`ἀνατείλαντος`". "Stripping the markup before searching" is a re-editing of the text! With CEX, we are simply doing that editing *once*, and capturing it in a citable *edition*. 

- **Isn't CEX very verbose?** Maybe.

