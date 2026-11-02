# Turn repeated failures into reusable parts and observable checks

Use this pattern when real tasks reveal the same class of defect more than once.
It implements the existing principles of testable success and small, evidence-led
changes. It is not a new global requirement to automate every task.

## Diagnose before adding instructions

Compare the failed behavior with the current instructions and actual workflow.
Distinguish missing guidance, duplicated implementations, missing validation and
tool limitations. If the rule already exists, adding it again rarely addresses
an implementation or verification gap.

Write one concrete expected/observed example. Keep domain-specific examples,
algorithms and implementation code in the child project.

## Apply the smallest useful intervention

1. Identify a small number of affected real outputs as a pilot.
2. Reuse or extract only the stable part that failed repeatedly. Leave domain
   calculations and judgment in their existing owner.
3. Express a few observable acceptance criteria independently of the new helper.
4. Run checks on the actual output in a suitable execution environment. Source
   review, simulated execution, real execution and deployed verification are
   different kinds of evidence.
5. Select affected outputs when possible; a shared dependency change should
   check representative consumers. Explicitly report outputs outside coverage.
6. Save version, environment, expected/observed behavior and failure evidence.
7. Observe the pilot before expanding to other projects or promoting a global rule.

Automate measurable failures when the repeated cost justifies it. Retain human
review for clarity, usability or other judgments that the check does not establish.
Use a separate verification job when adding checks to a slow delivery path would
unnecessarily delay every output.

## Keep unverified work actionable

For every unverified item, record:

- the behavior still to check and a concrete next operation;
- the output/version and expected result;
- the accountable owner, such as the current PR author/reviewer;
- where the follow-up and eventual result will be recorded.

A tool failure is not a passed check. Successful checks do not erase the remaining
human or deployment checks. Do not turn an honest limitation into a blanket ban
on useful features, or require an approval step the user has not requested.

## Ownership

The factory owns this method. Child projects own reusable components, executable
checks, domain acceptance criteria, pilot registration and operational records.
Link to the child implementation instead of copying its rules into the factory.
Do not automatically migrate every registered agent or introduce an additional
agent merely to run a deterministic check.

## Pilot evidence

The first UI pilot is tracked in the [2026-11-02 research entry](../../research/changelog.md).
Its implementation lives in the study-site repository. The pilot's proposed scope
is evidence for trying the method, not proof that all child agents benefit from it.
