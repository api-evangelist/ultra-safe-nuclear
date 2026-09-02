# Ultra Safe Nuclear

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Ultra Safe Nuclear Corporation (USNC) was a Seattle-based advanced nuclear company, founded in 2011,
that vertically integrated fourth-generation nuclear power — the Micro Modular Reactor (MMR), the
Pylon space reactor developed through its USNC-Tech subsidiary, and Fully Ceramic Microencapsulated
(FCM) TRISO nuclear fuel manufactured at Oak Ridge, Tennessee.

**The company is defunct.** It filed for Chapter 11 bankruptcy in the District of Delaware in
October 2024 and its assets were sold in a bifurcated Section 363 auction:

- **NANO Nuclear Energy** — MMR and Pylon reactor patents and demonstration partnerships, $8.5M
  (court-approved 18 December 2024) — https://nanonuclearenergy.com/
- **Standard Nuclear** — FCM/TRISO fuel business and the Oak Ridge facility, $28M (closed
  February 2025) — https://www.standardnuclear.com/

## Why this profile is thin

No API surface was found, and none is expected: USNC manufactured reactors and nuclear fuel, not
software. The full contract-discovery pass (OpenAPI on every candidate host root, GraphQL
introspection, MCP `tools/list`, A2A agent card on both well-known paths, gRPC/Protobuf, WSDL,
package registries) returned nothing.

- `usnc.com` — the primary corporate domain — returns **NXDOMAIN**. The registration is active
  through 2027-03-12 and mail is still routed to `usnctech.mail.protection.office365.us` (Microsoft
  365 US Government cloud) with a `p=quarantine` DMARC policy, but no address record is published.
- `ultrasafenuclear.com` resolves to an **unpublished Squarespace site** that answers every path
  with the same 3,141-byte "Coming Soon" shell — including a negative-control path that cannot
  exist — so every 200 it returns is a catch-all, not a document. Its ownership could not be tied
  to USNC from any public record, so it is **not** wired as this company's website.
- The company's GitHub organization, [github.com/USNC](https://github.com/USNC) ("Ultra Safe
  Nuclear Coporation - Technologies"), exists but has **zero public repositories**.
- No first-party package was found on npm, PyPI, RubyGems, crates.io, NuGet, Maven Central or
  pkg.go.dev.

The stub's original `Website` pointer was `https://forgeglobal.com/ultra-safe-nuclear_stock/` — a
secondary-market trading venue's listing page, not the company's own site. It has been moved out of
the scored pointers into `x-venue-listing` (roadmap#56).

## Artifacts

| File | What it records |
|---|---|
| `well-known/ultra-safe-nuclear-well-known.yml` | The full named-path `.well-known` probe on both candidate hosts — all misses, with the negative control that discards the catch-all 200s |
| `security/ultra-safe-nuclear-domain-security.yml` | DNS/TLS/SPF/DMARC evidence of the wind-down: registered domain, live mail plane, no web plane |
| `llms/ultra-safe-nuclear-llms.txt` | Agent-readable summary of the company's status and where its technology went |
