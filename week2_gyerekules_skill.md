# Skill: Gyerekülés Vélemény Elemző
Version: 1.0
Author: [László]
Created: 2026-02-05

## Mire jó ez a skill?
Elemzi a gyerekülés vásárlói véleményeket.
Kiszedi a top 3 problémát rangsorolva (high/medium/low).
Használható webshop értékelésekhez, termékfejlesztésekhez.

## Inputs (mit kell megadni)
- velemeny: string "A szék jó, de nehéz felemelni. Szíj beállítása nehézkes."

## Output (json eredmény)
```json
{
  "summary": "string",
  "pain_points": [{"description": "string", "severity": "low|medium|high"}]
}
```

## Használati példa

Input:
"A szék jó, de nehéz felemelni. Szíj beállítása nehézkes."

Output (várható JSON struktúra):
{
  "summary": "A vásárló szerint az ülés alapvetően jó, de a mindennapi használatot nehezíti a súly és a szíj beállítása.",
  "pain_points": [
    {
      "description": "Az ülés túl nehéz, nehéz felemelni és mozgatni.",
      "severity": "high"
    },
    {
      "description": "A biztonsági öv/szíj beállítása nehézkes.",
      "severity": "medium"
    },
    {
      "description": "A kényelem nem tökéletes a mindennapi használathoz.",
      "severity": "low"
    }
  ]
}
