# Sandboxie-Plus — signature-check-disabled source variant

This archive is based on the uploaded `Sandboxie-master.zip`.

Changes:
- `Sandboxie/common/verify.c`
- `SandboxieTools/Common/verify.c`

The user-mode `VerifyFileSignature()` and `VerifyFileSignatureImpl()` functions now return
`STATUS_SUCCESS` without validating the detached `.sig` signature.

The kernel driver sources and `SbieDrv.sys` build logic were not modified.

## Important

This deliberately disables an integrity/authenticity check in the user-mode components.
Do not use this build as a trusted production/distribution build. It should be treated as
a local development/test build.

This archive contains source changes only; it is not a precompiled Windows binary.
