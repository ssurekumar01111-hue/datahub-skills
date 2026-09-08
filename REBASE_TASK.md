# Rebase Task for feat/datahub-decision-provenance

## Objective
Rebase the `feat/datahub-decision-provenance` branch onto the latest `main` from datahub-project/datahub-skills and push it back to the fork.

## Current State
- Active branch: `feat/datahub-decision-provenance`
- Fork: `https://github.com/ssurekumar01111-hue/datahub-skills`
- Upstream: `https://github.com/datahub-project/datahub-skills`
- Branch is currently 39 days behind main
- Contains 1 new file: `skills/datahub-decision-provenance/SKILL.md`

## Steps to Complete

1. **Fetch the latest main from upstream:**
   ```bash
   git fetch https://github.com/datahub-project/datahub-skills.git main:main-upstream
   ```

2. **Rebase current branch onto the fetched main:**
   ```bash
   git rebase main-upstream
   ```
   - If there are no conflicts, this will complete immediately
   - If conflicts occur, resolve them and run: `git rebase --continue`

3. **Force-push the rebased branch to your fork:**
   ```bash
   git push --force-with-lease origin feat/datahub-decision-provenance
   ```

4. **Verify the rebase succeeded:**
   - Check GitHub PR #71 to confirm it no longer shows "behind main"
   - Verify CI checks pass
   - Branch should now be mergeable

## Expected Outcome
- PR #71 will show "This branch can be automatically merged"
- All CI checks will pass
- The SKILL.md file will be on top of the latest datahub-project/datahub-skills main
- Ready for maintainer review
