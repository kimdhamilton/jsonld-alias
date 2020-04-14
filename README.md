# jsonld-alias

- input_credentialSubject.json is [Example 9 from the VC Data Model](https://www.w3.org/TR/vc-data-model/#example-9-usage-of-issuer-expanded-property)
- input_learnerRecord.json changes `credentialSubject` to `learnerRecord` through an alias in the context
    - Reference: [Aliasing keywords](https://json-ld.org/spec/latest/json-ld/#aliasing-keywords)

The norm and quad files demonstrate no diffs.

How we'd want to go about this is defining an ILR context, where we would move this alias plus define other terms.