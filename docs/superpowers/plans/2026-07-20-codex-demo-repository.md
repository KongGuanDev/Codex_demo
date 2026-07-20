# codex_demo Repository Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create a public GitHub repository named `codex_demo` for `KongGuanDev` with a single README.

**Architecture:** Use GitHub's authenticated repository-creation page to perform the external write. Then verify the public repository URL and re-query the connected GitHub app after its index refreshes.

**Tech Stack:** GitHub web application; Codex GitHub connector

## Global Constraints

- Owner must be `KongGuanDev`.
- Repository name must be `codex_demo`.
- Visibility must be public.
- Initialize with `README.md` only; do not add a license or `.gitignore`.

---

### Task 1: Create and verify the repository

**Files:**
- Create remotely: `KongGuanDev/codex_demo/README.md`

**Interfaces:**
- Consumes: authenticated GitHub session for `KongGuanDev`
- Produces: public repository URL `https://github.com/KongGuanDev/codex_demo`

- [ ] **Step 1: Open GitHub's new repository page**

Open `https://github.com/new` in the authenticated browser session.

- [ ] **Step 2: Configure the repository**

Set owner to `KongGuanDev`, repository name to `codex_demo`, visibility to `Public`, enable README initialization, leave `.gitignore` and license unset.

- [ ] **Step 3: Create the repository**

Submit the form once and wait for GitHub to redirect to `https://github.com/KongGuanDev/codex_demo`.

- [ ] **Step 4: Verify the public result**

Open `https://github.com/KongGuanDev/codex_demo` without relying on connector indexing and confirm that the default branch contains `README.md`.

- [ ] **Step 5: Verify connector discovery**

Query the connected GitHub app for `codex_demo`. If it is absent immediately, report the expected GitHub indexing delay and retry after repository access is configured.
