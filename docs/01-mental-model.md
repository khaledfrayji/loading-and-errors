# 🧠 Mental Model: How Next.js Handles Errors

In Next.js 16, errors are not handled with `try/catch`.

They are handled by the **filesystem**.

---

## 🧩 Two Types of Errors

### 1. Expected Errors

* Missing data
* Validation issues
* Controlled outcomes

👉 These should NOT be thrown
👉 They are handled explicitly

According to Next.js:
Expected errors should be modeled as return values instead of exceptions ([Next.js][1])

---

### 2. Unexpected Errors

* Bugs
* Crashes
* Runtime failures

👉 These are caught by:

* `error.tsx`
* `global-error.tsx`

---

## 🧠 The Core Insight

> Errors are routed through the **folder structure**

---

## 🧭 High-Level Flow

Request → Route → Data → Render

At each step, Next.js decides:

* Not found?
* Crashed?
* Root failed?

---

## ⚡ Key Idea

> Every failure type has a **dedicated file**

[1]: https://nextjs.org/docs/app/getting-started/error-handling
