# Lab 5: Static Code Analysis — Issues and Fixes

## Issues Identified and Fixed

| No. | Issue | Type | Fix Applied |
|---:|---|---|---|
| 1 | Mutable default argument in `addMoney()` | Bug | Changed `log=[]` to `log=None` and initialized the list inside the function. |
| 2 | Hardcoded gateway secret | Security | Read the gateway secret from the `GATEWAY_SECRET` environment variable. |
| 3 | Weak SHA-1 PIN hashing | Security | Replaced the weak hash with `hashlib.scrypt`. |
| 4 | Insecure temporary file creation using `tempfile.mktemp()` | Security | Replaced it with `tempfile.NamedTemporaryFile()`. |
| 5 | Insecure OTP generation using `random.randint()` | Security | Used `secrets.randbelow()` to generate a six-digit OTP. |
| 6 | PIN comparison | Security | Used `hmac.compare_digest()` for comparison. |
| 7 | Missing module and function docstrings | Code quality | Added documentation strings. |
| 8 | Non-standard naming conventions | Code quality | Renamed functions and variables to follow Python naming conventions. |
| 9 | Unused function parameter | Code quality | Explicitly handled the unused merchant type parameter. |
| 10 | Missing final newline and formatting violations | Style | Corrected formatting and ensured the file ends with a newline. |
| 11 | Global statement warning | Code quality | Stored the daily limit in a configuration dictionary instead of using a global statement. |

## Verification Results

- Pylint score: 10.00/10
- Bandit: No issues identified.
- Flake8: No issues reported.
- Python compilation: Successful.
- Program execution: Successful.

## Conclusion

Static analysis helped identify security vulnerabilities, potential bugs, naming convention violations, and formatting problems. After applying the fixes, all three tools were rerun to verify the corrected code.
