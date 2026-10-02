# TRITRI MAVLink C library (v2)

Generated MAVLink 2 C headers for the
[TRITRI](https://github.com/tritrisi/mavlink-tritri) dialect (MAVLink-M plus
private COP messages).

This repository is written by CI. Every commit here is generated from a commit
in [tritrisi/mavlink-tritri](https://github.com/tritrisi/mavlink-tritri),
and the commit subject matches the source commit it was built from. Don't edit
these files by hand or open pull requests here: changes will be overwritten on
the next generation. Propose message changes against `tritri.xml` /
`military.xml` in the source repository instead.

## Using it

The headers are header-only C and need no build step. Add the repository as a
submodule (or vendor a copy), put its root on your include path, and include
the dialect:

```sh
git submodule add https://github.com/tritrisi/mavlink-tritri-c_library_v2.git \
  mavlink/c_library_v2
```

```c
#include "tritri/mavlink.h"
```

`tritri/mavlink.h` pulls in `military`, `common`, `standard` and `minimal`, so
the full common and MAVLink-M message sets are available alongside the TRITRI
private messages. The dialect definitions the headers were generated from are
kept in `message_definitions/` for reference.

## Traceability

Each commit message records:

- the source commit in `tritrisi/mavlink-tritri` (short SHA and link)
- the pinned `mavlink` and `pymavlink` revisions used to generate it

To generate the headers yourself, or for another language, see the
[source repository](https://github.com/tritrisi/mavlink-tritri#generate-bindings).

## License

MIT. See [`LICENSE`](LICENSE).
