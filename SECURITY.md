# Security

Tools and skills that help with focus and follow-through.

## Reporting a vulnerability

Report security issues privately to **aleximperiale@outlook.com**. Do not open a public
issue for anything you believe is exploitable.

Include the version or commit you tested, the org edition and configuration if relevant,
what you observed, and the smallest set of steps that reproduces it. A proof of concept is
welcome but not required.

What to expect:

| Stage | Target |
|---|---|
| Acknowledgement that the report was received | 3 working days |
| Initial assessment, including whether it is accepted | 10 working days |
| Fix or documented mitigation for an accepted issue | 30 days, sooner where severity warrants |

We will tell you which way the assessment went either way. If a report is not accepted you
will get the reasoning, not silence. Credit is offered on any accepted report unless you ask
us not to.

## Supported versions

Security fixes land on the default branch. There are no long-lived release branches and no
backports to older commits, so the supported version is the current `main`.

## What this repository is, and what that means for risk

This repository contains configuration, prompts and documentation. It is not a
deployable Salesforce package and contains no Apex, no LWC and no server-side code. The
risk it carries is the risk of content that a person or an automated agent may act on,
rather than the risk of running code.

## Threat model

- Instructions in this repository are read by humans and by coding agents. Treat anything here as advisory, not authoritative.
- Content in a repository can be modified by anyone with write access. Review changes before acting on them, particularly changes to instructions that an automated agent will follow.
- Nothing here executes on its own. Any effect comes from a person or tool choosing to run it.

## Secrets

No API keys, tokens, passwords, certificates or org credentials are committed here.
Examples that need a credential use an obvious placeholder. If you find a real one,
treat it as a live incident and report it to the address above rather than opening an
issue.

## What this repository deliberately does not do

- It does not contain executable application code.
- It does not access any Salesforce org, external service or user data.
- It does not collect telemetry.

## Using this content safely

- Read a file before you let a tool act on it.
- Pin to a commit if you depend on this content in an automated workflow, so an upstream edit cannot silently change behaviour.
- Do not paste credentials into any file here.

## License and warranty

Released under the MIT License. It is provided without warranty of any kind, including
any warranty of security or fitness for a particular purpose. See [LICENSE](LICENSE).

Copyright (c) 2026 Alex Imperiale
