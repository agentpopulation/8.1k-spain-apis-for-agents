<p align="center"><img src="assets/banner.svg" width="100%" alt="Spain API endpoints: 8,139 API endpoints passed a keyless data call"></p>

# 🇪🇸 Spain API endpoints

**8,139 API endpoints filed under country code ES that answered a keyless GET with a data body. For agent and app builders.**

<p align="center"><a href="#files"><img src="https://img.shields.io/badge/endpoints-8%2C139-6366F1" alt="endpoints: 8,139"></a> <a href="#columns-and-tags"><img src="https://img.shields.io/badge/keyless%20JSON-6%2C134-6366F1" alt="keyless JSON: 6,134"></a> <a href="#whats-inside"><img src="https://img.shields.io/badge/services-141-0F172A" alt="services: 141"></a> <a href="#whats-inside"><img src="https://img.shields.io/badge/country-ES-EA580C" alt="country: ES"></a> <a href="LICENSE"><img src="https://img.shields.io/badge/licence-CC%20BY%204.0-0F172A" alt="licence: CC BY 4.0"></a></p>

<p align="center"><a href="#whats-in-it-for-you">What's in it</a> · <a href="#for-ai-agents">For AI agents</a> · <a href="#quick-start">Quick start</a> · <a href="#test-it-yourself">Test it yourself</a> · <a href="#files">Files</a> · <a href="#licence-and-credit">Licence</a> · <a href="#part-of-10m-api-endpoints-for-ai-agents">More packs</a></p>

