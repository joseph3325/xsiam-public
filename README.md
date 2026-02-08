# XSIAM Public

A collection of example automations, integrations, and utilities for the [Palo Alto Networks XSIAM](https://www.paloaltonetworks.com/cortex/cortex-xsiam) platform.

## Contents

### Automations

| Name | Description |
|------|-------------|
| `jp-get-case-url` | Generates a direct URL to the parent case |
| `jp-get-playbook-by-name` | Returns a playbook name and ID based on a provided name using the Core REST API |
| `jp-gpds-get-related-host-issues` | Dynamic section that queries issues to find others with the same impacted host (agent ID) |
| `jp-gpds-get-related-user-issues` | Dynamic section that queries issues to find others with the same impacted user |
| `ps-list-to-html` | Converts a given array to a styled HTML table |
| `ps-list-to-markdown` | Converts a given array to a Markdown table compatible with XSIAM |

### Integrations

| Name | Description |
|------|-------------|
| `XQL HTTP Collector` | Posts data to the XSIAM HTTP collector so it can be queried via XQL |

## Importing into XSIAM

Automation and integration YAML files can be imported directly into your XSIAM tenant:

1. Navigate to **Settings > Content > Automation** (or **Integrations**)
2. Click **Upload** and select the `.yml` file
3. Configure any required parameters (API keys, instance names, etc.)

## Development Setup

### Prerequisites

- Python 3.10+
- Git

### Getting Started

```bash
# Clone the repository
git clone https://github.com/joseph3325/xsiam-public.git
cd xsiam-public

# Create and activate a virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install dev dependencies
pip install -r requirements-dev.txt

# Install pre-commit hooks
pre-commit install
```

### Dev Tools

| Tool | Purpose |
|------|---------|
| [ruff](https://docs.astral.sh/ruff/) | Python linting and formatting |
| [pytest](https://docs.pytest.org/) | Testing framework |
| [yamllint](https://yamllint.readthedocs.io/) | YAML validation |
| [pre-commit](https://pre-commit.com/) | Git hook management |

### Pre-commit Hooks

The following checks run automatically on each commit:

- Trailing whitespace removal
- End-of-file newline enforcement
- YAML syntax validation
- Large file detection
- Merge conflict markers
- Ruff lint and format checks

## Repository Structure

```
xsiam-public/
├── automations/          # XSIAM automation scripts (Python in YAML)
├── Integrations/         # XSIAM integration configurations
├── .editorconfig         # Editor formatting rules
├── .gitignore            # Git ignore rules
├── .pre-commit-config.yaml
├── pyproject.toml        # Project config and tool settings
├── requirements-dev.txt  # Development dependencies
└── README.md
```

## Contributing

1. Create a feature branch from `main`
2. Add your automation or integration YAML file to the appropriate directory
3. Ensure pre-commit hooks pass
4. Open a pull request
