# XSIAM Public

A collection of example automations, integrations, playbooks, and utilities for the [Palo Alto Networks XSIAM](https://www.paloaltonetworks.com/cortex/cortex-xsiam) platform.

## Contents

### Automations

| Name | Description |
|------|-------------|
| `jp-get-case-url` | Generates a direct URL to the parent case |
| `jp-get-playbook-by-name` | Returns a playbook name and ID based on a provided name using the Core REST API |
| `jp-get-script-details` | Retrieves details of an automation script by name using the Core REST API |
| `jp-gpds-get-related-host-issues` | Dynamic section that queries issues to find others with the same impacted host (agent ID) |
| `jp-gpds-get-related-user-issues` | Dynamic section that queries issues to find others with the same impacted user |
| `jp-normalize-timestamp-for-xql-query` | Builds a normalized XQL config timeframe string from an initial timestamp and a time window |
| `ps-list-to-html` | Converts a given array to a styled HTML table |
| `ps-list-to-markdown` | Converts a given array to a Markdown table compatible with XSIAM |
| `ps-print-markdown-url` | Logs a clickable URL in the war room |

### Integrations

| Name | Description |
|------|-------------|
| `XQL HTTP Collector` | Posts data to the XSIAM HTTP collector so it can be queried via XQL |

### Playbooks

| Name | Description |
|------|-------------|
| `JP - XSIAM Export Content Bundle` | Exports an XSIAM content bundle via the Core REST API and notifies the team on failure |

## Importing into XSIAM

Automation, integration, and playbook YAML files can be imported directly into your XSIAM tenant:

1. Navigate to **Settings > Content > Automation** (or **Integrations** / **Playbooks**)
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
```

### Dev Tools

| Tool | Purpose |
|------|---------|
| [ruff](https://docs.astral.sh/ruff/) | Python linting and formatting |
| [pytest](https://docs.pytest.org/) | Testing framework |
| [yamllint](https://yamllint.readthedocs.io/) | YAML validation |

## Repository Structure

```
xsiam-public/
├── automations/          # XSIAM automation scripts (Python in YAML)
├── Integrations/         # XSIAM integration configurations
├── Playbooks/            # XSIAM playbook definitions
├── .gitignore            # Git ignore rules
├── pyproject.toml        # Project config and tool settings
├── requirements-dev.txt  # Development dependencies
└── README.md
```

## Contributing

1. Create a feature branch from `main`
2. Add your automation, integration, or playbook YAML file to the appropriate directory
3. Open a pull request
