# check-readme-file
CI/CD Governance (Google Cloud Build)
Overview

All builds and deployments are orchestrated using Google Cloud Build with mandatory manual approvals.
This ensures:

Controlled releases

Full auditability

Reduced deployment risk

Clear accountability
| Branch | CI Trigger      | Deployment Control |
| ------ | --------------- | ------------------ |
| `dev`  | Push / PR merge | Manual approval    |
| `main` | Push / PR merge | Manual approval    |

Deployment Lifecycle
Code is merged into dev or main.

A Cloud Build pipeline is automatically triggered.

Build and validation steps are executed.

Deployment pauses at an approval gate.

Deployment proceeds only after explicit approval.

Logs and execution metadata are retained.

Manual Deployment Approval
To approve a deployment:

Open Google Cloud Console

Navigate to Cloud Build → Build History

Locate the build awaiting approval

Click Approve

Monitor deployment progress via build logs and stage
