# Design and assurance notes

## Security objectives

| Objective | Scenario | Design response |
|---|---|---|
| Confidentiality | Examination question leakage (R01) | Phishing-resistant MFA, restricted question bank, independently authorised export, monitoring |
| Availability | Ransomware disruption (R02) | Isolated immutable backups, segmentation, verified restoration and continuity procedures |
| Integrity | Unauthorised grade change (R03) | Server-side role checks, separation of marking/moderation/publication, protected audit history |

## Interpretation of existing results

The original risk model contains 10 critical, 14 high and 1 medium baseline risks. Target residual ratings are 0 critical, 1 high, 22 medium and 2 low, conditional on successful treatment and verification. These are not measured incident frequencies or evidence of actual risk reduction. R06 remains high in the target model. The six-month roadmap and budget are planning assumptions.

The manual demonstration ended with a synthetic published grade of 79%, one accepted submission and an existing receipt ES-R001 on retry. The Security analyst generated synthetic alert ES-INC-01. The final dashboard recorded 38 events and 17 denials, not real attacks. The prototype intentionally allows screen inspection by every persona and uses mutable browser memory. Real access to sensitive content and logs must be enforced server-side. In the manual exercise the exact premature-publication rejection message was not captured, although the original automated check covered that condition. The tests do not prove real MFA, encryption, tenant isolation, resilience or GDPR compliance.

## Proposed implementation priorities

1. Agree ISMS scope, ownership, risk appetite and management commitment.
2. Validate business process and asset assumptions and classify risk by technology, people and processes and by CIA.
3. Treat priority risks using selected controls and document inclusion/exclusion decisions in the SoA; verify against the licensed standard.
4. Establish operational controls, incident response, continuity, protected audit logging and supplier assurance.
5. Verify controls with technical tests, recovery drills and internal audit before reassessing residual risk; record management acceptance and continual improvement.

## Standards approach

ISO/IEC 27001:2022 is the management-system basis; ISO/IEC 27002 and 27005 support controls and risk management. NIST SP 800-30 supports risk assessment, SP 800-53 supplies detailed control references, and CSF 2.0 provides six outcome functions. Cyber Essentials supplies baseline technical controls, and CIS Controls offer implementation guidance. UK GDPR obligations depend on controller/processor roles. PCI DSS is outside the assumed examination scope unless a cardholder-data environment is involved. No certification or legal compliance is claimed.

The lecture-alignment improvements and final assessment review are outstanding; this repository preserves the original technical evidence rather than representing proposed improvements as completed.
