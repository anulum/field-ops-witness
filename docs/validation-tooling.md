<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
FIELD-OPS-WITNESS — repository governance and provenance
-->

# Validation tooling API

The metadata command accepts `--root` and `--json`. The inventory command additionally accepts `--mode generate|verify` and requires `--output` only for generation. All commands emit safe structured JSON. Exits are 0 for the requested scope, 2 for refusal, 3 for unavailable required inputs or tools, and 4 for invalid invocation or configuration.

Metadata validation accepts no generated inventory dependency. Inventory generation publishes deterministic new bytes; verification requires the canonical inventory and complete initial paths. A successful operation does not qualify field sources, drift judgments or recall coverage or establish release readiness.

## Metadata acceptance

::: field_validation.metadata.validate_metadata

## Finite input

::: field_validation.inputs.read_file

::: field_validation.inputs.read_json

## Capability inventory

::: field_validation.capabilities.inventory_bytes

::: field_validation.capabilities.create_inventory

::: field_validation.capabilities.validate_capabilities

## Diagnostics

::: field_validation.report.Finding

::: field_validation.report.Report

## Command interfaces

::: field_validation.cli.metadata_main

::: field_validation.cli.inventory_main

## Source ownership and maintained tree

::: field_validation.provenance.validate_notice

::: field_validation.provenance.validate_provenance

::: field_validation.structure.maintained_paths

::: field_validation.structure.validate_structure

## YAML and workflow policy

::: field_validation.yaml_input.read_yaml

::: field_validation.workflows.validate_workflows

## Complete dependency observations

Release candidates and observed installed metadata are separate records. The hash lock covers the entire selected development graph. Exact source-builder constraints also use that lock. Recorded installation RECORD hashes are observations; relocated entry-script paths prevent treating them as universal build identities. Custom licence references retain exact source terms and do not infer permissions.

::: field_validation.dependency_lock.parse_direct

::: field_validation.dependency_lock.parse_lock

::: field_validation.dependency_records.Artifact

::: field_validation.dependency_records.LicenseEvidence

::: field_validation.dependency_records.LicenseSource

::: field_validation.dependency_records.PackageRecord

::: field_validation.dependency_records.read_provenance

::: field_validation.dependencies.verify_records

::: field_validation.dependencies.verify_installed

::: field_validation.dependencies.verify_configuration

::: field_validation.dependencies.validate_dependencies

::: field_validation.native_tools.verify_native_tools

## Actual documentation rendering

::: field_validation.documentation.References

::: field_validation.documentation.render_markdown

::: field_validation.documentation.inspect_markdown

::: field_validation.documentation.build_site

::: field_validation.documentation.inspect_projection

::: field_validation.documentation.validate_documentation

## Tool completion and scoped preflight

Every tool uses a fixed absolute executable, literal arguments and a finite deadline. Actual exits survive communication errors where observed. Output limits apply to accepted completed output; the caller reserves process memory separately. A named preflight subset reports its narrower scope. The complete operation requires the entire compiled profile. Missing tools, invalid protocol and native failures retain their real states.

::: field_validation.execution.ToolResult

::: field_validation.execution.run_tool

::: field_validation.preflight.Check

::: field_validation.preflight.Outcome

::: field_validation.preflight.PreflightReport

::: field_validation.preflight.validate_checker_report

::: field_validation.preflight.run_check

::: field_validation.preflight.run_checks

::: field_validation.preflight.source_payload

::: field_validation.validation_profile.scaffold_checks

::: field_validation.preflight_cli.preflight_main

## Shared command and protocol interfaces

::: field_validation.inputs.parse_json

::: field_validation.report.Refusal

::: field_validation.cli.Parser

::: field_validation.cli.check_main

::: field_validation.cli.emit_report

::: field_validation.ci_dependencies.verify_ci_dependencies

## Native workflow composition

The coordinator executes the eight complete native jobs from the maintained workflow sources. Each of four category gates requires every actual descendant result, and the stable required gate checks all four category results. The workflow policy verifies exact job equality with each source and rejects missing descendants, masked outcomes, altered commands and workflow calls. This preserves all category checks without depending on an unsupported reusable-workflow syntax. Both native syntax and unchanged pedantic workflow checks inspect the actual executable configuration; no projected input or suppressed finding is used.
