---
type: moc
tags: [moc, dermatology]
---

# 🗂 Dermatology map

> [!tip] How this vault works
> Every disease is a **hub note** with Theory, Practical and Exam pages. Things that appear in many diseases (Koebner, methotrexate, phototherapy, topical steroids) are **their own notes**, so you learn them once and see every disease that uses them in the **Backlinks** pane.
> ➕ = added beyond the WAQF book (standard teaching, verify against your department's references).

## Diseases (builds itself from each note's properties)
```dataview
TABLE group, koebner AS "Koebner", key_sign AS "Key sign", first_line AS "First line"
FROM #disease
SORT group ASC, file.name ASC
```

## Papulosquamous side-by-side
```dataview
TABLE koebner AS "Koebner", itch AS "Itch", histology_key AS "Histology", key_sign AS "Key sign"
FROM #papulosquamous
```
Static comparison with discriminators: [[Papulosquamous DDx]]

## Drugs and treatments
```dataview
TABLE class AS "Class", key_toxicity AS "Key toxicity", monitoring AS "Monitor"
FROM #drug OR #treatment
SORT file.name ASC
```

## Diseases done so far
- [[Psoriasis]]
- Next: [[Lichen Planus]] · [[Pityriasis rosea]] · [[Eczema]] · [[Acne]]

## One-time setup
1. Settings → Community plugins → install **Dataview** (needed for the tables above) and **Spaced Repetition** (for the `:::` flashcards).
2. Settings → Core plugins → turn on **Templates**, set template folder to `_Templates`.
3. Graph view → Groups: `tag:#disease` (red), `tag:#drug` (blue), `tag:#sign` (yellow), `tag:#treatment` (green). Now the graph is a real map.
