# Claude Requirements Reviewer

Requirements Reviewer Framework v1.0

An open-source Claude Code skill for reviewing Product Requirements Documents (PRDs), user stories, epics, and requirements specifications for quality issues that commonly lead to scope creep, delivery delays, rework, and misaligned expectations.

The skill evaluates requirements using a structured review framework and generates actionable feedback on ambiguity, completeness, acceptance criteria quality, consistency, and scope definition.

---

## Why This Exists

One of the most common causes of engineering delivery issues is not poor implementation—it is unclear requirements.

Ambiguous language, missing acceptance criteria, hidden assumptions, and undefined dependencies often lead to:

* Scope creep
* Rework
* Delivery delays
* Misaligned stakeholder expectations
* Increased project risk

This skill provides an AI-assisted first-pass review of requirements before implementation begins.

---

## What It Reviews

The framework evaluates requirements across five dimensions:

| Dimension                     | Weight |
| ----------------------------- | ------ |
| Clarity & Precision           | 25     |
| Completeness                  | 25     |
| Acceptance Criteria Quality   | 20     |
| Consistency                   | 15     |
| Scope & Dependency Definition | 15     |

Total Score: 100

---

## Review Areas

### Clarity & Precision

Detects:

* Ambiguous language
* Vague terminology
* Undefined performance expectations
* Placeholder requirements

Examples:

* should
* might
* TBD
* fast
* scalable
* user-friendly

---

### Completeness

Identifies:

* Missing workflows
* Missing business rules
* Missing assumptions
* Missing edge cases

---

### Acceptance Criteria Quality

Checks whether requirements are:

* Testable
* Measurable
* Verifiable

---

### Consistency

Identifies:

* Contradictions
* Conflicting requirements
* Terminology inconsistencies

---

### Scope & Dependency Definition

Reviews:

* Scope boundaries
* External dependencies
* Third-party integrations
* Approval requirements

---

## Example Output

```text
Requirements Quality Score: 78/100

Top Findings

1. Missing acceptance criteria for report generation.
2. Authentication ownership is undefined.
3. Performance requirements use ambiguous language ("fast").

Recommendations

1. Add measurable acceptance criteria.
2. Define ownership for authentication integration.
3. Replace ambiguous performance expectations with SLAs.
```

---

## Installation

Clone the repository.

Copy the skill folder into your Claude Code skills directory:

```bash
~/.claude/skills/
```

Restart Claude Code.

The skill will automatically become available when reviewing requirements documents.

---

## Usage

Example:

```text
Review this PRD using the Requirements Reviewer skill.
```

or

```text
Analyze this user story for ambiguity, completeness, and delivery risks.
```

---

## Example Documents

See the `examples/` directory for:

* Good PRD example
* Poor PRD example
* Sample review outputs

---

## Scoring Interpretation

| Score    | Interpretation     |
| -------- | ------------------ |
| 90–100   | Excellent          |
| 80–89    | Good               |
| 70–79    | Needs refinement   |
| 60–69    | Significant gaps   |
| Below 60 | High delivery risk |

---

## Roadmap

### Version 1.1

* Improved contradiction detection
* Better acceptance criteria recommendations

### Version 1.2

* User Story Review Mode
* INVEST framework scoring

### Version 2.0

* Architecture Review Framework
* Extensible review modules

---

## Disclaimer

This tool is intended to assist human reviewers, not replace them.

Engineering judgment, product context, and stakeholder alignment remain essential.

AI-generated findings should be reviewed before making implementation decisions.

---

## License

MIT
