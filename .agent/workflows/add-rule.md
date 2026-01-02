---
description: Add a new rule to clash-mihono.yaml and shadowrocket.conf in alphabetical order with a comment
---

1. **Analyze the Request**:
   - Identify the **domain(s)** to add.
   - Identify the **comment** (if provided).
   - Determine the **target group** (e.g., `google`, `misc`, `openai`, etc.) based on the domain or user input.

2. **Read Configuration Files**:
   - Read `/Users/scoheart/Code/opensource/clash-rules/clash-mihono.yaml` to find the correct `rule-providers` section.
   - Read `/Users/scoheart/Code/opensource/clash-rules/shadowrocket.conf`.

3. **Determine Insertion Points**:
   - For `clash-mihono.yaml`: Find the correct alphabetical position within the target group's `payload`.
   - For `shadowrocket.conf`: Find the correct alphabetical position within the `[Rule]` section (or the corresponding group block).

4. **Update `clash-mihono.yaml`**:
   - use `replace_file_content` or `multi_replace_file_content` to insert the new rule.
   - Format: `- DOMAIN,domain.com # Comment`

5. **Update `shadowrocket.conf`**:
   - use `replace_file_content` or `multi_replace_file_content` to insert the new rule.
   - Format: `DOMAIN,domain.com,USA-amazon # Comment` (Ensure the proxy group `USA-amazon` is correct or matches existing rules).

6. **Verify and Finish**:
   - Confirm the edits were successful.