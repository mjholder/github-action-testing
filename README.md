# github-action-testing
testing ground for github actions

## How to use stable-merge.yml:
The purpose of stable-merge.yml is to keep a carbon copy of a main branch on a separate branch. The example we have created assumes your head is "main" and the copy is "main-stable".

Make sure you have created the "main" and "main-stable" branches in your repo, or their equivalent.

You need to enable Github Actions to have read AND write access to your repo. To do this:
- Go to Settings->Actions->General
- Scroll down to Workflow permissions and set it to "Read and write permissions"

To add this workflow, copy the file and it's relative path to the root of your repo.
`./.github/workflows/stable-merge.yml`

Once that is in the repo, Github should pick it up and run it on your PRs to main.

Note: It's probably a good idea to protect your main-stable branch to avoid accidental pushes directly to it from other users. This would only allow the Github actions bot and admins to push to the branch.