<!-- NOTE: This file's contents are automatically generated. Do not edit manually. -->
# Create rendered template PR (Action)

This action creates a PR in the rendered template repository.
It creates a PR for the updates applied by the `update-rendered-template` action.

## 🔧 Inputs

|Name                 |Description                                                                                                                                |Required|Default         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|--------|----------------|
|`github-token`       |GitHub token for authentication. It must have permissions to read and write to the rendered repository. A GitHub App token is recommended. |Yes     |                |
|`rendered-repo-path` |Path where the rendered repository is cloned to.                                                                                           |No      |`rendered-repo` |

## 📤 Outputs

_None_

## 🚀 Usage

```yaml
- name: Create rendered template PR
  uses: eidp/actions-template/create-rendered-template-pr@v0
  with:
    # your inputs here
```
