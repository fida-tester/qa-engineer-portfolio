# Defect Metrics & QA Reporting

## Purpose
Defect metrics help teams measure product quality, testing effectiveness,
and release readiness.

These metrics are commonly used in Agile/Scrum QA environments.

---

## 1. Defect Density

**Definition:**  
Number of defects found per module or feature size.

**Formula:**

Defect Density = Total Defects / Size of Feature (Story Points or LOC)

**Example:**
- Checkout module: 12 defects
- Size: 20 story points  
Defect Density = 0.6

---

## 2. Defect Severity Distribution

Tracking defects by severity helps prioritize fixes.

| Severity | Meaning |
|---------|---------|
| Blocker | Testing cannot continue |
| Critical | Major functionality broken |
| Major | Feature works incorrectly |
| Minor | UI or small issue |
| Trivial | Cosmetic only |

---

## 3. Defect Leakage

**Definition:**  
Defects found in production that were missed in QA.

**Formula:**

Leakage % = Production Defects / Total Defects × 100

**Goal:** Keep leakage as low as possible.

---

## 4. Defect Removal Efficiency (DRE)

Measures how effective QA is at catching defects early.

**Formula:**

DRE = Defects found in QA / (QA Defects + Production Defects)

**Example:**
- QA defects: 40  
- Production defects: 5  
DRE = 40 / 45 = 88%

---

## 5. Test Execution Progress

Tracks test completion status during a sprint or release.

| Status | Count |
|--------|------|
| Planned | 120 |
| Executed | 100 |
| Passed | 90 |
| Failed | 10 |
| Blocked | 5 |

---

## 6. Common QA Reports

QA engineers typically provide:

- Daily defect summary
- Sprint
