Extractor.epub for VitalSource Bookshelf
========================================

This EPUB file allows you to convert books in VitalBook EPUBBook format into regular EPUB books.
By sideloading Extractor.epub, the content of other EPUBBooks loaded in Bookshelf can be packaged
into a regular EPUB file which you can then use on other ebook readers.

Usage
-----
* Sideload Extractor.epub into Bookshelf. See [here](https://support.vitalsource.com/hc/en-us/articles/203256896-Side-load-EPUB-files-to-Bookshelf-for-Mac-PC) for instructions.
* Open the book you want to extract. This is important, otherwise the extractor won't be able to access the book's files. You can close it once you opened it once in the session.
* You need to know the file name of the book you're trying to extract. VitalSource started to use randomized name from some version, but it's using WebView2 so it's extremely easy to follow [Microsoft guide](https://learn.microsoft.com/en-us/microsoft-edge/webview2/how-to/remote-debugging-desktop) to get new book name. Remember that the device ID before the randomized string is also part of the file name you need. (in ABCDEFG/abcdefg.vbk format, if your url is http://localhost:1234/ABCDEFG/abcdefg.vbk/xxx/xxx )
* VitalSource blocks access to .opf file from internal server, but it's basically some logic similar to url.contains('opf'), so it should be extremely easy to find in any debugger with string search.
* Enter the name into the 'File name' box on Extractor.epub. Then click 'Extract'.
* When processing is finished, you will be presented with a download of the converted EPUB file.

For Non-WebView2 Systems
---------------
MSHTML (classical EDGE) should be used, so you just need [Microsoft Edge DevTools Preview](https://apps.microsoft.com/detail/9mzbfrmz0mnj?hl=en-US&gl=US).
