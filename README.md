# electric_yellow

A targeted collection of highly probable injection payloads.

- Targetted "hit-lists" for application fuzzing and parameter injection.
- Seek quick response hits, resulting in faster vulnerability enumeration.
- Minimal footprint testing.
- Easily use with burp intruder or ffuf.

### Fuzz

### Injection

- inj_jsfuck.txt
  - baseline jsfuck JavaScript injection payloads
  - https://jsfuck.com/

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

## Hitlist Usage

[generic.txt](https://github.com/dualfade/electric_yellow/fuzz/inj_generic.txt) generic.txt: This list contains a concise but varied list of fuzzing payloads. Run this during your initial testing of POST/GET parameters looking for anomalous behavior. Any interesting behavior detected should help inform more focused tests.

[separators.txt](https://github.com/dualfade/electric_yellow/meta/meta_separators.txt): This file contains the payloads which would replace the {separator} keyword.

[generic_api.txt](https://github.com/dualfade/electric_yellow/inject/inj_generic_api.txt): Use this in tandem with separators.txt where the entries would replace the {payload} keyword during fuzzing.

```json
{
  "param": "value{separator}{payload}"
}
```

`https://target.com/path?param=value{separator}{payload}`
