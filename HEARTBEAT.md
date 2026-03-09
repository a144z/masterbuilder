# HEARTBEAT.md - Periodic Task Checklist

## Trigger
Heartbeat prompt: Read this file. Follow tasks in order. If nothing critical, reply: HEART_OK

## Execution Schedule
- **Frequency**: Every 2-4 hours
- **Timezone**: Asia/Hong_Kong (HKT)

---

## Priority 1: Project Health (Run EVERY heartbeat)

### 1.1 GitHub Status Check
```bash
cd /home/jk/.openclaw/workspace
git status
gh repo view a144z/masterbuilder --json visibility,updatedAt
```
- Check for uncommitted changes
- Verify repo visibility (should be private)
- Note last update time

### 1.2 Code Quality Scan
```bash
# Check for outdated dependencies
npx npm-check-updates -u
# Check for linting issues
npx eslint . --max-warnings=0
# Check for security vulnerabilities
npm audit
```

### 1.3 Documentation Status
- Review `MEMORY.md` for stale info
- Check `PROJECT_README.md` for accuracy
- Verify all .md files are current

---

## Priority 2: Trend Research (Run EVERY heartbeat)

### 2.1 Web3/Tech Trend Discovery
- Search X (Twitter) for: "web3 trends 2026", "crypto dev tools"
- Search Reddit: r/web3, r/programming, r/ai
- Look for:
  - Emerging frameworks
  - New tools/SDKs
  - Developer pain points
  - Community discussions

### 2.2 a144z/masterbuilder Specific Checks
- Check for new issues/PRs on GitHub
- Monitor related repositories
- Track version updates in ecosystem

---

## Priority 3: Vibe Code Updates (Run EVERY 3rd heartbeat)

### 3.1 Vibe Audit
```bash
# Check for SOTA standards
npx npm outdated
npx npx-check
# Review package.json for modern syntax
# Check for deprecated APIs
```

### 3.2 Code Refactoring
- Simplify complex functions
- Add missing error handling
- Improve type safety
- Update comments/docs
- Standardize code style

### 3.3 Push Updates
- Commit with format: "AI: [action] - [description]"
- Push to main branch
- Update README with changes

---

## Priority 4: Memory Maintenance (Run EVERY 5th heartbeat)

### 4.1 Memory Cleanup
- Read recent `memory/YYYY-MM-DD.md` files
- Identify significant events/insights
- Update `MEMORY.md` with distilled learnings
- Archive or remove outdated info

### 4.2 Project Context Review
- Verify all context files are current
- Update `USER.md` if preferences changed
- Refresh `IDENTITY.md` if needed
- Review `SOUL.md` principles

---

## Execution Order (Always Follow)

1. **GitHub Status** → Check repo health
2. **Code Quality Scan** → Run npm audit, outdated checks
3. **Documentation Status** → Review and update files
4. **Trend Research** → Search web3/tech trends
5. **Vibe Code Updates** → Refactor and improve (every 3rd)
6. **Memory Maintenance** → Update long-term memory (every 5th)
7. **Response** → Report results or HEART_OK

---

## Commit Standards

**Format**: `AI: [action] - [description]`

**Examples**:
- `AI: add feature - user authentication`
- `AI: refactor - simplify authentication flow`
- `AI: update docs - README improvements`
- `AI: fix bug - resolve login issue`

**Before Pushing**:
- ✅ All .md files updated
- ✅ Commit message follows format
- ✅ No uncommitted changes
- ✅ Tests pass (if applicable)

---

## Tools Reference

### Git Commands
```bash
cd /home/jk/.openclaw/workspace
git add .
git commit -m "AI: [action] - [description]"
git push origin main
```

### Dependency Updates
```bash
npx npm-check-updates -u
npm install
```

### Documentation Updates
```bash
# Edit files in workspace
# Then commit and push
```

---

## Response Rules

- **Nothing critical**: Reply `HEART_OK`
- **Issues found**: Report what needs attention
- **Updates made**: Summarize changes
- **Trends found**: List interesting findings

---

Last Updated: 2026-03-10
