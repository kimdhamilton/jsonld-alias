# jsonld-alias

- [input_credentialSubject.json](https://github.com/kimdhamilton/jsonld-alias/blob/master/input_credentialSubject.json) is [Example 9 from the VC Data Model](https://www.w3.org/TR/vc-data-model/#example-9-usage-of-issuer-expanded-property)
- [input_learnerRecord.json](https://github.com/kimdhamilton/jsonld-alias/blob/master/input_learnerRecord.json) changes `credentialSubject` to `learnerRecord` and defines an alias in the context. See [aliasing keywords](https://json-ld.org/spec/latest/json-ld/#aliasing-keywords)

I generated the norm and quad files in [json-ld playground](https://json-ld.org/playground/) to demonstrate the output norms and quads have no diffs. (Attached)

Instead of defining the terms inline like this example did (example 1 below), we'd want to define/host an ILR context (example 2), where we would move this alias plus define other terms.

Example 1:
```
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    "https://www.w3.org/2018/credentials/examples/v1",
    {
      "learnerRecord": "https://www.w3.org/2018/credentials#credentialSubject"
    }
  ]
```
  
Example 2:
```
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    "https://www.w3.org/2018/credentials/examples/v1",
    "https://path-to-ilr-jsonld-context"
  ]
```
