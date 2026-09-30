---
url: /parity-report/docs/contributing.md
description: >-
  Set up a local BabelFHIR-TS development environment, understand the project
  structure and generator pipeline, run tests, and submit pull requests.
---

# Contributing

Thank you for your interest in contributing to BabelFHIR-TS!

## Development Setup

### Prerequisites

* Node.js 18 or higher
* npm 9 or higher
* Git

### Installation

```bash
git clone https://github.com/babelfhir-ts/BabelFHIR-TS.git
cd BabelFHIR-TS
npm install
```

The `prepare` script automatically configures git hooks (including the [pre-commit hook](#pre-commit-hook) that syncs CLI help text).

### Build & Test

```bash
npm run build       # Compile TypeScript
npm test            # Type-check + run all Vitest suites
npm run generate    # Run CLI against local input/ folder
```

## Useful Scripts

| Script | Purpose |
|---|---|
| `npm run generate` | Execute the CLI against the local `input/` folder and refresh `output/`. |
| `npm run generate:check` | End-to-end check: generate, type-check, and lint the emitted output. |
| `npm test` | Type-check and run all Vitest suites (coverage enabled). |
| `npm run test:parity` | Run pipeline parity tests against the Firely SDK Validator. |
| `npm run docs:dev` | Start VitePress dev server for documentation. |
| `npm run docs:build` | Build static documentation site. |

## Project Structure

```
src/
  ├── generator/
  │   ├── index.ts                    # Orchestrates full generation pipeline
  │   ├── sdProcessor.ts              # SD processing coordinator
  │   ├── generationHelpers.ts        # Shared generation utilities
  │   ├── parser/                     # StructureDefinition parsing
  │   │   ├── sdParser.ts             # Parses SD JSON → Field[]
  │   │   ├── sdFetcher.ts            # Resolves/downloads SDs by URL
  │   │   ├── vsParser.ts             # ValueSet parsing
  │   │   ├── sliceAggregator.ts      # Slice definition aggregation
  │   │   ├── packageParser.ts        # FHIR package extraction
  │   │   └── txClient.ts             # Terminology server client
  │   ├── core/                       # Shared types and constants
  │   │   ├── sdTypes.ts              # Field, SliceGroup, etc.
  │   │   └── fhirTypes.ts            # FHIR type constants
  │   ├── fhir/                       # FHIR version abstraction
  │   │   ├── versionContext.ts       # R4/R4B version context
  │   │   └── versionRegistry.ts      # Version-specific registries
  │   └── emitters/                   # Code generation output
  │       ├── interface/              # TypeScript interface generation
  │       │   └── interfaceGenerator.ts
  │       ├── validator/              # Runtime validator generation
  │       │   ├── validatorGenerator.ts
  │       │   ├── validatorConstraintBuilders.ts
  │       │   ├── validatorBindingBuilder.ts
  │       │   └── sliceValidatorGenerator.ts
  │       ├── class/                  # Class + random() generation
  │       │   ├── classGenerator.ts
  │       │   ├── randomSupportGenerator.ts
  │       │   └── enrichResourceHandlers.ts
  │       ├── valueset/               # ValueSet code generation
  │       │   └── valueSetGenerator.ts
  │       ├── zod/                    # Zod schema generation
  │       │   └── zodSchemaGenerator.ts
  │       └── client/                 # FHIR client generation
  │           └── clientGenerator.ts
  ├── main.ts                         # CLI entry point
  └── logger.ts                       # Logging utilities
scripts/                              # Build and utility scripts
docs/                                 # VitePress documentation (this site)
test/                                 # Test files
out/                                  # Compiled JavaScript (gitignored)
```

## Pre-Commit Hook

The repo includes a pre-commit hook (`.githooks/pre-commit`) that automatically captures `babelfhir-ts -h` output and updates:

* `README.md`
* `.github/instructions/copilot.instructions.md`
* `docs/cli-reference.md`

This ensures CLI documentation stays in sync whenever `printUsage()` in `src/main.ts` changes. The hook is activated automatically via the `prepare` script in `package.json`.

## Submitting Changes

1. Fork the repository and create a feature branch from `develop`
2. Make your changes with clear commit messages
3. Ensure `npm test` passes
4. Open a pull request against `develop`

For bug reports and feature requests, please [open an issue](https://github.com/babelfhir-ts/BabelFHIR-TS/issues).
