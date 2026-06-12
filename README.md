# Protein Sequence Analyzer

A single-page, browser-based protein analysis tool. Paste an amino-acid
sequence — raw, line-wrapped, or FASTA (single or multiple records) — and get
physicochemical properties that match [Expasy ProtParam](https://web.expasy.org/protparam/):

- Length, molecular weight (Da / kDa), theoretical pI
- Instability index (with stable/unstable verdict), aliphatic index, GRAVY
- Net charge at pH 7, charged-residue counts, extinction coefficients
- Full amino-acid composition table
- Interactive **net charge vs pH** curve with the pI marked

Everything runs **client-side** — no server, no build step, no data leaves your
device. It works offline once loaded.

## Live site

Once Pages is enabled, the app is served at the repository's GitHub Pages URL.

## Methods

Calculations use the same constants as Expasy ProtParam:

- **pI / charge** — Bjellqvist pK values, Henderson–Hasselbalch summation
- **Instability index** — Guruprasad dipeptide weight values (DIWV)
- **Hydropathy (GRAVY)** — Kyte–Doolittle scale
- **Molecular weight** — average residue masses + one water
- **Extinction coefficient** — Tyr/Trp/cystine contributions at 280 nm

## Usage

Just open `index.html` in any browser, or visit the hosted page. To use on a
phone, add the page to your home screen for an app-like launcher.
