UK Micro-entity Accounts Tool — Vercel deployment v27

Static interface: index.html, app.js, template.xhtml
Companies House lookup: api/company.js (Vercel Node Function)

Deploy this directory to the Vercel project uk-micro-entity-accounts-tool.
The app fetches the company name from Companies House via the serverless API. The user enters the balance-sheet date; filing dates are not fetched.
Generated iXBRL remains in the user's browser and is downloaded locally.
Blank direct-input rows are omitted when blank for both years and receive no numeric facts. Entered zeroes remain visible and tagged. Calculated subtotals treat blank inputs as zero.
Generated reports reference the FRC FRS 102 2024 taxonomy suite. Amounts display with thousands separators while remaining inline XBRL numeric facts.
Only entered approving directors are included in the generated accounts; each signature slot is updated or removed by its fixed template ID, and the generated XHTML is checked for blank director lines.

The project includes package.json with type=commonjs so api/company.js is not affected by a parent Downloads/package.json setting.
