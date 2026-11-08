<p align="center">
  <img src="https://sncfoundation.github.io/logos/sheetwire.svg" width="96" alt="SheetWire logo">
</p>

<h1 align="center">SheetWire</h1>

<p align="center"><b>The gateway that lets **real database clients connect to a spreadsheet**.</b><br>
A <a href="https://sncfoundation.github.io">Sheet-Native Computing Foundation</a> project · the spreadsheet-native <b>Postgres/Redis/Mongo wire protocols</b></p>

---

**Status:** 📝 Unsaved Draft &#183; **design only**. Data & Storage TAG. This repository holds the design below and no code: no wire-protocol gateway exists yet, so `psql` will not connect to your Sheet today. Implementation is tracked in [sncfoundation/sheeternetes#50](https://github.com/sncfoundation/sheeternetes/issues/50).

The name already ships elsewhere, though: [`sheetwire.py`](https://github.com/sncfoundation/sheeternetes-onprem/blob/main/sheetwire.py) in [sheeternetes-onprem](https://github.com/sncfoundation/sheeternetes-onprem#cross-substrate-networking-sheetwire) is a working TCP relay that uses a shared Sheet as the wire between two clusters behind NAT. That is where SheetWire code lives today; the database-protocol gateway described here would grow on top of it.

## The mapping

- A local process implements the **wire protocol** of Postgres / MySQL / Redis / MongoDB and translates queries to the Sheets API / `QUERY()`.
- So `psql`, `mysql`, `redis-cli`, `mongosh` connect to a Google Sheet as if it were the real database.

## Honest limit

Bounded by Sheets latency & quotas; a translation layer, not a storage engine. The killer demo of the whole data stack.

## Connect with real clients

Once this gateway exists, real Postgres, MySQL, Redis and MongoDB clients will be able to connect to a Google Sheet over their native wire protocols. Not before.

- 🗺️ [SNCF Landscape](https://sncfoundation.github.io/landscape.html) · 🧩 [Projects](https://sncfoundation.github.io/projects.html) · 🎓 [Certification](https://sncfoundation.github.io/certification.html)

---

<sub>Apache-2.0. Do not run production data on a spreadsheet. If you do, please film the query plan.</sub>
