# Power System Planning Engineering Lab

An educational Python and OSeMOSYS project for learning, implementing, and testing power-system planning studies through progressively more realistic engineering challenges.

The repository combines power-system planning theory with software development practices: structured input data, reproducible OSeMOSYS models, Python automation, scenario analysis, resource adequacy assessment, risk evaluation, automated testing, and documented assumptions.

It is intended for engineers, planners, researchers, and students who want to understand both the planning methodologies and how to implement them using Python and OSeMOSYS.

**Status:** Educational project under active development. Do not use its results for regulatory, operational, investment, or real-world planning decisions without independent engineering validation.

---

## What you can do here

- Build and run OSeMOSYS models from first principles.
- Develop and automate planning workflows using Python.
- Create and analyse long-term capacity expansion studies.
- Investigate renewable energy integration challenges.
- Model energy storage technologies and storage-duration trade-offs.
- Study transmission constraints and regional planning concepts.
- Assess resource adequacy using industry reliability metrics.
- Explore uncertainty, scenario analysis, and risk assessment techniques.
- Learn through worked examples, engineering notes, tests, and documented assumptions.

---

## Repository guide

| Location | What it is for |
|-----------|-----------|
| `01_study_definition/` | Study objectives, planning mandates, project background, and high-level assumptions for the fictional planning system. |
| `02_model_inputs/` | OSeMOSYS input data, assumptions, reference datasets, and generated model inputs. |
| `03_planning_studies/` | Progressive planning studies that form the core learning journey of the repository. |
| `src/planning_lab/` | Python package containing model utilities, input/output functions, automation tools, calculations, analyses, and validation logic. |
| `tests/` | Automated tests for calculations, data loading, validation, and analysis workflows. |
| `docs/` | Engineering reference material, planning assumptions, worked examples, methodology notes, verification guidance, and recorded decisions. |
| `results/` | Generated outputs, study results, plots, reports, and analysis artefacts. |
| `pyproject.toml` | Python project metadata, package configuration, and test configuration. |

The model inputs, planning assumptions, Python code, and analysis outputs are maintained separately wherever practical. This makes it easier to inspect assumptions, understand calculations, and reproduce study results.

### Where should I start?

- **New to the repository?** Start here, then inspect `01_study_definition/` and `03_planning_studies/Study01_Generation_Expansion_Plan/`.
- **Want to understand the planning challenge?** Read `01_study_definition/study_brief.md`.
- **Want to understand the engineering assumptions?** Read `docs/study_basis.md`.
- **Need to understand the model inputs?** Explore `02_model_inputs/`.
- **Want to follow calculations by hand?** Read `docs/worked_examples.md`.
- **Want to understand how results are checked?** Read `docs/verification_checklist.md` and explore `tests/`.
- **Want to understand why a modelling decision was made?** Read `docs/engineering_decisions.md`.

Some files may be added as the project develops. If a path listed above is not yet present in the current branch, use the files that are available and treat the relevant documentation as planned or in progress.

---

## Prerequisites

You will need:

- **Git** to clone the repository.
- **Python 3.10 or later**.
- **pip**, included with standard Python installations, to install the project and its development tools.
- **OSeMOSYS**, the primary energy system optimisation framework used throughout the repository.
- An optimisation solver such as **GLPK** or **CBC**.
- A terminal and a code editor. VS Code or another Python-capable editor is suitable.

The project uses a `src/` package layout and is configured through `pyproject.toml`. The test suite uses `pytest`.

OSeMOSYS is the primary capacity-expansion modelling framework used throughout the repository.

---

## Setup

### 1. Clone the repository

Replace `<repository-url>` with the clone URL shown on the repository's GitHub page.

```bash
git clone <repository-url>
cd power-system-planning-engineering-lab
```

If you already have the repository locally, change into its root directory instead.

### 2. Create a virtual environment

A virtual environment keeps this project's Python packages separate from other Python projects.

**Linux / macOS**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows PowerShell**

```powershell
py -3 -m venv .venv
.venv\Scripts\Activate.ps1
```

If your system does not have the required Python version, install Python 3.10 or later before continuing.

### 3. Install the project

This repository assumes OSeMOSYS is installed and operational.

Follow the official OSeMOSYS installation instructions relevant to your operating system and preferred workflow.

Install an optimisation solver such as:

- GLPK
- CBC

Verify that the solver is accessible from your system before attempting to run any planning studies.

Many studies within this repository depend on a functioning OSeMOSYS installation and optimisation backend.

With the virtual environment activated, run:

