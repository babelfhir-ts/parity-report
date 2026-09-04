# pixm - Detailed Report (FHIR all)
Generated: 2026-08-29T11:16:02.754Z

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
    - The Audit Source is this agent too.
    - AuditEvent.entity:patient.what.reference: max allowed = 0, but found 1
    - AuditEvent.entity:patient.what.identifier: minimum required = 1, but only found 0
- ❌ AuditPixmFeedManagerDeleteClass (3 errors)
    - The Audit Source is this agent too.
    - AuditEvent.entity:patient.what.reference: max allowed = 0, but found 1
    - AuditEvent.entity:patient.what.identifier: minimum required = 1, but only found 0
- ❌ AuditPixmFeedManagerUpdateClass (3 errors)
    - The Audit Source is this agent too.
    - AuditEvent.entity:patient.what.reference: max allowed = 0, but found 1
    - AuditEvent.entity:patient.what.identifier: minimum required = 1, but only found 0
- ❌ AuditPixmFeedSourceDeleteClass (3 errors)
    - The Audit Source is this agent too.
    - AuditEvent.entity:patient.what.reference: max allowed = 0, but found 1
    - AuditEvent.entity:patient.what.identifier: minimum required = 1, but only found 0
- ❌ AuditPixmFeedSourceUpdateClass (3 errors)
    - The Audit Source is this agent too.
    - AuditEvent.entity:patient.what.reference: max allowed = 0, but found 1
    - AuditEvent.entity:patient.what.identifier: minimum required = 1, but only found 0
- ❌ AuditPixmQueryConsumerClass (2 errors)
    - The Audit Source is this agent too.
    - AuditEvent.entity:patient.what.identifier: minimum required = 1, but only found 0
- ❌ AuditPixmQueryManagerClass (2 errors)
    - The Audit Source is this agent too.
    - AuditEvent.entity:patient.what.identifier: minimum required = 1, but only found 0

---

[← Back to Summary](./pipeline-parity-summary.md)
