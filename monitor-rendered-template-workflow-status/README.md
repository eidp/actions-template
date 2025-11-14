<!-- NOTE: This file's contents are automatically generated. Do not edit manually. -->
# Monitor rendered template workflow status (Action)

This action monitors the status of the workflow run in the branch that was created as part of the rendered template update process.
It waits for the workflow to complete and checks whether it succeeded or failed.

## 🔧 Inputs

|Name                           |Description                                                                                                                                       |Required|Default           |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------|------------------|
|`github-token`                 |GitHub token for authentication. It must have permissions to read actions in the rendered template repository. A GitHub App token is recommended. |Yes     |                  |
|`rendered-template-repo-owner` |The owner of the rendered template repository to monitor (e.g. `eidp`).                                                                           |Yes     |                  |
|`rendered-template-repo`       |The rendered template repository to monitor (e.g. `python-fastapi`).                                                                              |Yes     |                  |
|`rendered-template-workflow`   |The workflow file name in the rendered template repository to monitor (e.g. `preview-env.yml`).                                                   |No      |`preview-env.yml` |

## 📤 Outputs

_None_

## 🚀 Usage

```yaml
- name: Monitor rendered template workflow status
  uses: eidp/actions-template/monitor-rendered-template-workflow-status@v0
  with:
    # your inputs here
```
