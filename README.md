# ExamShield — ISMS consultancy

A fictional digital examination and academic assessment service used to design a risk-based information security management programme aligned with ISO/IEC 27001:2022 and UK data protection requirements. Confidential examination questions, academic result integrity and service availability drive the design.

## Repository structure

| Directory | Purpose |
|---|---|
| `prototype/` | Original offline HTML workflow demonstrator |
| `architecture/` | Five editable Graphviz DOT diagrams |
| `tests/` | Browser interaction test runner and original automated test records |
| `docs/` | Design scope, evaluation and implementation priorities |
| `private-evidence/` | Local-only workbooks, governance and assessment evidence (excluded from Git by default) |

## Run the demonstration

Open `prototype/index.html` in a modern browser. Choose a synthetic persona and enter the public demonstration code `246810`. No server, database, real account or personal information is required. Use Reset demonstration to clear session data.

## Run interaction checks

```sh
python -m venv .venv
# Activate the virtual environment for your operating system
python -m pip install -r tests/requirements.txt
python -m playwright install chromium
python tests/run_prototype_checks.py
```

Generated results and screenshots appear in `tests/generated/`. The runner uses an available system Chromium or Playwright Chromium. Existing results document the original offline workflow test, not production security testing.

## Render architecture diagrams

Install Graphviz and render a diagram with, for example:

```sh
dot -Tsvg architecture/03_TO_BE.dot -o to-be.svg
```

## Evidence and boundaries

The consultancy model includes 25 identified risks, 30 requirements and a draft 93-control Annex A applicability review. Original browser checks recorded 13 passes. The manual walkthrough demonstrated six screens, with 38 session events and 17 denials; these are simulated workflow observations. Three discussion-based exercises address question leakage, ransomware and grade modification. Neither the application nor the ISMS is deployed, independently audited or certified. Target residual risks and recovery objectives are estimates. All demo data is synthetic.

The full assessment documents, participant records, student identifiers, and course materials must not be published publicly. Keep those materials private and retain accurate attribution and required AI-use disclosure. The repository is a design/evidence portfolio, not production software.
