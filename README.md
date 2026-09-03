<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/masthead-dark.svg">
  <img alt="Elton Sakyi. I build the parts of software that have to be right later." src="assets/masthead-light.svg">
</picture>

Permissions, financial records, audit trails, and evidence-backed decisions. I turn complicated institutional workflows into systems that can explain what happened, who was allowed to act, and what supports the result.

**[Portfolio](https://elton-sakyi-portfolio.vercel.app)** &nbsp;·&nbsp; **[Résumé](https://elton-sakyi-portfolio.vercel.app/Elton_Sakyi_CV.pdf)** &nbsp;·&nbsp; **[LinkedIn](https://www.linkedin.com/in/elton-sakyi/)** &nbsp;·&nbsp; **[eltonsakyi@proton.me](mailto:eltonsakyi@proton.me)**

<br>

## Wyncrest

![Wyncrest audit log verifying its own SHA-256 hash chain across 88 recorded events, beside a capability check refusing an administrator who was not granted it.](assets/project-visuals/wyncrest.png)

Rental operations for tenants, landlords and administrators. Rent charges, late fees, payments and refunds are stored as an append-only ledger, read back per contract and per role, and every privileged action is appended to a separate hash-chained audit log. A correction is a new entry pointing at the one it corrects, so a dispute is settled from the record rather than argued from memory.

|  |  |
|---|---|
| `01 / INVARIANT` | The ledger table has no `updated_at` column |
| `02 / EVIDENCE` | [1,101 tests passing](https://github.com/Knight-Frost/Wyncrest#test-verification) · [CI](https://github.com/Knight-Frost/Wyncrest/actions) · [the chain, and how it is verified](https://github.com/Knight-Frost/Wyncrest/blob/main/app/Models/AuditLog.php) |
| `03 / STATE` | Public · Active development · Live demo, HTTP only |

**[Repository](https://github.com/Knight-Frost/Wyncrest)** &nbsp;·&nbsp; [Live demo](http://18.216.245.190) &nbsp;·&nbsp; [Authorization model](https://github.com/Knight-Frost/Wyncrest/blob/main/docs/AUTHORIZATION.md)

<br>

## Camp Burnt Gin

![The administrator's queue showing three applications, beside the medical directory showing one camper, because clinical access is limited to active campers.](assets/project-visuals/camp-burnt-gin.png)

Enrolment and medical workflows for a state programme serving children with special health care needs. Four portals read one camper record. Which fields a portal may load is decided by a policy class on the server, not by the screen that asked, and health data is encrypted at rest.

|  |  |
|---|---|
| `01 / INVARIANT` | Clinical access is conditioned on a camper being active, not on rank |
| `02 / EVIDENCE` | [Encrypted attributes, model by model](https://github.com/Knight-Frost/camp-burnt-gin-platform/tree/main/backend/camp-burnt-gin-api/app/Models) · [Larastan, Pint and PHPUnit on PHP 8.2 to 8.4](https://github.com/Knight-Frost/camp-burnt-gin-platform/blob/main/.github/workflows/ci.yml) |
| `03 / STATE` | Public · Not deployed · I wrote the API, client, authorization, medical domain, tests and CI; [teammates led QA and the earlier prototype](https://github.com/Knight-Frost/camp-burnt-gin-platform/blob/main/CONTRIBUTORS.md) |

**[Repository](https://github.com/Knight-Frost/camp-burnt-gin-platform)** &nbsp;·&nbsp; [Contributors](https://github.com/Knight-Frost/camp-burnt-gin-platform/blob/main/CONTRIBUTORS.md)

<br>

---

### Also public

**[Portfolio](https://github.com/Knight-Frost/portfolio)** &nbsp; `Live · Maintained`<br>
Four modules that run each project's real logic instead of showing pictures of it. One hand-written `requestAnimationFrame` camera, no animation library. [Open it](https://elton-sakyi-portfolio.vercel.app)

**[FutureYou](https://github.com/Knight-Frost/Future-You)** &nbsp; `Prototype · Hackathon build`<br>
Six days at LetsBuild 26.3. Models what a money decision costs before you make it: a deterministic engine computes, and the explanation layer may only describe. No test suite.

**[Timeloop Snake](https://github.com/Knight-Frost/timeloop-snake)** &nbsp; `Public · No longer deployed`<br>
A Canvas game where a ghost of your previous run returns every fourteen seconds and repeats your moves.

### In private development

Two systems are still private, so nothing here is linked and none of it carries the weight of the work above. **Policora** ties each extracted insurance-policy fact to its source page. **Pathfinder** joins federal labour and education data without losing which source each figure came from. `Private · Publication review`

---

### How I work

**Corrections preserve history.** A financial error creates a compensating entry. The original stays readable. [`create_ledger_entries_table.php`](https://github.com/Knight-Frost/Wyncrest/blob/main/database/migrations/2024_01_01_000015_create_ledger_entries_table.php)

**Permission is decided on the server.** An interface can hide a control. Only the server can refuse the action, and the refusal is logged. [`EnsureAdminCan.php`](https://github.com/Knight-Frost/Wyncrest/blob/main/app/Http/Middleware/EnsureAdminCan.php)

**Absence stays absence.** A missing figure renders as missing. It is never quietly turned into a zero.

**Unfinished work says so.** A capability defined but not yet enforced reports itself that way in code. [`AdminCapability.php`](https://github.com/Knight-Frost/Wyncrest/blob/main/app/Enums/AdminCapability.php)

### How these were built

I use AI coding tools as part of implementation and review. Architecture, security boundaries and public claims remain mine. The decisions that matter are recorded in code, tests and documentation, so they can be inspected independently of how quickly they were produced.

### Now

Preparing Policora for a public read. Available for full-time software engineering roles, backend and platform work most of all.

**[eltonsakyi@proton.me](mailto:eltonsakyi@proton.me)**
