## Abdulwahed Mansour

### Rust Software & Systems Engineer

I build software systems in Rust — applications, backend services, storage engines,
infrastructure and developer tools, usually as multi-crate workspaces over PostgreSQL.

The through-line in my work is that guarantees are enforced rather than intended:
architecture rules that fail CI, database grants that make an invalid write
impossible, and tests that try to break a claim instead of confirming it.

---

### What I work on

| | |
|---|---|
| **Applications and backend services** | Multi-crate Rust workspaces over PostgreSQL — HTTP services, CLIs, schema design and migrations, RBAC, sessions, MFA, audit trails, JSON APIs and OpenAPI |
| **Systems software** | Storage-engine internals — segmented logs, frame codecs, crash recovery, single-writer locking — plus `no_std` crates, allocation control, bit-level wire formats and eBPF/XDP |
| **Developer tools** | Procedural macros, code generation with an overwrite contract, CLI scaffolding and migrations, golden-file testing |
| **Infrastructure software** | GitHub Actions as enforcement: MSRV matrices, `no_std` lanes, supply-chain gating, build-output assertions, repository-wide doctrine checks |
| **Storage and data systems** | Append-only and tamper-evident storage, canonical encoding, explicit durability control, database-enforced integrity |

Correctness, reliability, performance and security describe *how* I build, not what I
sell: property-based testing, fuzzing, differential testing against reference
implementations, conformance vectors, crash testing under `SIGKILL`, and written
records of what a system does not guarantee.

---

### Start here

**[rustio-admin](https://github.com/abdulwahed-sweden/rustio-admin)** — admin-panel
engine · *Rust · procedural macros · Axum · PostgreSQL*
[![crates.io](https://img.shields.io/crates/v/rustio-admin.svg)](https://crates.io/crates/rustio-admin)

Annotated Rust types in, a complete admin application out — list views, filters, bulk
actions, CSV import/export, relations, a JSON API, OpenAPI and SDK generation — plus a
CLI that scaffolds and migrates projects. Published on crates.io at 0.33.0, with
tags back to v0.4.0. 67 281 lines, 921 test attributes, five workspace crates.

Two parts worth opening the code for: generated files are content-addressed over a
canonical projection of their specification, so the tool can tell *"you edited this"*
from *"the spec changed"* and refuse an unsafe overwrite; and authentication is
written directly — Argon2, TOTP enrolment with a backup-code lifecycle and AES-256-GCM
secret storage, session tokens hashed at rest with every revocation funnelled through
one path, tested against ephemeral PostgreSQL via testcontainers.

---

**Failure-class demonstrations** — one integrity failure each, in the smallest system
that exhibits it

Each ships the same test suite **twice** — once against the repair and once against
the unrepaired code, with the expected pass and failure counts written in the README.
The failure is asserted, not only the fix, so a silently restored guard cannot produce
a green run. Each runs in about a second and each README opens by saying the system is
synthetic.

- **[append-only-demo](https://github.com/abdulwahed-sweden/append-only-demo)** — an
  audit log the application can rewrite, versus a schema where the application role
  holds no `UPDATE` or `DELETE` grant. The broken half is granted everything
  deliberately, because that is the normal setup rather than a strawman.
- **[double-write-demo](https://github.com/abdulwahed-sweden/double-write-demo)** — a
  check-then-write refund guard that passes every sequential test and double-refunds
  under overlapping requests.
- **[forked-history-demo](https://github.com/abdulwahed-sweden/forked-history-demo)** —
  two concurrent amendments producing two equally current versions of one record.
- **[broken-backfill-demo](https://github.com/abdulwahed-sweden/broken-backfill-demo)** —
  a lookup-table change that silently restates last year's invoices, and a backfill
  that reconstructs the historically correct value rather than today's.
- **[permission-leak-demo](https://github.com/abdulwahed-sweden/permission-leak-demo)** —
  a correct per-page permission check that still leaks a blocked table through search,
  autocomplete and names rendered inside an allowed list. The fix moves the check from
  endpoint to reachable data.

*(A sixth demonstration covers SSRF via DNS rebinding as a TOCTOU, with the resolver
and network simulated so the race is deterministic while the guard under test stays
real. It is local only and has no public repository.)*

---

**[polaris-chronos](https://github.com/abdulwahed-sweden/polaris-chronos)** — solar
position from first principles

Julian date, declination, equation of time, altitude and azimuth with an explicit
refraction constant, plus Hijri and lunar calendars and a location resolver with
caching. 108 test attributes over 5 618 lines. Ships as a CLI, an Axum service and a
Docker image.

---

**[rustio](https://github.com/abdulwahed-sweden/rustio)** — the predecessor of
rustio-admin

A Django-shaped web framework in Rust on SQLite: 49 216 lines, 696 test attributes,
with two full example applications generated in-tree. Superseded by rustio-admin,
which moved the same idea to PostgreSQL.

---

### Private work

Some of the work that best represents what I build is in private repositories. It is
described here and not linked.

**Authenticated record systems in Rust** — one line of work across three generations.
Append-only record systems whose tamper-evidence can be verified offline by a party
holding no key, built end to end: canonical wire format, cryptographic core, on-disk
storage engine, runtime and operator tooling.

The storage engine was written rather than chosen — a segmented on-disk log carrying
two independent hash chains, and a recovery routine that distinguishes a truncated
tail from a forged length field. SHA-256 and HMAC are implemented from FIPS 180-4 and
RFC 2104 and differentially tested against RustCrypto at the exact padding-block
boundaries. Authenticated encryption is applied to record bodies with the frame header
bound as associated data, so an auditor without the key can still verify the whole
chain. Six crates build `no_std` under a dedicated CI lane; architecture layering and
a cryptography allow-list are enforced as tests. Verification includes 622 lines of
property tests, 14 fuzz targets, a writer `SIGKILL`ed at seeded delays and then
reopened and audited, and two branches of one key produced by copying a persisted
directory and refused in both directions and through a relay.

**aero-mesh** — an XDP/eBPF packet filter written in Rust on `aya`, a `no_std`
bit-packed wire format with a CRC-4 integrity nibble and a 42-byte ceiling, and
Bellman-Ford negative-cycle detection.

Happy to walk through either privately.

---

### Also

Earlier work was Python and Django backends, and I still read and write Python, SQL,
C++ and Solidity where a target requires it. I do independent vulnerability research
on the side, written as runnable proofs inside a target's own test harness rather than
as descriptions.

**Status, stated plainly:** this work is verified rather than operated. It is held to
its stated properties by tests and CI; it has not been run in production for real
users.

---

**Rust · PostgreSQL · Tokio · Axum · sqlx · `no_std` · proptest · cargo-fuzz · Docker
· Linux · GitHub Actions · Python · SQL**

📍 Stockholm, Sweden · ✉️ abdulwahed.mansour@gmail.com

[❤️ Sponsor this work](https://github.com/sponsors/abdulwahed-sweden?metadata_source=github_profile&metadata_campaign=top)
