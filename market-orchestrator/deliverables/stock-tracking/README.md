# Stock Tracking

Keep one CSV per currently owned stock in this folder.

Filename pattern:

- `stock-name.csv`

Examples:

- `tcs.csv`
- `infosys.csv`

Rules:

- read the existing CSV before writing
- keep historical rows
- append one new row per company per date
- use ISO date format in the `date` column
- only track companies currently invested by the user
- create a new CSV only if the stock does not already have one
