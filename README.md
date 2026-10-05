# fl ledger

This branch is the shared ledger of fl (FerroLoop): the gate runs, attempts and decisions recorded against this repository's issues. fl only ever appends to it. Do not edit it by hand: every machine that reads it checks that each file only grows, and refuses a ledger that changed.

- `format`: the layout's version.
- `runs/<key>/<n>.jsonl`: gate runs, one directory per gate.
- `attempts/<key>/<n>.jsonl`: attempts, one directory per project.
- `decisions/<key>/<n>.jsonl`: decisions, one directory per record or finding.
- `quarantine.jsonl`: lines readers skip, and why.

A key is the first 32 hexadecimal digits of the SHA-256 of the item's IRI.
