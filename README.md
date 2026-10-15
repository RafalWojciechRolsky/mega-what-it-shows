# what it shows — the desk's tickets for #4471

MEGA.dev S01E03. The support desk merged 412 reports into ticket #4471 the night of the
03:12 job and closed it: "one issue, one fix, no follow-ups." The kb export shows three
issues. This repo is where the missing tickets live.

- `support-kb/` — the kb export as the desk shipped it
- `support-kb/src/routes/kb/incidents/4471-split/+page.svx` — the page added to the kb
- `support-kb/src/routes/kb/incidents/4471-split/rendered.html` — the same page as the desk sees it rendered
- Issues — one ticket per issue found in #4471

The issues found (by the kb's own `fingerprint.ts`: reporter's place + server code):

| fingerprint | reports | what it is |
|---|---|---|
| `sched-prod:E-TZ-114` | 349 | the ticket's own issue — shifts an hour late, fixed by change #29 |
| `tram-3:E-TZ-114` | 44 | departure boards an hour behind — merged, no ticket of its own |
| `rota-6:E-SYNC-04` | 19 | night rota duplicated an hour apart — merged, no ticket of its own |

The export holds 427 rows for 412 reports (15 overlapping-page duplicates), and R-41200 —
the 03:12 job's own "status: clean" output — was merged as if it were a report.
