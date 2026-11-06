# US companies worth $1 billion or more that delisted (Oct 2021 – Oct 2026)

473 companies that left the NYSE, Nasdaq or NYSE American, each with what happened to it: acquired, taken private, merged, moved abroad or other. Includes the buyer, payment type, deal terms and value, announcement and closing dates, a one-line summary, a source link, and SEC EDGAR data (CIK, SIC industry code, state of incorporation, and the Form 25 delisting notice).

Full write-up with charts: **[Delisted Stocks Report](https://www.quotelinks.com/delisted-stocks-report.html)** by [Quotelinks](https://www.quotelinks.com/).

## File

`delisted_companies.csv`: one row per company, UTF-8, comma-separated.

| column | description |
|---|---|
| symbol | Ticker before delisting |
| company | Company name |
| exchange | NYSE, Nasdaq or NYSE American |
| year | Year the company left: deal closing date if known, else SEC Form 25 filing, else last trading day (2021 from Oct 18; 2026 through October) |
| outcome | acquired, taken_private, merged, left_us_exchange, other |
| buyer | Buyer or merger partner |
| payment | cash, stock, cash_and_stock (blank if n/a or unknown) |
| terms | Per-share deal terms as announced |
| deal_value | Deal value as reported (original wording) |
| deal_value_usd_bn | deal_value in billions of USD (blank if none or non-USD; some include debt) |
| announced | Month announced (YYYY-MM) |
| closed | Date closed (YYYY-MM-DD) |
| summary | One-sentence summary |
| source_url | News article or press release confirming the outcome |
| cik | SEC Central Index Key |
| sic_code, sic_description | SEC Standard Industrial Classification |
| state_of_incorporation | Per SEC EDGAR |
| form25_type, form25_date, form25_url | SEC Form 25 delisting notice closest to the last trading day (blank if none found) |

## Method

- Universe: common stocks and ADRs delisted from the NYSE, Nasdaq or NYSE American between October 18, 2021 and October 2026 whose market value on the last trading day was at least $1 billion.
- Excluded: ticker changes and renames where the same company kept trading, share-class consolidations, duplicate share classes of one company (one row per company), and bad records.
- Outcomes, buyers and deal terms were researched from company press releases and news coverage; `source_url` links to the confirming source. Deals completed in 2026 are less thoroughly checked.
- SEC fields come from the EDGAR submissions API. No Form 25 is listed where the company left through another route (for example foreign ADR programs) or none was filed within the search window.
- Prices and market values are not included.

## License

- Quotelinks research fields: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please credit "Quotelinks" with a link to https://www.quotelinks.com/delisted-stocks-report.html.
- SEC EDGAR fields (cik, sic_code, sic_description, state_of_incorporation, form25_*): US government data, public domain.

Not investment advice. Corrections welcome via issues.
