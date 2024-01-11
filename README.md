# electric_yellow

A targeted collection of highly probable injection payloads.

- Targetted "hit-lists" for application and parameter injection.
- Seek quick response hits, resulting in faster vulnerability enumeration.
- Minimal footprint testing.
- Easily use with burp intruder or ffuf.

### Fuzz

- fuzz_jsfuck.txt
  - baseline jsfuck JavaScript fuzzing payloads
  - https://jsfuck.com/

### Injection

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
