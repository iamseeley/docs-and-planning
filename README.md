# DDAI - Documents & Planning

<https://github.com/UTK-ASE-DDAI/docs-and-planning/tree/main/README.md>

A Meta-Repository for collecting documents and artifacts required for
submission on Canvas.

This is a not a "living document", but may be updated as a "summary analysis"
of work performed elsewhere.

## Initial Project Proposal

- [Project Idea](https://github.com/UTK-ASE-DDAI/docs-and-planning/blob/main/project-idea.md)

## Meeting Minutes

- [2024-06-17](https://github.com/UTK-ASE-DDAI/docs-and-planning/blob/main/minutes-2024-06-17.md)

## High-level Planning (Waterfall Plan)

### Project Management Strategy

Project management will be loosely based around SCRUM, in a structure that best
fits our team, and at the guidance of our instructor.

GitHub will be our primary project management apparatus, utilizing the issues
system, project boards, and iteration timelines. These systems closely resemble
traditional SCRUM mechanisms with mild deviations.

### Requirements

- Automatically generate detailed NPCs with:

  - names
  - backgrounds
  - traits
  - dialogue options

- End-user web-based application for broad-reaching user accessibility.

- A resource-based server for API interaction.

- Future Work
  - Customizable parameters to tailor NPCs to specific campaigns.

### Design & Implementation

- Web-based end-user application utilizing either `react` or `svelte`.

- Resource-based HTTP API server utilizing `FastAPI`, `MongoDB`, and `ElasticSearch`.

- A centralized data model defined as `Pydantic` models, describing
  data-communication structure.

- A retrieval-augmented generation platform. (This is still not well known to
  the team, further research is required before documentation will be available
  here.)

- Further design prospects will follow and iterative development practice, as
  well as LEAN principles.

  - Eliminate Waste
  - Amplify Learning
  - Decide as late as possible
  - Deliver as fast as possible
  - Empower the team
  - Build integrity in
  - Optimize the whole

- Iterative work will be document thoroughly via. GitHub _projects_, _issues_,
  and _commits_.

### Testing Strategy

The overall testing strategy involves the following:

- Follow Test-Driven Development where it _makes sense_, with reasonable exceptions.

- Take full advantage of _GitHub Actions_ to perform automated tests
  on-push-or-merge.

- Use static analysis apparatus available to the development team to minimize
  semantic bugs before they reach source control.

- Localized unit testing by utilizing common-sense inversion-of-control
  principles, allowing for dependency injection of mock-systems during logic
  testing of independent components.

- Full-depth integration testing between systems facilitated with the help of
  `docker` during local-testing phases, and `azure` during final production
  testing.

- The _Web-Application_ will be tested internally using `jest` and `supertest`.
  (This is subject to change based on team requirements.)

- The _Resource Server_ will be tested internally using `pytest` and
  `FastAPI.TestClient`.
  (This is subject to change based on team requirements.)

- Per-feature manual testing may be design and followed where necessary.

- Final production testing may occur at certain documented intervals as seen
  fit by the team, and at the guidance of our instructor.

- All testing strategy points are subject to change at the guidance of our
  instructor.

### Deployment

Deployment will require a complete technology stack that includes:

- The _Resource Server_ served from a WSGI gateway instance.

- The _Web-Application_ served from a static web-host.

- A _MongoDB_ instance running on a local-or-remote host.

- An _ElasticSearch_ instance running on a local-or-remote host.

Future work includes deployment support via. `docker`.

### Maintenance

- Subject to approval by our instructor, ongoing development and maintenance
  will occur in line with the above mentioned project management strategy.

- At this time, maintenance beyond the scope of this UTK course has not been
  discussed by the team. At present, the _maintenance strategy_ is inline with the
  _development strategy_.
