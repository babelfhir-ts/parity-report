# pixm - Detailed Report (FHIR all)
Generated: 2026-09-05T11:25:22.598Z

Package: `ihe.iti.pixm@3.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 11 | 11 | 100% |
| Random Validation Parity | 11 | 11 | 100% |
| Random Generation Validation + Parity | 4 | 11 | 36% |


---

## Empty Validation Parity Results

### ✅ Passing (11)
- ✅ PIXmPatientBirthDateRequiredClass
- ✅ PIXmPatientClass
- ✅ AuditPixmFeedManagerCreateClass
- ✅ AuditPixmFeedManagerDeleteClass
- ✅ AuditPixmFeedManagerUpdateClass
- ✅ AuditPixmFeedSourceDeleteClass
- ✅ AuditPixmFeedSourceUpdateClass
- ✅ AuditPixmQueryConsumerClass
- ✅ AuditPixmQueryManagerClass
- ✅ PIXmQueryParametersInClass
- ✅ PIXmQueryParametersOutClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (11)
- ✅ PIXmPatientBirthDateRequiredClass
- ✅ PIXmPatientClass
- ✅ AuditPixmFeedManagerCreateClass
- ✅ AuditPixmFeedManagerDeleteClass
- ✅ AuditPixmFeedManagerUpdateClass
- ✅ AuditPixmFeedSourceDeleteClass
- ✅ AuditPixmFeedSourceUpdateClass
- ✅ AuditPixmQueryConsumerClass
- ✅ AuditPixmQueryManagerClass
- ✅ PIXmQueryParametersInClass
- ✅ PIXmQueryParametersOutClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (4)
- ✅ PIXmPatientBirthDateRequiredClass
- ✅ PIXmPatientClass
- ✅ PIXmQueryParametersInClass
- ✅ PIXmQueryParametersOutClass

### ❌ Failing (7)
- ❌ AuditPixmFeedManagerCreateClass (3 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
    - Missing required member: 'identifier' (for slice patient)
    - Instance count at element 'reference' is 1, which is not within the specified cardinality of 0..0 (for slice patient)
- ❌ AuditPixmFeedManagerDeleteClass (3 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
    - Missing required member: 'identifier' (for slice patient)
    - Instance count at element 'reference' is 1, which is not within the specified cardinality of 0..0 (for slice patient)
- ❌ AuditPixmFeedManagerUpdateClass (3 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
    - Missing required member: 'identifier' (for slice patient)
    - Instance count at element 'reference' is 1, which is not within the specified cardinality of 0..0 (for slice patient)
- ❌ AuditPixmFeedSourceDeleteClass (3 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
    - Missing required member: 'identifier' (for slice patient)
    - Instance count at element 'reference' is 1, which is not within the specified cardinality of 0..0 (for slice patient)
- ❌ AuditPixmFeedSourceUpdateClass (3 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
    - Missing required member: 'identifier' (for slice patient)
    - Instance count at element 'reference' is 1, which is not within the specified cardinality of 0..0 (for slice patient)
- ❌ AuditPixmQueryConsumerClass (2 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
    - Missing required member: 'identifier' (for slice patient)
- ❌ AuditPixmQueryManagerClass (2 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
    - Missing required member: 'identifier' (for slice patient)

---

[← Back to Summary](./pipeline-parity-summary.md)
