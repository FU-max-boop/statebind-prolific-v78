# StateBind Prolific Annotation UI

Public annotation pages for the StateBind human ambiguity pilots.

Participants read public coding-agent trajectory snippets and judge whether the observed next command/path is uniquely implied by the shown context.

Labels: `UNIQUE`, `ALT`, `UNCLEAR`.

## Pages

- `index.html`: v78 50-case pilot page. This was used for the first Prolific pilot and is kept unchanged for traceability.
- `v79.html`: compact 10-case pilot page. This is the recommended next pilot because it requires a Prolific ID, a label, confidence, and a short reason for every case before revealing the completion code.
- `v79_formsubmit.html`: contingency version of the compact 10-case pilot. It submits the compact TSV through an email form endpoint and only then redirects to the completion-code page.
- `v79_thanks.html`: static completion-code page used by the contingency submit flow.

## v79 Completion Code

The bundled v79 page uses completion code `C79BIND2`. If a new Prolific study uses a different completion code, regenerate `v79.html` from the research repo with:

```bash
python3 scripts/create_prolific_v79_compact_ui.py --completion-code YOUR_CODE
```

For the contingency submit flow, regenerate with:

```bash
python3 scripts/create_prolific_v79_formsubmit_ui.py --completion-code YOUR_CODE
```