```bash
python -m pip install --upgrade pip
python -m pip install -e .
```

The editable install makes the package importable from the development checkout without repeatedly reinstalling it after every source-code change.

### 4. Install the test tool

If `pytest` is not already installed in the virtual environment, install it:

```bash
python -m pip install pytest
```

The repository's `pyproject.toml` configures pytest and project settings.

**Dependency note:** If the project later declares development dependencies or optional development extras in `pyproject.toml`, prefer installing those declared dependencies rather than maintaining a separate manual list.

---

## Run the project

Run commands from the **repository root**, unless a command says otherwise.

### Run the first planning study

The repository includes planning studies that progressively develop a long-term electricity plan.

Example:

```bash
python 03_planning_studies/Study01_Generation_Expansion_Plan/run_study.py
```

This study should load the required inputs, run the workflow, and generate study outputs. If it fails, check that you are in the repository root, that the expected input files are present, and that the package has been installed in the active virtual environment.

### Run the automated tests

Run the full test suite:

```bash
python -m pytest
```

For a more detailed report:

```bash
python -m pytest -v
```

Run a single test file when working on a particular feature:

```bash
python -m pytest tests/test_input_validation.py
```

Test filenames and available test modules may evolve as the project grows. Use:

```bash
pytest --collect-only -q
```

to see which tests pytest currently discovers.

### Deactivate the virtual environment

When you are finished:

```bash
deactivate
```

To return to the project later, open a terminal in the repository and activate `.venv` again.

---

## Typical development workflow

- **Understand the planning problem.** Read the relevant engineering notes and identify the study objectives, assumptions, and constraints.
- **Inspect the model inputs.** Review the relevant datasets, parameters, and assumptions before making changes.
- **Implement one small improvement.** Keep planning logic and calculations within the Python package rather than duplicating them in scripts.
- **Write or update tests.** Cover expected results, boundary conditions, and invalid inputs where appropriate.
- **Run the tests.** Use `python -m pytest` before committing.
- **Document meaningful changes.** Update the relevant document in `docs/` when assumptions, methodologies, supported inputs, or model behaviour change.

A useful learning loop for this repository is:

**Learn → Model → Optimise → Analyse → Challenge → Validate → Document**

---

## Working with Git

Check the current working tree:

```bash
git status
```

Review the changes:

```bash
git diff
```

Stage and commit a change:

```bash
git add <path-to-file>
git commit -m "Describe the change"
```

Push your branch to GitHub using the branch and remote configured for your checkout:

```bash
git push
```

Before committing, make sure you have not accidentally staged virtual-environment files, caches, generated outputs, or unrelated changes.

---

## Troubleshooting

### ModuleNotFoundError: No module named 'planning_lab'

- Confirm that the virtual environment is active.
- From the repository root, run:

```bash
python -m pip install -e .
```

- Check that you are using the same Python interpreter for installation and execution.

### pytest is not found

Run:

```bash
python -m pip install pytest
python -m pytest
```

Using `python -m pytest` helps ensure pytest runs with the active Python interpreter.

### A planning study cannot find an input file

- Run the study from the repository root.
- Confirm that the expected files exist under `02_model_inputs/`.
- Check file names and required columns.
- Read the error message before changing paths or input data.

### Tests fail after a change

- Read the first failing test and its assertion or traceback.
- Determine whether the failure is caused by the code, input data, or an outdated test expectation.
- Avoid changing a test simply to make it pass unless the expected behaviour itself has been shown to be incorrect.

---

## Project scope and limitations

This is a learning and software-engineering project. Its planning workflows, calculations, OSeMOSYS models, adequacy assessments, and risk analyses are limited to what is implemented and tested in the current codebase.

The fictional planning system used throughout the repository exists to provide a consistent environment for learning and experimentation. A documented future feature should not be assumed to be implemented.

Do not use the repository as a substitute for utility-grade planning software, approved planning methodologies, regulatory studies, or review by a suitably qualified engineer.

---

## Contributing

Contributions that improve correctness, readability, tests, documentation, reproducibility, or learning value are welcome.

Before proposing a change:

- Keep calculations transparent and explainable.
- State units and assumptions explicitly.
- Add tests for new behaviour.
- Keep example values distinguishable from study inputs where appropriate.
- Update the relevant engineering documentation when needed.
- Avoid committing secrets, local environment files, virtual environments, generated outputs, or caches.
- Prioritise reproducibility and traceability over complexity.

---

## License

No license is specified here. Check the repository for a `LICENSE` file before reusing, modifying, or redistributing the code.