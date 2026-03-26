# RefCheck Pro

**Verify academic references against CrossRef, PubMed & OpenAlex — fix errors with one click, read abstracts, download corrected drafts.**

🔗 **[Use it now →](https://nethahussain.github.io/refcheck-pro/)**

---

## What it does

RefCheck Pro takes a manuscript (.docx or .txt), splits it into sentence + reference blocks, and verifies every cited reference against three major academic databases simultaneously. It catches hallucinated references, wrong years, author mismatches, and incorrect journal names.

### Features

- **Upload & parse** — supports Vancouver `[1]`, APA `(Author, 2020)`, Harvard, parenthetical `(1)`, and numbered citation styles
- **Verify all references** — checks each reference against CrossRef, PubMed, and OpenAlex in parallel (~1 sec/ref)
- **Spot errors** — flags year mismatches, author discrepancies, wrong journal names, and unfound references
- **One-click fix** — when a verified match is found, apply the corrected reference with a single click
- **Read abstracts** — view the abstract of any cited paper to verify it supports the claim in your text
- **Edit text** — rewrite any sentence directly in the tool after reviewing the abstract
- **Download corrected .docx** — export the full manuscript with all fixes applied

### Three views

| Tab | What it shows |
|-----|--------------|
| **Sentences** | Each sentence paired with its cited references — click to verify and read abstracts |
| **References** | Full reference list with verification status, DOI/PubMed/OpenAlex links |
| **Flagged** | Only problematic references — fix them one by one |

---

## How to use

1. Go to **[nethahussain.github.io/refcheck-pro](https://nethahussain.github.io/refcheck-pro/)**
2. Upload your manuscript (.docx or .txt)
3. Click **Verify all**
4. Review flagged references — click **Fix** to correct, **Show abstract** to read the source
5. Edit sentence text if needed
6. Click **Download corrected .docx** when done

---

## How it works

Everything runs **client-side in your browser** — no files are uploaded to any server.

**APIs used (all public, no keys needed):**
- [CrossRef](https://www.crossref.org/) — DOI resolution, metadata, abstracts
- [PubMed / NCBI E-utilities](https://www.ncbi.nlm.nih.gov/home/develop/api/) — biomedical literature search and abstracts
- [OpenAlex](https://openalex.org/) — open scholarly metadata and abstracts

**Libraries:**
- [mammoth.js](https://github.com/mwilliamson/mammoth.js/) — .docx text extraction
- [docx](https://github.com/dolanmiri/docx) — .docx generation for download
- [FileSaver.js](https://github.com/nicubunu/FileSaver.js) — client-side file download

---

## Citation styles supported

| Style | In-text example | Reference format |
|-------|----------------|-----------------|
| Vancouver | `[1]`, `[1-3]`, `[1, 4, 7]` | Numbered with period or bracket |
| Parenthetical numbered | `(1)`, `(3-5)`, `(8, 17-19)` | Numbered (e.g. EndNote) |
| APA | `(Smith, 2020)`, `(Smith et al., 2020)` | Author-date |
| Harvard | `(Smith 2020)` | Author-date variant |
| Narrative | `Smith (2020)`, `Smith et al. (2020)` | Author-date in running text |

---

## Self-hosting

It's a single HTML file. To run locally:

```bash
# Clone
git clone https://github.com/nethahussain/refcheck-pro.git
cd refcheck-pro

# Open directly
open index.html

# Or serve locally
python3 -m http.server 8765
# Then visit http://localhost:8765
```

---

## License

MIT
