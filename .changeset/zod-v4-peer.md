---
"@withtyped/server": minor
---

support zod 4 alongside zod 3.25+

The `zod` peer dependency is widened to `^3.25.0 || ^4.0.0`, the range Zod recommends for libraries that support both majors. Two model guards changed to behave the same on both: `json` columns use `z.record(z.string(), z.unknown())` (Zod 4 drops the single-argument form), and readonly fields use `z.undefined().optional()`, since Zod 4 only lets an object key be absent when its schema is optional.
