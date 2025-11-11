<!-- NOTE: This file's contents are automatically generated. Do not edit manually. -->
# Update rendered template (Action)

This action clones the rendered template repository and updates the rendered template based on changes in the current branch of the template repository.
It does not create a pull request; that is handled by a separate action. 
It only clones the rendered repository and applies updates.

It uses `cruft` to apply updates from the template repository to the rendered repository.
If there are merge conflicts, the action will attempt to resolve them by accepting incoming changes.
If manual intervention is required, the action will fail and provide details in the logs.

## 🔧 Inputs

|Name                 |Description                                                                                                                                |Required|Default         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|--------|----------------|
|`github-token`       |GitHub token for authentication. It must have permissions to read and write to the rendered repository. A GitHub App token is recommended. |Yes     |                |
|`rendered-repo-path` |Path to clone the rendered repository into.                                                                                                |No      |`rendered-repo` |

## 📤 Outputs

_None_

## 🚀 Usage

```yaml
- name: Update rendered template
  uses: eidp/actions-template/update-rendered-template@v0
  with:
    # your inputs here
```
