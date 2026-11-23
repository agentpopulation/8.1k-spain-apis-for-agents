## Spain API endpoints, snapshot 16 Nov 2026

- 8,139 endpoints passed a keyless data call, tested 16 Nov 2026 (IST)
- 141 services · country ES · 6,134 keyless JSON rows

### Download

- `Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz`: the full list, 8,139 rows, 213.5 kB gzipped (3.2 MB as CSV), SHA-256 `7193df356fddbc92a53c5045208cf0732af719fd3af4eb8da417293878ffe489`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 6,134 · Wrap one layer query as a get_layer_features tool: pass a where clause or a bounding box, return the matching features with a timeout.
- 📱 App features: 4,889 · Add the layers to an app map: read the service once, then ask for the features or the map of the visible area.
- 🧠 Grounding and data pipelines: 8,139 · Load the statistics and land-use layers on a schedule into your own store, so an agent can cite a dated source.
- 🧪 Evals and testing: 8,139 · Run your tool calls against a fixed set of URLs across formats and record which answer; last_tested is the baseline for your own re-tests.

### Changes

- First release
- Left out: 61 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 1 layer marked editable in the title (it can hold entries that people added).
- Left out: 15 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 66 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 2 ArcGIS layers that are records about named people (employee, patient, client or donor lists, home addresses, voter lists, sex offender and missing person layers).
- Left out: 2 rows of ArcGIS Online organisations that are class accounts (3 class sets or more in at least 20% of their rows, 10 class sets or more with no organisation name, or layers signed by students read by hand): their other layers are students' work too.
- Left out: 6 rows of class sets: one map layer saved under 5 or more students' initials or names in one ArcGIS Online organisation, or in 4 or more students' own organisations.
- Left out: 2 rows whose address is already in an earlier pack of the collection.
- Left out: 412 rows that are another address form of an ArcGIS layer already in an earlier pack of the collection (the same rows under another query).
- Left out: 1,391 rows that are a second address form of an ArcGIS layer in this list (the same rows under another query); one address is kept per layer, the newest test first.
- Overlap: 4,152 of these URLs are also in 59k-europe-region-arcgis-apis-for-agents.
- Overlap: 177 of these URLs are also in 25k-arcgis-server-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 16 Nov 2026; snapshot 16 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 16 Nov 2026.

Credit: Spain API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 16 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
