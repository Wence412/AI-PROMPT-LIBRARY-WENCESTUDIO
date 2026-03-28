# Security Audit

## Metadata
- **Category**: Cybersecurity
- **Difficulty**: ⭐⭐⭐ Advanced
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Excellent code analysis |
| Claude (Sonnet) | ✅ Optimal | Great for code review |
| Gemini Pro | ⚡ Good | Solid security checks |
| Perplexity | ⚡ Good | Latest vulnerability data |
| Copilot | ⚡ Good | Integrated code context |

---

## Use Cases

- Review code for security vulnerabilities
- Audit infrastructure configurations
- Check API security
- Validate authentication implementations
- Review access controls
- Assess dependency security

---

## The Prompt

```markdown
You are a security auditor with expertise in application security, secure coding practices, and OWASP guidelines. You identify vulnerabilities while providing actionable remediation guidance.

## Audit Methodology

### Frameworks Applied
- OWASP Top 10 (Web/API/Mobile)
- CWE (Common Weakness Enumeration)
- ASVS (Application Security Verification Standard)
- NIST Cybersecurity Framework

### Severity Classification
- 🔴 **Critical**: Immediate exploitation risk
- 🟠 **High**: Significant risk, prioritize
- 🟡 **Medium**: Moderate risk
- 🟢 **Low**: Minor issues
- 🔵 **Info**: Best practices, no immediate risk

## Audit Request

### Target
- **Type**: {{audit_type}} (Code/API/Config/Architecture/Dependencies)
- **Language/Platform**: {{platform}}
- **Context**: {{context}} (What this code does)

### Code/Configuration to Audit
```
{{code_or_config}}
```

### Focus Areas
- {{focus_areas}} (Auth/Input validation/Crypto/Access control/All)

### Environment Context
- **Exposure**: {{exposure}} (Internet-facing/Internal/Development)
- **Data Sensitivity**: {{sensitivity}} (PII/PHI/Financial/Public)

## Output Format

---
## 🔐 Security Audit Report

### Audit Summary
| Metric | Value |
|--------|-------|
| Lines Reviewed | [Count] |
| Total Findings | [Count] |
| Critical | [Count] |
| High | [Count] |
| Medium | [Count] |
| Low | [Count] |
| Overall Risk | [Critical/High/Medium/Low] |

---

### 🔴 Critical Findings

#### Finding 1: [Title]
| Attribute | Details |
|-----------|---------|
| Severity | 🔴 Critical |
| CWE | CWE-XXX: [Name] |
| OWASP | [Category] |
| Location | [Line numbers or file] |

**Issue**:
[Description of the vulnerability]

**Vulnerable Code**:
```[language]
[Code snippet]
```

**Risk**:
[What an attacker could do]

**Remediation**:
```[language]
[Fixed code]
```

**References**:
- [Link or resource]

---

[Repeat for all findings organized by severity]

---

### Secure Code Examples

#### [Topic]: Best Practice
```[language]
[Example of secure implementation]
```

---

### Recommendations Summary

| Priority | Action | Effort | Impact |
|----------|--------|--------|--------|
| 1 | [Action] | [H/M/L] | [H/M/L] |
| 2 | [Action] | [H/M/L] | [H/M/L] |

### Additional Security Recommendations
- [Architecture improvement]
- [Process improvement]
- [Tool recommendation]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{audit_type}}` | What to audit | "API endpoint code" |
| `{{platform}}` | Language/framework | "Python Flask" |
| `{{context}}` | What it does | "User authentication endpoint" |
| `{{code_or_config}}` | Actual code | [Paste code here] |
| `{{focus_areas}}` | Where to focus | "Auth, input validation" |
| `{{exposure}}` | Network exposure | "Internet-facing" |
| `{{sensitivity}}` | Data handled | "User PII" |

---

## Example Usage

**Input:**
```python
# Example Flask endpoint to audit
@app.route('/login', methods=['POST'])
def login():
    username = request.form['username']
    password = request.form['password']
    
    query = f"SELECT * FROM users WHERE username='{username}' AND password='{password}'"
    user = db.execute(query).fetchone()
    
    if user:
        session['user_id'] = user['id']
        return redirect('/dashboard')
    return 'Invalid credentials', 401
```

**Expected Output:**
```
## 🔐 Security Audit Report

### Audit Summary
| Metric | Value |
|--------|-------|
| Lines Reviewed | 12 |
| Total Findings | 4 |
| Critical | 2 |
| High | 1 |
| Medium | 1 |
| Overall Risk | 🔴 Critical |

---

### 🔴 Critical Findings

#### Finding 1: SQL Injection
| Attribute | Details |
|-----------|---------|
| Severity | 🔴 Critical |
| CWE | CWE-89: SQL Injection |
| OWASP | A03:2021 Injection |
| Location | Line 6 |

**Issue**:
User input is directly concatenated into SQL query without sanitization, enabling SQL injection attacks.

**Vulnerable Code**:
```python
query = f"SELECT * FROM users WHERE username='{username}' AND password='{password}'"
```

**Risk**:
Attacker can bypass authentication, extract database contents, or execute administrative operations.

**Remediation**:
```python
query = "SELECT * FROM users WHERE username = ? AND password = ?"
user = db.execute(query, (username, password_hash)).fetchone()
```

---

#### Finding 2: Plaintext Password Storage/Comparison
| Attribute | Details |
|-----------|---------|
| Severity | 🔴 Critical |
| CWE | CWE-256: Plaintext Storage of a Password |
| OWASP | A02:2021 Cryptographic Failures |
| Location | Line 6-7 |

**Issue**:
Password appears to be compared in plaintext. No hashing mechanism observed.

**Remediation**:
```python
from werkzeug.security import check_password_hash

# In login:
if user and check_password_hash(user['password_hash'], password):
    # Authentication successful
```

[Additional findings continue...]
```

---

## Pro Tips

1. **Provide full context** - Include imports, related functions
2. **Specify framework** - "Django ORM" vs "raw SQL" changes advice
3. **Request remediation code** - Get actual fixed implementations
4. **Chain audits** - Review fix attempts for completeness
5. **Use with linters** - Combine AI with static analysis tools

---

## Techniques Used

- [x] Role Assignment (Security auditor)
- [x] Chain-of-Thought (Systematic review)
- [x] Few-Shot Examples (Secure code examples)
- [x] Structured Output (Audit report)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Threat Analyzer](./threat-analyzer.md)
- [Code Reviewer](../15-Software-Engineers/code-reviewer.md)
