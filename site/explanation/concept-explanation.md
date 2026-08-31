---
title: Concept Explanation
layout: default
parent: Explanation
nav_order: 1
---

# Concept Explanation
{: .no_toc }

Martin Fowler's definition of a code smell, what's important about them, and three worked examples.
{: .fs-6 .fw-300 }

A **code smell** is a surface indication that usually corresponds to a deeper problem in the system — not a
verdict, a prompt to look closer. See [Martin Fowler's original definition][CodeSmell].

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What's important about code smells

- **Quick to spot** — that's the point; a smell is a cheap signal, not an exhaustive analysis
- **Most often — but not always — indicate a real problem** — treat a smell as a prompt to look closer, not an
  automatic defect
- **They have names** — a name is what makes a smell something a team can recognize and discuss together.
  Fowler's own catalogue in *Refactoring* lists 24; Samman Coaching's own reference lists 26

## Worked examples

### Comments

**How to spot it:** comments that explain the logic of a method, rather than the method's name and structure
explaining it themselves.

**How to fix it:**

- Extract method
- Rename method / field
- Introduce assertion
- Remove the comment

### Data Clumps

Spotting a repeated set of data (fields, parameters, classes) that always appear together — coordinates, a name
and address, and similar groupings. A long parameter list can be a warning sign of the same underlying clump.

**Fix:** extract the clump to a class, or a parameter object.

After fixing this, look for Long Parameter List and Feature Envy — they often surface next.

### Repeated Switches

**Detect:** the same set of options, switched on repeatedly, across multiple `switch` or `if`/`else` blocks.

**Fix:** replace the repeated conditional with polymorphic classes.

```java
enum EmployeeType {
    FULL_TIME,
    PART_TIME,
    CONTRACTOR
}

class PayrollService {
    double calculatePay(EmployeeType type, int hours) {
        switch (type) {
            case FULL_TIME:
                return hours * 50;
            case PART_TIME:
                return hours * 30;
            case CONTRACTOR:
                return hours * 70;
            default:
                throw new IllegalArgumentException();
        }
    }
}

class BenefitsService {
    int calculateVacationDays(EmployeeType type) {
        switch (type) {
            case FULL_TIME:
                return 20;
            case PART_TIME:
                return 10;
            case CONTRACTOR:
                return 0;
            default:
                throw new IllegalArgumentException();
        }
    }
}
```

Both methods switch on the same `EmployeeType` — that repetition is the smell. Introducing a polymorphic
`EmployeeType` hierarchy (or a `Payroll`/`Benefits` strategy per type) removes the duplication and the risk of the
two switches drifting out of sync.

### Still to work through in a future iteration

Insider Trading, Mysterious Name, Long Parameter List, Message Chains, Deep Nesting, Feature Envy, and Primitive
Obsession are part of the Concrete Practice exercise but don't yet have a worked example here — the source Miro
board's group frames for these were left as unfilled templates. Add them here as they're worked out in a live
session.

## Further Reading

- [Martin Fowler's Code Smell definition][CodeSmell]
- [Samman Coaching's Code Smells reference list](https://sammancoaching.org/reference/code_smells/index.html)
- [Refactoring Guru's Code Smells catalog](https://refactoring.guru/refactoring/smells)
- [Coding Horror: Code Smells](https://blog.codinghorror.com/code-smells/)
- [Learning Hour: Connect Activities](https://sammancoaching.org/activities/connect.html)
- [Learning Hour: Concept Activities](https://sammancoaching.org/activities/concept.html)
- [Learning Hour: Concrete Practice Activities](https://sammancoaching.org/activities/concrete.html)

[CodeSmell]: https://martinfowler.com/bliki/CodeSmell.html
