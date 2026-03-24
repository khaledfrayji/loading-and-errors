# 🌍 global-error.tsx — Full Application Crash

## 📌 What It Is

A global fallback when the **entire app fails**.

---

## 🧠 Why It Exists

Because:

> `error.tsx` cannot catch errors in the root layout ([Next.js][1])

---

## ⚡ Behavior

* Replaces the entire app
* Must include `<html>` and `<body>`

---

## 📍 Scope

* Root layout failures
* Critical crashes

---

## 🧠 Mental Model

> “Last line of defense”

---

## 🎤 Teaching Line

> If this renders… your app is already dead.

