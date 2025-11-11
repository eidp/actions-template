## auto-merge-rendered-template-pr (Workflow)

This reusable workflow automatically merges or closes a pull request in the rendered template repository based on whether the related template PR was merged or closed.

<!-- BEGIN WORKFLOW INPUT DOCS: auto-manage-rendered-template-pr -->

### 🔧 Inputs

|Name                      |Description                                                         |Required|Type   |Default         |
|--------------------------|--------------------------------------------------------------------|--------|-------|----------------|
|`runs-on`                 |The type of runner to run the job on                                |No      |string |`ubuntu-latest` |
|`template-manager-app-id` |GitHub App ID for the Template Manager App                          |Yes     |string |                |
|`rendered-template-repo`  |The rendered template repository to update (e.g. `python-fastapi`). |Yes     |string |                |

### 🔐 Secrets

|Name                            |Description                                      |Required|
|--------------------------------|-------------------------------------------------|--------|
|`template-manager-app-pem-file` |GitHub App PEM file for the Template Manager App |Yes     |

### 📤 Outputs

_None_

<!-- END WORKFLOW INPUT DOCS -->


### 🚀 Usage

```yaml
on:
  pull_request:
    types: [closed]
    branches:
      - main

jobs:
  manage-rendered-template-pr:
    uses: eidp/actions-template/.github/workflows/auto-manage-rendered-template-pr.yml@v0
    with:
      template-manager-app-id: ${{ secrets.TEMPLATE_MANAGER_APP_ID }}
      rendered-template-repo: 'your-rendered-repo'
    secrets:
      template-manager-app-pem-file: ${{ secrets.TEMPLATE_MANAGER_GITHUB_APP_PEM_FILE }}