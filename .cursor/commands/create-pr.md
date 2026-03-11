---
description: Generate a PR with conventional commit description
---

Review all staged and unstaged changes in the current branch compared to `main`.

Generate a pull request with:
1. **Title**: Conventional commit format (`feat:`, `fix:`, `refactor:`, etc.)
2. **Description** with these sections:
   - ## Summary (2-3 sentences)
   - ## Changes (bullet list of key changes)
   - ## Testing (how this was tested)
   - ## Checklist
     - [ ] Tests pass
     - [ ] No linting errors
     - [ ] Documentation updated (if applicable)
     - [ ] Breaking changes noted (if applicable)

3. Create the branch and commit if not already done
4. Push and create the PR via Git CLI
