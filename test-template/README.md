<!-- NOTE: This file's contents are automatically generated. Do not edit manually. -->
# Test template (Action)

Action that tests template rendering using cookiecutter.
It verifies that all template variables are replaced in the rendered output.
The rendered template is uploaded as an artifact for further inspection.

## 🔧 Inputs

|Name            |Description                                |Required|Default|
|----------------|-------------------------------------------|--------|-------|
|`template-path` |Path to the cookiecutter template to test. |No      |`.`    |

## 📤 Outputs

_None_

## 🚀 Usage

```yaml
- name: Test template
  uses: eidp/actions-template/test-template@v0
  with:
    # your inputs here
```
