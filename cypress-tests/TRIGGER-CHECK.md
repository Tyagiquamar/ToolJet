# Temporary — CI trigger check

Throwaway file. Exists only to give a dummy PR a diff so the
`Cypress Workflows` action can be exercised before its workflow file is merged
into `lts-3.16`.

Why this is needed: `cypress-workflows.yml` uses `pull_request_target`, which
reads the workflow definition from the PR's **base** branch. Until the file is on
`lts-3.16`, labelling a PR that targets `lts-3.16` does nothing. Basing a PR on
`test/workflow-cypress-cases` instead — where the file exists — makes the label
work.

Delete this file and close its PR once the run has been observed.
