# INJ - Injection Flaws (C)

### Related CWE(s): CWE-74
### Related CVE(s): ARAŞTIRILMADI

When input originating from a user controlled (we can say also attacker controlled) source is used to construct a command, data structure, or record, and the system does not properly sanitize or neutralize special characters ,or fails to apply a whitelist, these elements may influence how the data is interpreted by downstream components. There are many different types of injection attacks, we tried to cover these attacks in this category.