# Validate FHIR Resource Status Action

This GitHub Action validates that FHIR JSON files in a given folder have a `status` field that, if present, is either `"active"` or `"retired"`. Files without a `status` field are ignored.

## Usage

In your workflow YAML, you can reference the action as follows:

```yaml
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Validate FHIR Files
        uses: patrick-werner/validate-fhir-resource-status@v1.0.0
        with:
          folder: './path/to/fhir-files'
