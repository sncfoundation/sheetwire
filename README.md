<p align="center">
  <img src="https://sncfoundation.github.io/logos/sheetwire.svg" width="96" alt="SheetWire logo">
</p>

<h1 align="center">SheetWire</h1>

<p align="center"><b>The gateway that lets **real database clients connect to a spreadsheet**.</b><br>
A <a href="https://sncfoundation.github.io">Sheet-Native Computing Foundation</a> project · the spreadsheet-native <b>Postgres/Redis/Mongo wire protocols</b></p>

---

**Status:** 📝 Unsaved Draft (design). Data & Storage TAG.

## The mapping

- A local process implements the **wire protocol** of Postgres / MySQL / Redis / MongoDB and translates queries to the Sheets API / `QUERY()`.
- So `psql`, `mysql`, `redis-cli`, `mongosh` connect to a Google Sheet as if it were the real database.

## Honest limit

Bounded by Sheets latency & quotas; a translation layer, not a storage engine. The killer demo of the whole data stack.

## Connect with real clients

Paired with [SheetWire](https://github.com/sncfoundation/sheetwire), real Postgres/Redis/Mongo wire protocols clients can connect to a Google Sheet over the native wire protocol.

- 🗺️ [SNCF Landscape](https://sncfoundation.github.io/landscape.html) · 🧩 [Projects](https://sncfoundation.github.io/projects.html) · 🎓 [Certification](https://sncfoundation.github.io/certification.html)

---

<sub>Apache-2.0. Do not run production data on a spreadsheet. If you do, please film the query plan.</sub>
