# fx-unreachable

Test fixture for an Autoheal vulnerability-remediation agent. Nothing here is production code.

- **Setup:** `minimist` is pinned to `1.2.5` (CVE-2021-44906, prototype pollution; fixed in `1.2.6`).
- **Not reachable:** no source file imports or calls `minimist`. It is a leftover dependency.
- **Expected agent outcome:** no pull request. The agent should record the finding as "not reachable" with evidence (no import or call site found).
