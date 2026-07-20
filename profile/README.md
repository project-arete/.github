<p align="center">
  <img src="https://raw.githubusercontent.com/project-arete/.github/main/profile/logo.png" width="96" alt="Project Arete logo" />
</p>

<h1 align="center">Project Arete</h1>

<p align="center">
  <strong>Governed connectivity for systems, devices, and AI agents.</strong><br/>
  The orchestrator and SDKs for <a href="https://cnscp.github.io/web">CNS/CP</a> —
  the layer that decides <em>whether</em> two nodes should connect, under what contract,
  and in what context, before any data flows.
</p>

---

## What is this?

Traditional networks connect **addresses** and hope the rules get bolted on later.
**CNS/CP** (Connectivity Naming System using Connection Profiles) is
**relationship-centric** instead: nodes declare *what they can do* — as
**provider** or **consumer** of a **Connection Profile (CP)**, a machine-evaluable
contract — and the substrate decides what binds to what. Nothing connects
without declared identity, roles, and a matching CP: **deny-by-default**,
auditable by design.

> Others standardize messages. CNS/CP standardizes **binding**.

**Arete** is the orchestrator you deploy against. It performs **brokerage** —
matching compatible provider/consumer declarations in a shared context — then
instantiates governed connections and manages them through their whole
lifecycle. Depending on the CP, it either mediates the data itself (in-band)
or steps aside once the connection is governed and lets data flow peer-to-peer
(out-of-band).

The model in four steps:

**declare** → nodes publish the CPs they provide or consume &nbsp;·&nbsp;
**broker** → Arete matches compatible pairs in context &nbsp;·&nbsp;
**bind** → a governed connection is instantiated &nbsp;·&nbsp;
**operate** → the contract is monitored, adjusted, and audited for life

## Explore

| Repository | What it is |
|---|---|
| [**sdk**](https://github.com/project-arete/sdk) | The Arete SDK — build CNS/CP applications in **Node, Python, or Rust** |
| [**arete-monitor**](https://github.com/project-arete/arete-monitor) | A live dashboard for CNS/CP realms — systems, contexts, connections, and a realm graph. 📦 [**Easy installers for macOS / Windows / Linux**](https://github.com/project-arete/arete-monitor/blob/main/INSTALL.md) |
| [**arete-monitor-pwa**](https://github.com/project-arete/arete-monitor-pwa) | Arete Monitor as an **installable web app** — 🌐 [**open it in any browser**](https://project-arete.github.io/arete-monitor-pwa/), nothing to install, add it to your phone's home screen. Works with any realm presenting a valid certificate (all `*.aretehosting.com` realms qualify) |
| [**arete-widget**](https://github.com/project-arete/arete-widget) | Virtual widgets on a CNS/CP realm — describe a device as a **YAML widget** (its CP capabilities plus a faceplate) and the app registers it as a governed node with a live control panel, **no hardware required**. Great for prototyping contracts and standing in for real devices. 📦 [**Easy installers for macOS / Windows / Linux**](https://github.com/project-arete/arete-widget/blob/main/INSTALL.md)· 🌐 [**or open it as a web app**](https://project-arete.github.io/arete-widget-pwa/) |
| [**widget-library**](https://github.com/project-arete/widget-library) | The online widget library — community-extensible YAML widget definitions, validated against the CP registry and published as a [live catalog](https://project-arete.github.io/widget-library/) that **Arete Widget** loads at runtime |
| [**helm-charts**](https://github.com/project-arete/helm-charts) | Helm charts for deploying Arete |
| [**aretehosting**](https://github.com/project-arete/aretehosting) | The Arete Hosting application (Go + React) — deploy it in your own environment (Docker Compose or Kubernetes) to run **your own fleet of Arete orchestrators** |
| [**website**](https://github.com/project-arete/website) | Source of the Project Arete website |

**Connection Profiles** are governed centrally in the
[CP registry](https://cp.padi.io) — browse existing profiles like
[`padi.light`](https://cp.padi.io/profiles/padi.light) before authoring your own.

## Get a realm — no deployment required

**[Arete Hosting](https://aretehosting.com)** is a site we operate that gives
you your own Arete instance in a few clicks: sign in, click **Add
orchestrator**, pick a name — and you get a ready-to-run orchestrator at
`<name>.aretehosting.com` (deployed from the official Helm chart) with login
credentials to hand to your apps and users. It's the fastest way to get a live
realm to point the SDK, Monitor, or your own applications at.

> Arete Hosting is **free to use right now**. Down the road it will carry a
> fee — orchestrators take real compute to operate — so early experimenting is
> a good deal.

Prefer to run things yourself? The **same software that powers Arete Hosting**
lives in the [aretehosting](https://github.com/project-arete/aretehosting)
repo — deploy it on your own infrastructure and operate your own fleet of
orchestrators.

## Get started

1. **See a realm live** — create an orchestrator on
   [Arete Hosting](https://aretehosting.com) (or use your own), then open the
   [Arete Monitor web app](https://project-arete.github.io/arete-monitor-pwa/)
   right in your browser — or install the
   [desktop Monitor](https://github.com/project-arete/arete-monitor/blob/main/INSTALL.md) —
   and watch systems declare capabilities and the broker bind them in real time.
2. **Put a node on it — no code** — install
   [Arete Widget](https://github.com/project-arete/arete-widget/blob/main/INSTALL.md),
   pick a widget from the library, and add a governed virtual device to your
   realm in seconds.
3. **Build something** — grab the [SDK](https://github.com/project-arete/sdk),
   register a node, and declare your first provider or consumer.
4. **Design a contract** — model a new capability as a CP: two asymmetric
   roles, a schema, constraints, a context, and a data mode.

## Learn more

- 🌐 [projectarete.io](https://projectarete.io) — the project website
- 📖 [CNS/CP specification](https://github.com/CNSCP/specification) and the [CNS/CP site](https://cnscp.github.io/web)
