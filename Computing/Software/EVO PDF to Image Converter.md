The attempt to call  `ConvertPdfPagesToImageInEvent` ended up in an error. The error clearly indicates that it is trying to do a relative path based on the application.

```
pdfToImageConverter.ConvertPdfPagesToImageInEvent("http://www.africau.edu/images/default/sample.pdf", 1, 0);
```

```
System.IO.IOException: 'The filename, directory name, or volume label syntax is incorrect. : 'C:\Workspace\Applications\Iris\OnlineBanking.Iris\http:\www.africau.edu\images\default\sample.pdf''
```
