# CS-340

Maintainable, readable, adaptable.
The interface stays super simple (the four CRUD verbs), with clear names, docstrings, and type hints. Config lives in env vars so I can point the same code at dev/test/prod without edits. The end result: I could tweak dashboard filters and views freely without breaking data code, and the module stays easy to test and reuse.

How I approached the problem.
I started from user needs (e.g., disaster-rescue criteria), turned those into Mongo filters and  indexes, and kept a thin data layer: the dashboard builds a filter, the CRUD module executes it. I wrote tests for the critical paths and added basic logging for errors. Unlike one-off scripts, I treated it like a reusable package—clean interfaces, configurable settings, and small helper functions—so future clients can plug in new rules and queries with minimal changes.

What CS scientists do & why it matters?
They turn messy questions into reliable, repeatable tools: one click becomes a clear query, a fast table, a quick chart. For Grazioso Salvare, that means finding the right animals faster, making consistent data-driven decisions, and having a codebase that scales into reports, APIs, or batch jobs without starting over.
