# Luvaminos lot test results

*Published by Luvaminos, a US research peptide supplier. This is a first-party dataset about our own products, not an independent source.*

One row per lot: the laboratory's identity and purity results, the lab's accession number, and the links you need to check every row with the lab yourself.

- **Data file:** [`lots-public.csv`](lots-public.csv) (UTF-8, comma-separated, one header row)
- **Rows:** 17 lots, read from the pages at https://www.luvaminos.com/coa and the lab PDFs on 2026-11-01. The full certificate library is on that page
- **Laboratory:** Freedom Diagnostics Testing, PLLC, Franklin, Tennessee. The lab is not owned by or affiliated with Luvaminos.
- **Licence:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Reuse it, including commercially, with attribution: "Luvaminos lot test results, https://github.com/luvaminos/lot-test-results".

## What this is, and what it is not

This is **published by Luvaminos, not an independent source.** We sell every product in this file. The numbers in it come from an outside laboratory, and each row can be checked against the lab's own copy of the report, which is the point of publishing the accession numbers. If a row here ever disagrees with the lab's copy, the lab's copy is right and this file is wrong; please open an issue.

The file covers lots sold under their compound names. Lots of products we sell under coded names are not included.

## Columns

| Column | Meaning |
|---|---|
| `lot` | Our lot number, as printed on the vial and on the lab report |
| `product` | Product name |
| `label_on_certificate` | The amount the lab report states for the sample (for blends, per component) |
| `store_vial_size` | The vial size we sell this lot as |
| `hplc_purity_pct` | HPLC purity, area percent, as reported (for blends, the single combined figure the lab reports) |
| `identity` | The lab's identity result |
| `identity_method` | The method line from the lab report |
| `received_date` | Date the lab received the sample (ISO 8601) |
| `reported_date` | Date the lab issued the report. This is the "tested" date shown on our lot pages |
| `lab` | Testing laboratory |
| `accession` | The lab's accession number for the report |
| `lab_search_code` | The code to type into the lab's lookup: `Luva` + accession |
| `lab_pdf_url` | The lab's own copy of the report, served from the lab's domain |
| `luvaminos_coa_page` | Our page for the lot |
| `luvaminos_pdf_url` | Our PDF copy of the report |
| `luvaminos_research_page` | The compound's research summary page on luvaminos.com |
| `source_read_date` | Date the row was read from the live pages and the lab PDF |
| `notes` | Anything a reader needs to interpret the row |

## How to verify any row at the lab

1. Copy the row's `lab_search_code` (for example `Luva2608311071`).
2. Open the lab's lookup page, https://freedomdiagnosticstesting.com/search-for-your-coa-based-on-the-unique-accession-number/, and search that code. Search by code only; a company-name search returns a list rather than the one report.
3. Or open `lab_pdf_url` directly. It is served by the lab, not by us.
4. Compare the lab's report with the row: client (Luvaminos LLC), `lot`, `hplc_purity_pct`, and the received and reported dates. The report also prints net content against the label.
5. Optional: open `luvaminos_coa_page` and compare our copy with the lab's. They should be identical; we do not edit lab reports.

## How to read the numbers

- **HPLC purity** is the share of the UV-detected peak area that belongs to the main compound. It describes how clean the material is, not how much of it is in the vial.
- **Net content** is how many milligrams of the compound the lab measured. Freeze-dried powders also contain water and salt counterions, which are not counted. Every lab report prints it beside the label amount.
- **Identity "Confirmed"** means the lab found the expected mass by mass spectrometry. For blends, each named component was found.
- Two rows are not peptides: NAD+ (a dinucleotide) and 5-Amino-1MQ (a small molecule). The lab's template still calls the field "net content".

## What these results do not cover

- Vials other than the one sampled. A lot number ties your vial to its report.
- Stability after `reported_date`.
- Sterility, endotoxin, heavy metals or any test not listed. When extra panels are run, they are on that lot's certificate; none of the rows here includes one.
- Any use. These are laboratory research materials, not for human or veterinary consumption.

## Updates

New rows are added when a new lot's report is published. Rows are never edited after publication except to correct a transcription error, which is recorded in the commit message. Sold-through lots stay in the file.

## Citation

> Luvaminos LLC (2026). *Luvaminos lot test results* [Data set]. Published by the vendor (first-party). Laboratory: Freedom Diagnostics Testing, PLLC. https://doi.org/10.5281/zenodo.23572125

The Zenodo DOI record https://doi.org/10.5281/zenodo.23572125 holds version 2026-10 (10 lots), a fixed copy. This repository is the current working copy.

Contact: support@luvaminos.com. We reply by email within a day.
