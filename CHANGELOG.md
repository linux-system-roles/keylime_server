Changelog
=========

[1.0.1] - 2023-09-08
--------------------

### Other Changes

- ci: Add markdownlint, test_converting_readme, and build_docs workflows (#12)

  - markdownlint runs against README.md to avoid any issues with
    converting it to HTML
  - test_converting_readme converts README.md > HTML and uploads this test
    artifact to ensure that conversion works fine
  - build_docs converts README.md > HTML and pushes the result to the
    docs branch to publish dosc to GitHub pages site.
  - Fix markdown issues in README.md
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

- docs: Make badges consistent, run markdownlint on all .md files (#13)

  - Consistently generate badges for GH workflows in README RHELPLAN-146921
  - Run markdownlint on all .md files
  - Add custom-woke-action if not used already
  - Rename woke action to Woke for a pretty badge
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

- ci: Remove badges from README.md prior to converting to HTML (#14)

  - Remove thematic break after badges
  - Remove badges from README.md prior to converting to HTML
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>


[1.0.0] - 2023-07-24
--------------------

### New Features

- New role for managing keylime server

  This is an ansible role for configuring and deploying the server
  components for Keylime Remote Attestation.
  
  It currently supports Fedora 36+, CentOS Stream 9.1+ and RHEL 9.1+
