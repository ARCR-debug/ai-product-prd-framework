# AI Safety Checklist for Product Launch

## Purpose

This checklist is designed to help a product team determine whether an AI feature is ready for controlled release. The goal is not to prove that the model is perfect. The goal is to show that major risks have been identified, tested, mitigated, and assigned to an owner before launch.

## 1. Input Safety

- Have the expected user input types been documented
- Have adversarial prompts been tested
- Have prompt injection patterns been reviewed
- Have abusive, harmful, and policy violating inputs been tested
- Have malformed and edge case inputs been tested
- Is there a safe behavior for unsupported or ambiguous requests

## 2. Output Safety

- Can the system generate fabricated products or nonexistent entities
- Can the system expose unsafe, offensive, or irrelevant outputs
- Does the system overstate confidence when uncertain
- Are there output filters for harmful content
- Are there suppression rules for clearly unsafe output classes
- Has the team defined what constitutes a P0 versus P1 output failure

## 3. Privacy and Data Protection

- Does the feature process personal data
- Are prompts or responses logged
- Is sensitive data masked before storage where necessary
- Has the team defined retention rules
- Can the system accidentally echo user supplied sensitive information
- Has privacy review been completed for the intended launch scope

## 4. Grounding and Verification

- For factual or catalog backed experiences, is output grounded in an approved source
- Can the response be checked against a trusted database or retrieval layer
- Is there a product existence check for returned items
- Is there a confidence threshold below which the system falls back
- Has the team tested cases where the source data is incomplete or stale

## 5. Latency and Reliability

- Has the feature been tested under realistic traffic assumptions
- Are median and tail latency within acceptable bounds
- Is there a timeout behavior that protects the user experience
- Is there a circuit breaker or fallback mode
- Have error states been designed for clarity rather than silent failure

## 6. Human Review and Escalation

- Is there an owner for launch safety review
- Is there an incident review process for harmful outputs
- Is there a path for internal escalation if user harm is possible
- Is there a clear severity framework for classifying incidents
- Is user feedback captured in a reviewable way after launch

## 7. Rollback Readiness

- Is there a defined rollback threshold for quality failure
- Is there a defined rollback threshold for safety failure
- Is the rollback path technically simple and fast
- Has rollback been tested before launch
- Does the team know who can approve rollback in real time

## 8. User Trust and Disclosure

- Is it clear to users when AI is helping generate results
- Are limitations explained where needed
- Does the feature avoid implying certainty where uncertainty exists
- Are fallback experiences designed to preserve user trust
- Has the team defined how to communicate known limitations internally and externally

## Failure Mode Reference Table

| Failure Mode | Detection Method | Immediate Fallback | Severity |
|---|---|---|---|
| Hallucinated product | Validate returned product IDs against the catalog | Suppress invalid results and fall back to keyword search | P0 |
| Offensive result | Content safety classifier and policy filters | Replace with safe fallback and log for review | P0 |
| Excessive latency | Request timeout and latency alerting | Serve cached or baseline results | P1 |
| PII leakage | PII scanning on output and logs | Strip sensitive content and trigger security review | P0 |
| Prompt injection | Input sanitization and prompt risk classification | Reject or isolate the request and return safe default behavior | P1 |

## Launch Recommendation Logic

A launch should proceed only if:
- no unresolved P0 risks remain
- fallback behavior has been tested
- privacy handling has been reviewed
- monitoring is live
- rollback authority is assigned
- the team has reviewed representative bad case behavior, not just best case demos

## Closing Principle

The safest AI launch is not the one with the most optimistic demo. It is the one where the team already knows how the feature fails, how the user is protected, and how the system will recover if quality drops in production.
