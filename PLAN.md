# MVC Test implementation plan

Recover a reproducible local build for the Spring/Jetty MVC sample before deciding on further development.

Status: proposed next work, prepared from local source inspection on 2026-10-04. Existing behavior below has not been rerun or release-verified in this planning pass. Update this file as work lands; check an item only after recording its acceptance evidence.

## Current evidence

The Maven project includes MVC controllers, Thymeleaf configuration, account/security-code repositories, mail support, and Jetty startup. README.md only calls it an MVC test application.

## Pending implementation

- [ ] Document the Java/Maven baseline, startup entry point, database requirements, and which login/mail/captcha flows depend on external services.
- [ ] Build a local sample profile with disposable users and mocked mail; add a smoke test for page rendering and account activation boundaries.
- [ ] Decide whether to preserve the sample or modernize it; if modernization is chosen, inventory dependency/API incompatibilities before changing behavior.

## Acceptance

A documented local profile starts without contacting real users, one page and the activation fixture pass, and required external dependencies are explicit.

## Scope and decisions

This is a legacy sample, not a newly approved production service. Dependency modernization should follow the continuation decision.

## Sources

- [README.md](<README.md>)
- [pom.xml](<pom.xml>)
- [src/main/java](<src/main/java>)
- [src/main/resources](<src/main/resources>)
