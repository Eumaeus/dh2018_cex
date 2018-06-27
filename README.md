# dh2018_cex
Tutoriales y demostraciones: Formato CEX, para DH 2018, Ciudad de México.

## Contents

- `MSS2017-091`: An integrated digital edition of Furman University, James B. Duke Library, MS2017-091, a 10th Century fragment of a manuscript of Matthew 12-13.
- `CEX_Tutorial_Files`: Files aimed at demonstrating how CEX can capture integrated digital library information.
- `DH2018_Posters`: PDF versions of the posters for the two projects represented in this dataset.
- `Scripts`: Scripts for opening a Chrome Browser with "cross-origin" and "local-file" restrictions disabled. See below.

## Using CiteApp Locally

`citeApp` is the easiest environment for exploring data encoded in the CEX format. You can start it by double-clicking `citeApp-1.11.0.html`. **But**…

To see images, you need to disable some protections in your browser. Spefically, to have CiteApp show images in `image_archive`, you need to disable your browser's restriction on accessing the local file system.

**These restriction exist for good reasons! This would allow CiteApp, or any other Javascript application, to read files off your computer. Proceed at your own risk! If you do not trust us, please do not proceed!**

### Safari

- In Safari, in the Safari menu >> `Preferences…`, go to the "Advanced" tab, and click "Show develp menu in menu bar"
- In that menu, check "Disable Local File Restrictions" and "Disable Cross-Origin Restrictions"

### Chrome

On Windows…

- In the `Scripts` directory of this repository, double-click the `InsecureChrome.lnk` linke, to open Chrome with those restrictions turned off. **Do not use this instance of Chrome for anything other than CiteApp!**

On Mac OSX…

- In a Terminal, type `open -a Google\ Chrome --args --disable-web-security --user-data-dir=""`
- **Or**, also in a Terminal, navigate to the `Scripts` directory in this repository and type `./macOS_insecure_chrome.sh`

On Linux…

- You are a godlike Linux user and can probably discover how to modify the Mac OS X instructions.

### Firefox

I have no idea. If you figure out how, I would love to know: `christopher.blackwell@furman.edu`

## Using CiteApp in Server Mode

If you have Python installed on your computer, you can do the following:

- In a terminal, navigate to a directly containing `citeApp-1.11.0.html`.
- Type `python -m SimpleHTTPServer`
- In a browser, visit `http://localhost:8000/citeApp-1.11.0.html`

If you do this, you should not have to disable "local file restrictions". To use the (preconfigured) images remotely, you will still need to disable "cross-origin" restrictions, as described above.

## Contact

Christopher W. Blackwell. Furman University. Greenville, South Carolina, USA. `christopher.blackwell@furman.edu`

