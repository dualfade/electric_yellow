# electric_yellow

A targeted collection of highly probable injection payloads.

- Targetted "hit-lists" for application fuzzing and parameter injection.
- Seek quick response hits, resulting in faster vulnerability enumeration.
- Minimal footprint testing.
- Easily use with burp intruder or ffuf.

### Fuzz

- fuzz_http_methods
  - http methods fuzz list
  - [ianna](https://www.iana.org/assignments/http-methods/http-methods.xhtml)

### Injection

- inj_jsfuck.txt
  - baseline jsfuck JavaScript injection payloads
  - [jsfuck](https://jsfuck.com/)

### ffuf usage

```zsh

# ~/.ffufrc
[input]
    wordlists = [
        "file1.txt:EY_FILE1",
        "file2,txt:EY_FILE2",
        "file3.txt:EY_FILE3",
        "file4.txt:EY_FILE4"
    ]

```
