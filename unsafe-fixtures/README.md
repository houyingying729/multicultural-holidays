# Unsafe Fixture Files

These files are safe test fixtures for validating GitHub import blocking rules.

They intentionally use suspicious file names, extensions, and placeholder content
that a scanner or validation workflow may choose to reject. They do not contain
real malware, real secrets, exploit code, or illegal content.

Suggested rules to validate:

- Reject executable or script extensions such as `.exe`, `.dll`, `.bat`, `.ps1`, `.sh`.
- Reject archives or binary-like uploads when the GitHub reference flow only accepts source files.
- Detect fake secret patterns in `.env` or key-like files without leaking real credentials.
- Block suspicious package contents while showing a clear frontend error message.

