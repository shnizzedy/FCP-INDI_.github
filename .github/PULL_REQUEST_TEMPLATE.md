body:
  - type: textarea
    id: fixes
    attributes:
      label: Fixes / related to
      description: |
        If PR doesn't fully resolve the issue, replace 'Fixes' below with 'Related to'.
        If there is no issue being resolved, consider opening one before creating this pull request.
      placeholder: "Fixes #[issue number] by @[issue author]"
  - type: textarea
    id: description
    attributes:
      label: Description
      description: Concisely describe what the pull request does.
    validations:
      required: true
  - type: textarea
    id: technical
    attributes:
      label: Technical details
      description: Add any other information or technical details about the implementation.
  - type: textarea
    id: tests
    attributes:
      label: Tests
      description: Give steps for the reviewer to verify that this PR fixes the problem.
  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots
      description: Add screenshots to show the problem and the solution.
  - type: input
    id: target
    attributes:
      label: Target branch
      description: Which branch should this pull request merge into?
    validations:
      required: true
  - type: checkboxes
    id: checklist
    attributes:
      options:
        - label: My pull request has a descriptive title (not a vague title like `Update index.md`).
        - label: My pull request targets the target branch of the repository specified above.
          required: true
        - label: My commit messages follow best practices.
        - label: My code follows the established code style of the repository.
        - label: I added tests for the changes I made (if applicable).
        - label: I updated the changelog.
        - label: I added or updated documentation (if applicable).
        - label: I tried running the project locally and verified that there are no visible errors.
        - label: I agree to the developer certificate of origin attestation. 
          required: true
  - type: markdown
    value: |
        "## Developer Certificate of Origin

        <details>
        <summary>Developer Certificate of Origin</summary>

        ```
        Developer Certificate of Origin
        Version 1.1

        Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
        1 Letterman Drive
        Suite D4700
        San Francisco, CA, 94129

        Everyone is permitted to copy and distribute verbatim copies of this
        license document, but changing it is not allowed.


        Developer's Certificate of Origin 1.1

        By making a contribution to this project, I certify that:

        (a) The contribution was created in whole or in part by me and I
            have the right to submit it under the open source license
            indicated in the file; or

        (b) The contribution is based upon previous work that, to the best
            of my knowledge, is covered under an appropriate open source
            license and I have the right under that license to submit that
            work with modifications, whether created in whole or in part
            by me, under the same open source license (unless I am
            permitted to submit under a different license), as indicated
            in the file; or

        (c) The contribution was provided directly to me by some other
            person who certified (a), (b) or (c) and I have not modified
            it.

        (d) I understand and agree that this project and the contribution
            are public and that a record of the contribution (including all
            personal information I submit with it, including my sign-off) is
            maintained indefinitely and may be redistributed consistent with
            this project or the open source license(s) involved.
        ```

        </details>"