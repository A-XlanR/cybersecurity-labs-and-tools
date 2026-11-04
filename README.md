# cybersecurity-labs-and-tools

## SQL Injection in WHERE clause.
Payload used: 'OR 1=1--.
Remediation: Use parameterized queries to sanitize input.

## SQL Injection Bypass Login
Payload used: administration'--.
Remediation: Use parameterized queries to sanitize input.

## SQL UNION Injection
Payload user: 'UNION SELECT BANNER, NULL FROM v$version-- (used to display database version)
Remediation: Use parameterized queries to sanitize input.
EX in python: # The database treats %s strictly as a literal value, neutralizing the payload
                query = "SELECT * FROM products WHERE category = %s"
                cursor.execute(query, (user_input,))
