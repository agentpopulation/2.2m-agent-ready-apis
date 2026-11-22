## Agent-ready API endpoints, snapshot 15 Nov 2026

- 2,248,987 endpoints passed a keyless data call, tested 10–15 Nov 2026 (IST)
- 64,426 services · 251 country codes · 2,248,987 keyless JSON rows

### Download

- `Agent_Ready_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz`: the full list, 2,248,987 rows, 75.2 MB gzipped (685.0 MB as CSV), SHA-256 `b157f3ab92dbcc30de86018e3c8b2c8d59709ddd06f033f7e805e5a9f5c0efbc`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Agent_Ready_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Agent_Ready_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 84,727 · Wrap one URL pattern per source as a tool (get_observation, get_river_level, get_forecast, get_metar): pass a station id, airport code or coordinates, return the value, its unit and its time, with a timeout.
- 📱 App features: 81,764 · Show what is near a user on a card or a map: bikes and docks at a station, the status of a transit line, open parking spaces or the air-quality reading, refreshed when the card opens.
- 🧠 Grounding and data pipelines: 187,547 · Load indicators and statistics tables on a schedule into your own store, so an agent answers with a figure, its period and the source URL.
- 🧪 Evals and testing: 2,248,987 · Run your agent against a fixed set of URLs from many services and topics; check that each JSON body parses into the fields your tools return, and keep last_tested as the baseline for your own re-tests.

### Changes

- First release: 2,518,343 endpoints from 65,954 services, tested 10–15 Nov 2026 (IST), snapshot 15 Nov 2026.
- Rebuilt under the same snapshot with the latest leave-out rules (other addresses of a left-out ArcGIS layer, teaching organisations, more class-layer, name and record rules): 2,248,987 endpoints from 64,426 services, 269,356 fewer endpoints than first published under this snapshot (2,518,343 from 65,954 services), tested 10–15 Nov 2026 (IST).
- Left out: 1,747 rows whose URL carried a credential-looking parameter or a login.
- Left out: 52 rows with a private or local address.
- Left out: 371 rows with an email-like address.
- Left out: 43,725 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 12 camera or image URLs (webcam and camera feeds, picture and video files).
- Left out: 110 ArcGIS proxy layers (utility.arcgis.com/usrsvcs and portal /sharing/servers/ addresses) that can call a service with a stored login.
- Left out: 1,240 class-exercise copies of the same few ArcGIS Online layers (Miami Beach sea level rise, high-risk areas without shelter, flooded areas, sea level rise and storm surge maps) across many organisations, many with a person's name in the title.
- Left out: 508 layers marked editable in the title (they can hold entries that people added).
- Left out: 73 police traffic-stop layers (they can hold details of people stopped).
- Left out: 7,384 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 118 rows that passed a data call only from a network location in India.
- Left out: 6 rows whose address or title held a token-like string, a private address or a similar string.
- Left out: 41,513 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 3,427 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 1,455 ArcGIS layers that are records about named people (employee, patient, client or donor lists, home addresses, voter lists, sex offender and missing person layers).
- Left out: 102,908 rows of server information from Mastodon, PeerTube, Lemmy, Nostr and other social network servers (instance documents name the server's contact person).
- Left out: 94 rows that are another address of an ArcGIS layer dropped for what it holds (one of the reasons above, found under another address of the layer).
- Left out: 4,124 rows of ArcGIS Online organisations that are class accounts (25 layers or more, at least 50% of them class or coursework layers): their other layers are students' work too.
- Left out: 72,999 rows of ArcGIS Online organisations that are class accounts (3 class sets or more in at least 20% of their rows, 10 class sets or more with no organisation name, or layers signed by students read by hand): their other layers are students' work too.
- Left out: 17,666 rows of class sets: one map layer saved under 5 or more students' initials or names in one ArcGIS Online organisation, or in 4 or more students' own organisations.
- Left out: 158,329 rows of the ArcGIS Online organisations of universities, colleges and schools (many of their layers are students' work).
- Left out: 1,883 rows that repeat an address already in the pack.
- Overlap: 117,939 of these URLs are also in 170k-weather-apis-for-agents.
- Overlap: 174,255 of these URLs are also in 240k-transit-apis-for-agents.
- Overlap: 208,038 of these URLs are also in 260k-water-apis-for-agents.
- Overlap: 87,229 of these URLs are also in 120k-finance-economy-apis-for-agents.
- Overlap: 32,406 of these URLs are also in 130k-india-apis-for-agents.
- Overlap: 886,888 of these URLs are also in 1.2m-government-open-data-apis.
- Overlap: 188,179 of these URLs are also in 270k-statistics-apis-for-agents.
- Overlap: 66,254 of these URLs are also in 84k-oceans-apis-for-agents.
- Overlap: 12,188 of these URLs are also in 22k-maritime-apis-for-agents.
- Overlap: 105,430 of these URLs are also in 160k-environment-apis-for-agents.
- Overlap: 9,831 of these URLs are also in 19k-air-quality-apis-for-agents.
- Overlap: 215,427 of these URLs are also in 350k-maps-gis-apis-for-agents.
- Overlap: 55,778 of these URLs are also in 84k-health-apis-for-agents.
- Overlap: 205,459 of these URLs are also in 380k-science-apis-for-agents.
- Overlap: 32,536 of these URLs are also in 40k-hazards-apis-for-agents.
- Overlap: 4,525 of these URLs are also in 4.9k-wildfire-apis-for-agents.
- Overlap: 46,465 of these URLs are also in 67k-energy-apis-for-agents.
- Overlap: 21,460 of these URLs are also in 23k-aviation-apis-for-agents.
- Overlap: 12,557 of these URLs are also in 22k-traffic-apis-for-agents.
- Overlap: 8,589 of these URLs are also in 10k-parking-apis-for-agents.
- Overlap: 5,639 of these URLs are also in 7.8k-earthquake-apis-for-agents.
- Overlap: 2,311 of these URLs are also in 4.2k-volcano-tsunami-apis-for-agents.
- Overlap: 16,074 of these URLs are also in 17k-bike-share-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 10–15 Nov 2026; snapshot 15 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 15 Nov 2026.

Credit: Agent-ready API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 15 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
