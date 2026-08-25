# Soc Ops Agent Guide

## Mandatory Development Checklist

Before completing a change, run and confirm:

- [ ] Lint: use the repository's configured lint tool, if present; report when none is configured.
- [ ] Build: `cd socops && ./mvnw clean package`
- [ ] Test: `cd socops && ./mvnw test`

## Project Shape

- The runnable Java 21 / Spring Boot 3.4.2 app is in `socops/`; it uses Maven and Thymeleaf.
- `SocOpsApplication` starts the app. `BingoRestController` serves `/` and `GET /api/bingo/fresh-board`.
- `BoardAssembler` is the pure static home for bingo rules: it creates 25-cell boards, flips immutably, and detects row, column, and diagonal wins.
- Reuse the records and enum in `socops/src/main/java/com/socops/model/`. Cell id `12` is the selected free cell.
- `game.html` owns the Thymeleaf page and browser game behavior; `app.css` owns custom CSS utilities.

## Change Guidance

- Add or update focused tests in `socops/src/test/java/` for rule changes.
- Never mutate input boards or `BingoCell` records; controller code should remain HTTP/page wiring.
- For frontend work, follow [CSS utilities](.github/instructions/css-utilities.instructions.md) and [frontend design guidance](.github/instructions/frontend-design.instructions.md).
- Use Java 21+ and prefer `socops/mvnw`; the app runs on port 8080 by default.
- Keep `socops/target/` and unrelated generated files out of changes.

## Documentation

- Use the [README](README.md) for setup and the [workshop guide](workshop/GUIDE.md) for the learning flow.
- Existing reusable agents and prompts are in [.github/agents](.github/agents) and [.github/prompts](.github/prompts).
