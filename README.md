# check-readme-file
**Environment Strategy**

| Environment | Branch | Purpose                                    |
| ----------- | ------ | ------------------------------------------ |
| Development | `dev`  | Feature validation and integration testing |
| Production  | `main` | Live Prod environment                      |



**CI/CD Governance (Google Cloud Build)**
**Overview**
All builds and deployments are managed using Google Cloud Build.
Deployments require manual approval for both development and production, ensuring controlled and auditable releases.

**Branch-Based Deployment Model**

| Branch | CI Trigger      | Deployment Control |
| ------ | --------------- | ------------------ |
| `dev`  | Push / PR merge | Manual approval    |
| `main` | Push / PR merge | Manual approval    |

**Deployment Lifecycle**

**1.** Code is merged into dev or main.
**2.** A Cloud Build pipeline is automatically triggered.
**3.** Build and validation steps are executed.
**4.** Deployment pauses at an approval gate.
**5.** Deployment proceeds only after explicit approval.
**6.** Logs and execution metadata are retained.

**Manual Deployment Approval Steps**

**1** Open Google Cloud Console
**2** Navigate to Cloud Build → Build History
**3** Locate the build awaiting approval
**4** Click Approve (Optinonal message)
**5** Monitor deployment progress via build logs and stage