This repository holds a 1,000-row sample and the services list; the full list of 8,139 endpoints is one download from the [latest release](https://github.com/agentpopulation/8.1k-spain-apis-for-agents/releases/latest).

**Endpoints filed under country code ES, for building an agent or app for Spain.** Statistics and boundary services of the Canary Islands, regional geoservices of Castilla-La Mancha and Cantabria, and layers of the national geographic institute, as URLs that answered with no key on their test date.

Selection rule: rows where `country is ES AND (host is services-eu1.arcgis.com OR NOT url matches /^https?://(services(dev|qa)?|tiles)[0-9]*(-[a-z0-9]+)?\.arcgis\.com//i)`, less the rows that a leave-out rule drops (each counted under Known limits).

8,071 of these 8,139 rows match the focus rule (below); the others are in the pack by the selection rule only, and Known limits says what they are. 4,152 rows (51.0%) are map layers on ArcGIS Online, where anyone can publish.

## In plain words

**What is an API endpoint?** An API endpoint is one web address that a program can ask for data, for example the latest reading at one weather station. A single service, such as a national weather agency, can have thousands of endpoints: one per station, city or dataset. This pack counts endpoints, not separate services.

**What does "passed a data call" mean?** On the date shown in each row, AgentPopulation sent one plain request to that address, with no password or key, and got a non-empty data body back (JSON, CSV, XML or a file): not an error page and not an empty result. Some bodies describe a dataset rather than hold its values; see Known limits. It shows the address answered with data on that day. It is not a promise that it answers today, and licences and usage limits were not reviewed.

## What's in it for you

Four ways to use this pack. Each bucket gives a count, a filter you can apply to the CSV, one example that passed, and a list of recommended starting points with the rule that picked them. Buckets overlap; a row can fit more than one.

Examples, recommended lists and the preview are drawn from rows that match this pack's focus rule, so a row that the selection rule put in this pack but that is about something else is not shown as a starting point. Counts cover the whole bucket.

<details>
<summary>The focus rule</summary>

Focus rule: `NOT title matches /(?<![a-z])(test|tests|testing|draft|drafts|copy|sample|samples|demo|untitled|scratch|temp|tmp|delete|deleteme|practice|dummy|example|training)(?![a-z])|final_final|\d{7,}/i`

</details>

### 🤖 Agent tools: Keyless JSON layers and tables an agent can call (Spain)

**6,134** endpoints from 141 services · Wrap one layer query as a get_layer_features tool: pass a where clause or a bounding box, return the matching features with a timeout.

4,329 of these are map-layer queries that asked for a few records (`resultRecordCount`); add a where clause or a geometry to ask about one place, and page through for the whole layer.

Start with: `tags has agent-ready`

Example: [1996](https://services-eu1.arcgis.com/C3HgCqjBMl1pyvzK/ArcGIS/rest/services/1996/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) · ArcGIS Online layers (services-eu1.arcgis.com, org C3HgCqjBMl1pyvzK) · passed 2026-11-16

<details>
<summary>Recommended starting points: 5 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack with the most endpoints that match this bucket and are tagged `agent-ready` (no key sent in the test call, JSON body, passed a data call). Ties go to the service with more country codes, then by name. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Sample preference in this bucket: `url matches //query\?/i`. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Datos Abiertos de Canarias (datos.canarias.es) | 1,805 | 3,810 | ES | json | [Indicadores demográficos. Grandes comar…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) (2026-11-16) |
| Castillalamancha (geoservicios.castillalamancha.es) | 74 | 74 | ES | json | [SIOSE/SIOSE\_2015](https://geoservicios.castillalamancha.es/arcgis/rest/services/SIOSE/SIOSE_2015/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Ign (serviciosgis.ign.es) | 48 | 48 | ES | json | [Hosted/Naturaleza](https://serviciosgis.ign.es/servicios/rest/services/Hosted/Naturaleza/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Rivasciudad (sit.rivasciudad.es) | 40 | 40 | ES | json | [Áreas\_de\_incidencia\_COVID](https://sit.rivasciudad.es/server/rest/services/%C3%81reas_de_incidencia_COVID/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Cantabria (geoservicios.cantabria.es) | 15 | 15 | ES | json | [Ocio\_Deportes\_Turismo](https://geoservicios.cantabria.es/inspire/rest/services/Ocio_Deportes_Turismo/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

### 📱 App features: Map services and layers to draw (Spain)

**4,889** endpoints from 141 services · Add the layers to an app map: read the service once, then ask for the features or the map of the visible area.

Start with: `url matches //(Feature|Map)Server//i OR url matches /[?&]service=w[mf]s/i`

Example: [1996](https://services-eu1.arcgis.com/C3HgCqjBMl1pyvzK/ArcGIS/rest/services/1996/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) · ArcGIS Online layers (services-eu1.arcgis.com, org C3HgCqjBMl1pyvzK) · passed 2026-11-16

<details>
<summary>Recommended starting points: 5 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack with the most endpoints that match this bucket and passed a data call. Ties go to the service with more country codes, then by name. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Datos Abiertos de Canarias (datos.canarias.es) | 560 | 3,810 | ES | xml, csv, json | [Indicadores demográficos. Grandes comar…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) (2026-11-16) |
| Castillalamancha (geoservicios.castillalamancha.es) | 74 | 74 | ES | json | [SIOSE/SIOSE\_2015](https://geoservicios.castillalamancha.es/arcgis/rest/services/SIOSE/SIOSE_2015/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Ign (serviciosgis.ign.es) | 48 | 48 | ES | json | [Hosted/Naturaleza](https://serviciosgis.ign.es/servicios/rest/services/Hosted/Naturaleza/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Rivasciudad (sit.rivasciudad.es) | 40 | 40 | ES | json | [Áreas\_de\_incidencia\_COVID](https://sit.rivasciudad.es/server/rest/services/%C3%81reas_de_incidencia_COVID/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Cantabria (geoservicios.cantabria.es) | 15 | 15 | ES | json | [Ocio\_Deportes\_Turismo](https://geoservicios.cantabria.es/inspire/rest/services/Ocio_Deportes_Turismo/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

### 🧠 Grounding and data pipelines: Statistics and land-use layers for scheduled loads (Spain)

**8,139** endpoints from 141 services · Load the statistics and land-use layers on a schedule into your own store, so an agent can cite a dated source.

Start with: the whole pack

Example: [Indicadores demográficos. Grandes comarcas de Can…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) · Datos Abiertos de Canarias · passed 2026-11-16

<details>
<summary>Recommended starting points: 5 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack with the most endpoints that match this bucket and passed a data call. Ties go to the service with more country codes, then by name. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Datos Abiertos de Canarias (datos.canarias.es) | 3,810 | 3,810 | ES | json, xml, csv | [Indicadores demográficos. Grandes comar…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) (2026-11-16) |
| Castillalamancha (geoservicios.castillalamancha.es) | 74 | 74 | ES | json | [SIOSE/SIOSE\_2015](https://geoservicios.castillalamancha.es/arcgis/rest/services/SIOSE/SIOSE_2015/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Ign (serviciosgis.ign.es) | 48 | 48 | ES | json | [Hosted/Naturaleza](https://serviciosgis.ign.es/servicios/rest/services/Hosted/Naturaleza/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Rivasciudad (sit.rivasciudad.es) | 40 | 40 | ES | json | [Áreas\_de\_incidencia\_COVID](https://sit.rivasciudad.es/server/rest/services/%C3%81reas_de_incidencia_COVID/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Cantabria (geoservicios.cantabria.es) | 15 | 15 | ES | json | [Ocio\_Deportes\_Turismo](https://geoservicios.cantabria.es/inspire/rest/services/Ocio_Deportes_Turismo/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

### 🧪 Evals and testing: Varied responses to test tool calls and parsers

**8,139** endpoints · 141 services · country ES · 3 formats · Run your tool calls against a fixed set of URLs across formats and record which answer; last_tested is the baseline for your own re-tests.

Start with: the whole pack

Example: [Indicadores demográficos. Grandes comarcas de Can…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) · Datos Abiertos de Canarias · passed 2026-11-16

<details>
<summary>Recommended starting points: 5 services, picked by the stated criteria inside</summary>

**Recommended starting points.** Selected by stated criteria, not a ranking of quality: Services in this pack that returned the most different formats, then the most endpoints that passed a data call, then by name: a mix of response shapes to test parsers and tool calls. Only services with at least one bucket row that matches the focus rule are listed, and the sample comes from those rows; the counts cover the whole bucket. The sample URL is the first row by URL sort after preferring, in this order: rows that match the bucket's sample preference when it has one, rows that return values rather than describe a dataset or a service (not ERDDAP /info/ pages, OGC GetCapabilities requests, bare OWS addresses, PxWeb tables, UN SDG series lists, Statistics Canada download pointers, WorldPop listings, GTFS validation reports, untitled rows or service root addresses), and agent-ready rows. Services named "ArcGIS organization" hold map layers from many owners and are added only when fewer than 5 other services match.

| Service (host) | Endpoints in bucket | In pack | Country codes in bucket | Formats in bucket | Sample URL that passed |
|---|---:|---:|---|---|---|
| Datos Abiertos de Canarias (datos.canarias.es) | 3,810 | 3,810 | ES | json, xml, csv | [Indicadores demográficos. Grandes comar…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) (2026-11-16) |
| Castillalamancha (geoservicios.castillalamancha.es) | 74 | 74 | ES | json | [SIOSE/SIOSE\_2015](https://geoservicios.castillalamancha.es/arcgis/rest/services/SIOSE/SIOSE_2015/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Ign (serviciosgis.ign.es) | 48 | 48 | ES | json | [Hosted/Naturaleza](https://serviciosgis.ign.es/servicios/rest/services/Hosted/Naturaleza/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Rivasciudad (sit.rivasciudad.es) | 40 | 40 | ES | json | [Áreas\_de\_incidencia\_COVID](https://sit.rivasciudad.es/server/rest/services/%C3%81reas_de_incidencia_COVID/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |
| Cantabria (geoservicios.cantabria.es) | 15 | 15 | ES | json | [Ocio\_Deportes\_Turismo](https://geoservicios.cantabria.es/inspire/rest/services/Ocio_Deportes_Turismo/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (2026-11-16) |

</details>

The same lists are in [recommended.json](recommended.json), ready for an agent to load.

## Questions an agent can answer with this pack

- Which demographic indicators does the Canary Islands statistics service map by district? Try [Indicadores demográficos. Grandes comarcas de Can…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) (Datos Abiertos de Canarias, passed 2026-11-16).
- Which land-use layers does Castilla-La Mancha serve? Try [SIOSE/SIOSE\_2015](https://geoservicios.castillalamancha.es/arcgis/rest/services/SIOSE/SIOSE_2015/MapServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (Castillalamancha, passed 2026-11-16).
- Which layers does the national geographic institute serve? Try [Hosted/Naturaleza](https://serviciosgis.ign.es/servicios/rest/services/Hosted/Naturaleza/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) (Ign, passed 2026-11-16).

## What "passed a data call" means

> [!NOTE]
> On the date in `last_tested` (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The `format` column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 16 Nov 2026; snapshot 16 Nov 2026.

## For AI agents

Start from keyless JSON endpoints (`agent-ready`). The code below loads `recommended.json` and calls the first recommended service in the Agent tools bucket, with a timeout (`node examples/agent-start.mjs --recommended`). With no argument, `node examples/agent-start.mjs` calls the most recently tested agent-ready row of the sample; pass a `.csv` or `.csv.gz` path to use that file instead. See [examples/agent-start.mjs](examples/agent-start.mjs).

```js
// Node 18+. Loads recommended.json (the local copy, or the raw file on GitHub) and calls one keyless JSON endpoint.
import fs from 'node:fs';

const RAW = 'https://raw.githubusercontent.com/agentpopulation/8.1k-spain-apis-for-agents/main/recommended.json';
const rec = fs.existsSync('recommended.json')
  ? JSON.parse(fs.readFileSync('recommended.json', 'utf8'))
  : await (await fetch(RAW)).json();

const pick = rec.buckets.find((b) => b.id === 'agent').services[0];
try {
  const res = await fetch(pick.sample_url, {
    headers: { 'User-Agent': 'agent-example/1.0' },
    signal: AbortSignal.timeout(15000),
  });
  console.log(pick.service, res.status, res.headers.get('content-type'));
  console.log((await res.text()).slice(0, 300));
} catch (err) {
  console.log(`did not answer now; last passed ${pick.sample_last_tested} (${err.message})`);
}
```

How an agent picks an endpoint:

1. Filter to `agent-ready` and your country or topic.
2. Prefer the newest `last_tested` and the larger services.
3. Call with a timeout and check the body before you use it.

## Quick start

The examples run against the sample in `data/` out of the box (1,000 rows). Each takes an optional path to a `.csv` or `.csv.gz` file instead.

```bash
git clone https://github.com/agentpopulation/8.1k-spain-apis-for-agents.git
cd 8.1k-spain-apis-for-agents
python examples/quickstart.py
node examples/quickstart.mjs
node examples/agent-start.mjs
```

Full list: download `Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz` (8,139 rows, 213.5 kB) from [releases/latest](https://github.com/agentpopulation/8.1k-spain-apis-for-agents/releases/latest), then gunzip it and pass its path. The scripts also read the `.csv.gz` as it is.

```bash
gunzip Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz
python examples/quickstart.py Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv
node examples/quickstart.mjs Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv
```

### curl

Quote the URL: some contain commas.

```bash
curl -sL "https://raw.githubusercontent.com/agentpopulation/8.1k-spain-apis-for-agents/main/data/Spain_API_Endpoints_AgentPopulation_Sample.csv" | head -n 4
curl -s --max-time 15 "https://services-eu1.arcgis.com/C3HgCqjBMl1pyvzK/ArcGIS/rest/services/1996/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json" | head -c 600
```

### Python

Standard library only: [examples/quickstart.py](examples/quickstart.py) reads the sample, or the path you pass, keeps agent-ready rows and calls the most recently tested one.

<details>
<summary>The code</summary>

```python
# Python 3, standard library only. Run from a clone of this repository:
#   python examples/quickstart.py [path]
# With no path it reads the sample in data/. Pass the full list from the latest release (.csv or .csv.gz) instead.
# Keeps agent-ready rows and calls the most recently tested one.
import csv
import gzip
import os
import re
import sys
import urllib.request

HERE = os.path.dirname(os.path.abspath(__file__))
path = sys.argv[1] if len(sys.argv) > 1 else os.path.join(HERE, "..", "data", "Spain_API_Endpoints_AgentPopulation_Sample.csv")
opener = gzip.open if path.endswith(".gz") else open
with opener(path, "rt", newline="", encoding="utf-8") as f:
    rows = list(csv.DictReader(f))

agent = [r for r in rows if "agent-ready" in r["tags"].split("|")]
# Newest test date first; URLs that describe a dataset or a service rather than return values go last.
DESCRIBES = re.compile(r"/erddap/info/|action-report\.json$|[?&]request=getcapabilities|/GeoArea/[^/?]+/List|getFullTableDownloadCSV|hub\.worldpop\.org", re.I)
agent.sort(key=lambda r: r["last_tested"], reverse=True)
agent.sort(key=lambda r: 1 if DESCRIBES.search(r["url"]) else 0)
print(len(rows), "rows,", len(agent), "agent-ready")
if not agent:
    sys.exit(0)

row = agent[0]
req = urllib.request.Request(row["url"], headers={"User-Agent": "agent-example/1.0"})
try:
    with urllib.request.urlopen(req, timeout=15) as res:
        body = res.read(1_000_000).decode("utf-8", "replace")
        print(res.status, res.headers.get("Content-Type"))
        print(body[:300])
except Exception as err:
    print(f"did not answer now; last passed {row['last_tested']} ({err})")
```

</details>

### JavaScript

Reads the sample as JSON because the CSV has quoted commas.

<details>
<summary>The code</summary>

```js
// Node 18+. Reads the sample as JSON (the CSV has quoted commas), local file first.
import fs from 'node:fs';

const FILE = 'data/Spain_API_Endpoints_AgentPopulation_Sample.json';
const rows = fs.existsSync(FILE)
  ? JSON.parse(fs.readFileSync(FILE, 'utf8'))
  : await (await fetch('https://raw.githubusercontent.com/agentpopulation/8.1k-spain-apis-for-agents/main/data/Spain_API_Endpoints_AgentPopulation_Sample.json')).json();

const row = rows.find((r) => r.tags.includes('agent-ready'));
const res = await fetch(row.url, { headers: { 'User-Agent': 'agent-example/1.0' }, signal: AbortSignal.timeout(15000) });
console.log(res.status, (await res.text()).slice(0, 300));
```

</details>

### Agent tools

[examples/agent-tools.json](examples/agent-tools.json) holds two tool definitions in the shape most tool-calling APIs accept (name, description, JSON Schema); rename `parameters` if yours uses another key. [examples/quickstart.mjs](examples/quickstart.mjs) implements them:

- `find_endpoints` searches the agent-ready rows of the list by words (their format is json). When you load the tools of more than one pack, prefix the names (for example `spain_find_endpoints`) so they do not clash.
- `fetch_endpoint` calls one URL, **refuses any URL that is not in the list** and does not follow redirects. The allowlist is built from the CSV, so a URL injected into a prompt is refused.

The same two tools can sit behind an MCP server.

## Test it yourself

Re-test endpoints from the sample with the same rule: HTTP 2xx and a non-empty body that is not an HTML page. Node 18+, no packages.

```bash
node tools/test-endpoints.mjs
```

It tests the first 50 URLs and prints one line: tested, passed, did not pass. Options: a `.csv` or `.csv.gz` path (the full list from the release), `--limit 50`, `--timeout-ms 10000`, `--out results.csv`. The results file holds `url`, `status`, `passed`, `content_type`, `ms` and `checked_at`; a status of `timeout` or `error:<code>` means no HTTP answer came back. It is polite: GET only, no key sent, at most 4 requests in flight, one at a time per listed host, at least 1 second between requests to one listed host, and reading stops once 256 kB of a body is kept. Redirects are followed and may lead to another host. `results.csv` is in `.gitignore`.

## Preview

One row from each of the five largest services among rows that match the focus rule, services with rows that return values first.

| Title | Service | Country | Format | Tested | Link |
|---|---|---|---|---|---|
| Indicadores demográficos. Grandes comarcas de Canarias. 01/… | Datos Abiertos de Canarias | ES | json | 2026-11-16 | [datos.canarias.es](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) |
| 1996 | ArcGIS Online layers (services-eu1.arcgis.com, org C3HgCqjBMl1pyvzK) | ES | json | 2026-11-16 | [services-eu1.arcgis.com](https://services-eu1.arcgis.com/C3HgCqjBMl1pyvzK/ArcGIS/rest/services/1996/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |
| 407\_JACUAPA\_WSL1 | ArcGIS Online layers (services-eu1.arcgis.com, org HuGcP11ciutroljg) | ES | json | 2026-11-16 | [services-eu1.arcgis.com](https://services-eu1.arcgis.com/HuGcP11ciutroljg/ArcGIS/rest/services/407_JACUAPA_WSL1/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |
| ÁMBITO\_DE\_ESTUDIO | ArcGIS Online layers (services-eu1.arcgis.com, org LYlXCI0Cv1tEOvkM) | ES | json | 2026-11-16 | [services-eu1.arcgis.com](https://services-eu1.arcgis.com/LYlXCI0Cv1tEOvkM/ArcGIS/rest/services/%C3%81MBITO_DE_ESTUDIO/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |
| AREAS\_CRITICAS\_AGUILA\_IMPERIAL1 | ArcGIS Online layers (services-eu1.arcgis.com, org LVA9E9zjh6QfM7Mo) | ES | json | 2026-11-16 | [services-eu1.arcgis.com](https://services-eu1.arcgis.com/LVA9E9zjh6QfM7Mo/ArcGIS/rest/services/AREAS_CRITICAS_AGUILA_IMPERIAL1/FeatureServer/0/query?where=1%3D1&outFields=*&resultRecordCount=10&f=json) |

Browse the 1,000-row sample: [Sample CSV](data/Spain_API_Endpoints_AgentPopulation_Sample.csv) · [Sample JSON](data/Spain_API_Endpoints_AgentPopulation_Sample.json).

## What's inside

<p align="center"><img src="assets/breakdown.svg" width="100%" alt="Top categories and formats in this pack"></p>

<details>
<summary>Categories: top 8</summary>

| Category | Endpoints | |
|---|---:|---|
| Government & Open Data | 3,738 | `████████████████████` |
| Navigation & Geo/Maps | 2,041 | `██████████▉` |
| Statistics & Economy | 1,376 | `███████▍` |
| Health | 548 | `██▉` |
| Weather & Climate | 142 | `▊` |
| Transport & Mobility | 100 | `▌` |
| Environment | 72 | `▍` |
| Energy | 44 | `▎` |

</details>

Formats: json 6,134 · xml 1,091 · csv 914

<details>
<summary>Largest services: top 25 of 141</summary>

| Service | Host | Endpoints | Keyless JSON | |
|---|---|---:|---:|---|
| Datos Abiertos de Canarias | datos.canarias.es | 3,810 | 1,805 | `████████████████████` |
| ArcGIS Online layers (services-eu1.arcgis.com, org C3HgCqjBMl1pyvzK) | services-eu1.arcgis.com | 864 | 864 | `████▌` |
| ArcGIS Online layers (services-eu1.arcgis.com, org HuGcP11ciutroljg) | services-eu1.arcgis.com | 566 | 566 | `███` |
| ArcGIS Online layers (services-eu1.arcgis.com, org LYlXCI0Cv1tEOvkM) | services-eu1.arcgis.com | 376 | 376 | `██` |
| ArcGIS Online layers (services-eu1.arcgis.com, org LVA9E9zjh6QfM7Mo) | services-eu1.arcgis.com | 320 | 320 | `█▋` |
| ArcGIS Online layers (services-eu1.arcgis.com, org XDTEoosVb6mbI5ee) | services-eu1.arcgis.com | 253 | 253 | `█▍` |
| ArcGIS Online layers (services-eu1.arcgis.com, org HJZ4IZB6mQFqe0lK) | services-eu1.arcgis.com | 125 | 125 | `▋` |
| ArcGIS Online layers (services-eu1.arcgis.com, org huF49oYTagCpb797) | services-eu1.arcgis.com | 119 | 119 | `▋` |
| ArcGIS Online layers (services-eu1.arcgis.com, org JyY1Tfb8ShrMQIdE) | services-eu1.arcgis.com | 106 | 106 | `▌` |
| ArcGIS Online layers (services-eu1.arcgis.com, org Y0im5hxYVxvfLOro) | services-eu1.arcgis.com | 95 | 95 | `▌` |
| Castillalamancha | geoservicios.castillalamancha.es | 74 | 74 | `▍` |
| ArcGIS Online layers (services-eu1.arcgis.com, org 3Xgxip3BoxrYTPj9) | services-eu1.arcgis.com | 70 | 70 | `▍` |
| ArcGIS Online layers (services-eu1.arcgis.com, org 6qu067tjnBgX8DW4) | services-eu1.arcgis.com | 61 | 61 | `▍` |
| ArcGIS Online layers (services-eu1.arcgis.com, org GlbwYH8qvpzNZno5) | services-eu1.arcgis.com | 58 | 58 | `▎` |
| ArcGIS Online layers (services-eu1.arcgis.com, org Et0t50k0BIgKUuLE) | services-eu1.arcgis.com | 49 | 49 | `▎` |
| Ign | serviciosgis.ign.es | 48 | 48 | `▎` |
| ArcGIS Online layers (services-eu1.arcgis.com, org UrtTdLP2PYSxwtI6) | services-eu1.arcgis.com | 45 | 45 | `▎` |
| ArcGIS Online layers (services-eu1.arcgis.com, org WCEIifo5j3luTcRc) | services-eu1.arcgis.com | 45 | 45 | `▎` |
| ArcGIS Online layers (services-eu1.arcgis.com, org 9OdsxSwES8vNXRId) | services-eu1.arcgis.com | 41 | 41 | `▎` |
| ArcGIS Online layers (services-eu1.arcgis.com, org E6YomoZj1vqGepVM) | services-eu1.arcgis.com | 40 | 40 | `▎` |
| Rivasciudad | sit.rivasciudad.es | 40 | 40 | `▎` |
| ArcGIS Online layers (services-eu1.arcgis.com, org gInnN1cT3lT7tET2) | services-eu1.arcgis.com | 37 | 37 | `▎` |
| ArcGIS Online layers (services-eu1.arcgis.com, org LZ34GBXK59x9Cuz1) | services-eu1.arcgis.com | 34 | 34 | `▏` |
| ArcGIS Online layers (services-eu1.arcgis.com, org WlVt7XtJWxCz9XOk) | services-eu1.arcgis.com | 33 | 33 | `▏` |
| ArcGIS Online layers (services-eu1.arcgis.com, org KmoBn3Qii9gbOa4C) | services-eu1.arcgis.com | 31 | 31 | `▏` |

</details>

<details>
<summary>Rows per test date: 16 Nov 2026</summary>

| Date (IST) | Endpoints | |
|---|---:|---|
| 2026-11-16 | 8,139 | `████████████████████` |

</details>

## Files

| File | Rows | Size | Use |
|---|---:|---:|---|
| [data/Spain_API_Services_AgentPopulation.csv](data/Spain_API_Services_AgentPopulation.csv) | 141 | 9.3 kB | One row per service with its endpoint count in this pack |
| [data/Spain_API_Endpoints_AgentPopulation_Sample.csv](data/Spain_API_Endpoints_AgentPopulation_Sample.csv) | 1,000 | 362.2 kB | The sample: focus-rule rows first, each service in proportion to its share; ArcGIS Online layers count as one service |
| [data/Spain_API_Endpoints_AgentPopulation_Sample.json](data/Spain_API_Endpoints_AgentPopulation_Sample.json) | 1,000 | 545.0 kB | The same rows as JSON, tags as an array |
| [Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz](https://github.com/agentpopulation/8.1k-spain-apis-for-agents/releases/latest) | 8,139 | 213.5 kB | The full list, gzipped CSV: a download from the latest release, checked by `SHA256SUMS.txt` |
| [tools/test-endpoints.mjs](tools/test-endpoints.mjs) | | | Re-tests endpoints from the sample or the full list |

Sample size: 1,000 rows, which is 1,000 or one third of the pack rounded down, whichever is smaller. Rows that match the focus rule come first. Each service gets rows in proportion to its share of those rows, at least one for the largest services and at most 50% of the sample while other services have rows; ArcGIS Online layers count as one service, whatever their organisation. Within a service, agent-ready rows, rows that return values and the newest test dates come first, and rows are written in turn across services. Service root addresses are placed at the end of the sample.

Full list: download `Spain_API_Endpoints_AgentPopulation_Snapshot_2026-11-16.csv.gz` (8,139 rows, 213.5 kB) from [releases/latest](https://github.com/agentpopulation/8.1k-spain-apis-for-agents/releases/latest), then gunzip it and pass its path. The scripts also read the `.csv.gz` as it is.

Excel users: Data > From Text/CSV, UTF-8. Files are UTF-8 without a byte-order mark and comma-separated.

## Columns and tags

<details>
<summary>Columns, types and tags</summary>

| Column | Type | Example | Meaning |
|---|---|---|---|
| url | string | [https://datos.canarias.es/api/estadisti…](https://datos.canarias.es/api/estadisticas/geographical-resources/indicadoresdemograficos/ows?service=WFS&version=1.1.0&request=GetFeature&typeName=Grandes%20comarcas-20230101&outputFormat=application/json) | The address that was tested |
| title | string | Indicadores demográficos. Grandes comar… | Station, dataset or feed name |
| service | string | Datos Abiertos de Canarias | The service the endpoint belongs to; joins to the services file together with host |
| host | string | datos.canarias.es | Host name of the address |
| country | string | ES | ISO 3166-1 alpha-2 code, or EU; empty when global or unknown |
| category | string | Government & Open Data | Category of the endpoint |
| subcategory | string |  | Left empty from the 15 Nov 2026 snapshot; kept so the columns stay the same |
| format | string | json | What the test call returned: json, csv, geojson, xml, gtfs, zip, txt and so on |
| tags | string | `no-key\|json\|agent-ready` | Tags separated by \| |
| last_tested | date | 2026-11-16 | Date of the test call, YYYY-MM-DD (IST) |

| Tag | Rows | Meaning |
|---|---:|---|
| no-key | 8,139 | No key was sent in the test call |
| agent-ready | 6,134 | No key sent, JSON body, passed a data call on last_tested |
| json | 6,134 | Format of the body |
| xml | 1,091 | Format of the body |
| csv | 914 | Format of the body |

A machine-readable copy of this dictionary is in [datapackage.json](datapackage.json).

</details>

## Known limits

- 4,329 rows are map-layer queries with resultRecordCount set: the tested call asked for a few records; change the query to get the full layer.
- 4,152 rows are layers on ArcGIS Online, where anyone can publish: some are class projects, tests or copies. Check the owner and the fields before you rely on one. Layers whose titles read as a test, draft or copy are not used as starting points; named organisations come first in the recommended lists.
- 68 rows have a title that reads as a test, a draft, a copy or a sample; they are not used as starting points.
- The country code (ES) is the code the endpoint is filed under, not the place the data covers and not always the publisher's country. Where a row had no code, the code of its ArcGIS organisation is used when that organisation lists one country only. This pack holds only rows on the EU-region ArcGIS Online host and rows on hosts that are not hosted ArcGIS; the other rows coded ES, mostly Spanish-language layers about Latin America, are left out of it. In a sample of 40 of its titles read before release, none was about a place outside Spain. Filter by title or service if you need data about one place.
- Stations and feeds can go quiet after their test date; re-test a URL before you rely on it.
- Not in this pack: endpoints that need a key or a POST, and URLs that did not pass.
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

## Licence and credit

> [!IMPORTANT]
> This list (URLs, titles, tags and test results) is © 2026 AgentPopulation, released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Credit AgentPopulation and link agentpopulation.com. The data each endpoint returns belongs to its provider and stays under that provider's terms; this licence does not cover it.

Copy-ready credit:

`Spain API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 16 Nov 2026.`

GitHub's "Cite this repository" button reads [CITATION.cff](CITATION.cff).

<!-- agentpopulation:start -->
## Part of 10M API endpoints for AI agents

This pack is one of the 50 topic packs of [10m-open-apis-for-ai-agents](https://github.com/agentpopulation/10m-open-apis-for-ai-agents), the open collection by [AgentPopulation](https://agentpopulation.com). Target: 10 million+ open API endpoints that pass a keyless API call.

AgentPopulation's test run of 16 Nov 2026: 4,452,803 tested, 3,346,053 passed a data call. This is the Spain pack: 8,139 endpoints from 141 services, none of them in a pack read from the earlier snapshot, by address or as another address of the same map layer. Packs overlap, so an endpoint can appear in more than one.

For the latest tested endpoints, search [agentpopulation.com/apis](https://agentpopulation.com/apis). This pack is a snapshot from 16 Nov 2026.

Sibling packs that share the most URLs with this one: [59k-europe-region-arcgis-apis-for-agents](https://github.com/agentpopulation/59k-europe-region-arcgis-apis-for-agents) (4,152 shared) · [25k-arcgis-server-apis-for-agents](https://github.com/agentpopulation/25k-arcgis-server-apis-for-agents) (177 shared). The rest are listed in [10m-open-apis-for-ai-agents](https://github.com/agentpopulation/10m-open-apis-for-ai-agents).

Questions, pack requests, reports of endpoints that stopped answering and requests to remove a row go to [Discussions](https://github.com/agentpopulation/10m-open-apis-for-ai-agents/discussions), or to [@agentpopulation](https://x.com/agentpopulation) on X. The packs are a work in progress and corrections are welcome.

Spotted a wrong row or a dead URL? Tell us on X: [@agentpopulation](https://x.com/agentpopulation).

If this pack saved you time, a star helps others find it.

---

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · [10m-open-apis-for-ai-agents](https://github.com/agentpopulation/10m-open-apis-for-ai-agents)

<!-- agentpopulation:end -->
