# JavaTLSParser
Parses Java TLS Debug log

To debug your Java TLS traffic run your java with `-Djavax.net.debug=ssl:record:plaintext`

Then save the log to a file.

That file is messy and it is not convinient to read it.
My HTML parser parses the log to a more convenient representation.
Including gzip and chunks decoding.
It also has sorting, filtering and colors

With `-Djavax.net.debug=ssl:record:plaintext` you'll get an inconvenient output that will look like this:
```
  0000: 48 54 54 50 2F 31 2E 31   20 34 30 31 20 55 6E 61  HTTP/1.1 401 Una
  0010: 75 74 68 6F 72 69 7A 65   64 0D 0A 44 61 74 65 3A  uthorized..Date:
  0020: 20 57 65 64 2C 20 31 33   20 4E 6F 76 20 32 30 32   Wed, 13 Nov 202
  0030: 34 20 31 39 3A 32 36 3A   30 38 20 47 4D 54 0D 0A  4 19:26:08 GMT..
  0040: 43 6F 6E 74 65 6E 74 2D   54 79 70 65 3A 20 61 70  Content-Type: ap
  0050: 70 6C 69 63 61 74 69 6F   6E 2F 6A 73 6F 6E 3B 20  plication/json; 
  0060: 63 68 61 72 73 65 74 3D   75 74 66 2D 38 0D 0A 43  charset=utf-8..C
  0070: 6F 6E 74 65 6E 74 2D 4C   65 6E 67 74 68 3A 20 35  ontent-Length: 5
  0080: 39 0D 0A 43 6F 6E 6E 65   63 74 69 6F 6E 3A 20 6B  9..Connection: k
```

Running it with the parser it will look like this:

![image](https://github.com/user-attachments/assets/1229f25a-3405-49ac-8c68-f47d094f3b9c)
