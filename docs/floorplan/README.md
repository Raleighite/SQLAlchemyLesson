# Source Floorplan

Open [the offline map](index.html) after downloading it. GitHub may show HTML source rather than execute it. Use **Start here**, **Flows**, search and the details-panel toggle to read the architecture. On narrow screens the fit-to-view overview can be small; readable details/tour prose is the preferred path.

A script-only ORM lesson creates a user table, inserts three demonstration users and prints assigned IDs. There is no interactive menu, relationship implementation or HTTP service.

## Source boundary

No relationships or HTTP routes are implemented. A repeated script run can insert duplicates. Dependencies and database contents were not exercised.

Pinned original source: `ed6a9b7b851c00a7e92d956e27afb4ab0517f1e2`. Original project licensing is unchanged. See [notices](NOTICE.md), [omissions](source-census.json), [authoring](architecture.json) and [integrity pins](source-manifest.json). This is source documentation, not application execution, secure deployment approval or automatic refresh.

## Check without running the application

```sh
python3 docs/floorplan/check_freshness.py
python3 -B -m unittest discover -s docs/floorplan/tests -v
python3 -B -O -m unittest discover -s docs/floorplan/tests -v
```

The checker compares original source/config/static/input-file hashes and file membership, and all reviewed map artifacts. It does not regenerate on drift. Tests create disposable copies, never import the application, and require only Python standard library and Git. Regeneration requires a separately qualified renderer and reviewed authoring; its runtime is not bundled here.
