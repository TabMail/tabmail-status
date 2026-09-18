# TabMail status

Public uptime monitor and status page for TabMail services, live at
**https://status.tabmail.ai**.

Powered by [Upptime](https://upptime.js.org): GitHub Actions probe every
endpoint in [`.upptimerc.yml`](.upptimerc.yml) every five minutes, commit the
results to this repository, open and close an issue for each incident, and
publish the site to GitHub Pages. No server, no third-party account.

## How to read it

Each service has two entries, listed together:

- **`<service>`** — its own `/health` endpoint, probed directly. This stays
  accurate even if TabMail's edge provider is down.
- **`<service> · error rate`** — a summary of the service's error rate over the
  last fifteen minutes, published by the TabMail backend. _Degraded_ means an
  elevated error rate; an outage here means most requests are failing even
  though the service answers. Auth is an external provider and has no error-rate
  entry.

## Repository conventions

- Everything outside `.upptimerc.yml`, `README.md` and `.github/` is generated
  by Upptime's workflows. Do not edit generated files by hand.
- Issues in this repository are opened and closed by the monitor and are its
  data source for uptime history. Do not open unrelated issues here; use
  [tabmail-support](https://github.com/TabMail/tabmail-support).
- Commits by the Upptime bot are unsigned and carry no DCO sign-off. That is
  acceptable in this repository only because it contains generated monitoring
  data and no TabMail source code.
