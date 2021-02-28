# JavaTLSParser
Parses Java TLS Debug log

To debug your Java TLS traffic run your java with `-Djavax.net.debug=ssl:record:plaintext`

Then save the log to a file.

That file is messy and it is not convinient to read it.
My HTML parser parses the log to a more convenient representation.
It also has sorting, filtering and colors
