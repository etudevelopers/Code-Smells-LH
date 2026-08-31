---
title: Home
layout: home
nav_order: 1
---

# {{ site.title }}
{: .no_toc }

{{ site.description }}.
{: .fs-6 .fw-300 }


This [Learning Hour] is about **code smells**: surface-level patterns in code that are quick to spot, don't
always indicate a real problem, but are worth a closer look — and the refactorings that resolve them once they do.

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Learning Goals 🎯

- Understand Martin Fowler's definition of a code smell, and why smells are a communication tool, not a verdict
- Know the three things that matter most about code smells: they're quick to spot, they most often (not always)
  indicate a real problem, and they have names
- Practice recognizing a specific code smell, explaining how to detect and fix it, and producing an illustrative
  example — then teaching it to someone else

## Connect activity to get everyone thinking about the topic (⏱️ 5 min)

**Warm-up.** Before we look at any formal list: do you know any code smells? What are they called? Write down
every name you can think of.

See [Connect Activities] in the [Samman Coaching] website for more ideas on how to connect with your team and
introduce the topic of this Learning Hour.

## An explanation of a new Concept or a coding demo (⏱️ 5 min)

**What's a code smell?** [Martin Fowler's definition][CodeSmell]: a surface indication that usually corresponds
to a deeper problem in the system.

**What's important about code smells:**

- They're quick to spot
- They most often — but not always — indicate a real problem
- They have names, which is what makes them useful to talk about as a team

There isn't one canonical list: Fowler's own catalogue in *Refactoring* names 24, and Samman Coaching's own
reference lists 26. See [Concept Explanation] for the full checklist and worked examples, and the
[Concept Activities] in the [Samman Coaching] website for more ideas on how to introduce a new Concept or do a
coding demo.

## Concrete Practice in a coding exercise (⏱️ 45 min)

Split into up to ten groups. Each group is assigned one code smell:

Comments · Repeated Switches · Data Clumps · Mysterious Name · Insider Trading · Long Parameter List ·
Message Chains · Deep Nesting · Feature Envy · Primitive Obsession

For your assigned smell:

1. How can you detect this smell in your code?
2. How would you address or solve it?
3. Bonus: get a Gen AI tool to produce some code with this smell as an illustrative example
4. Present your smell to another group

See [Concrete Practice Activities] in the [Samman Coaching] website for more ideas on how to design a coding
exercise to practice the new Concept.

## Conclusions discussion and reflection (⏱️ 5 min)

- If you had to explain the main idea of code smells to a colleague, what would you say?
- Was recognizing and fixing your assigned smell easier or harder than you expected?
- What's one smell you'll now watch for that you weren't looking for before?
- When should you stop at "it smells" and when should you actually refactor?

See [Conclusions Activities] in the [Samman Coaching] website for more ideas on how to facilitate a discussion to
reflect on the learning experience and draw conclusions.

## References

- [Learning Hour] — the Samman format this session follows
- [Concept Explanation] — the full checklist and worked examples
- [Martin Fowler's Code Smell definition][CodeSmell]
- [Samman Coaching's Code Smells reference list](https://sammancoaching.org/reference/code_smells/index.html)
- [Samman Coaching] — [Connect Activities] · [Concept Activities] · [Concrete Practice Activities] · [Conclusions Activities]


[Learning Hour]: https://sammancoaching.org/reference/learning_hour_definition.html
[Concept Explanation]: explanation/concept-explanation.html
[Connect Activities]: https://sammancoaching.org/activities/connect.html
[Concept Activities]: https://sammancoaching.org/activities/concept.html
[Concrete Practice Activities]: https://sammancoaching.org/activities/concrete.html
[Conclusions Activities]: https://sammancoaching.org/activities/conclusions.html
[Samman Coaching]: https://sammancoaching.org/
[CodeSmell]: https://martinfowler.com/bliki/CodeSmell.html
