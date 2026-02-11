# Skill: Webshop Termék Vélemény Elemző
Version: 1.0
Author: [László]
Created: 2026-02-07

## Mire jó ez a skill?
Webshop termékértékeléseket elemez.  
Kiszedi a top 3 vásárlói problémát rangsorolva.

## Inputs
- **velemeny**: string
  Példa: "Telefon jó, de az akksi hamar lemerül. Kamera életlen."

## JSON Prompt sablon

{
"objective": "Elemezd webshop termékértékelést",
"persona": "Webshop termékmenedzser",
"context": {
"product": "Mobiltelefon vagy elektronikai cikk",
"tone": "Elemző, üzleti"
},
"constraints": [
"Max 200 szó",
"Top 3 probléma rangsorolva",
"Csak a véleményből dolgozz"
],
"output_format": {
"summary": "string (2 mondat)",
"pain_points": [
{
"description": "string",
"severity": "low|medium|high"
}
]
}
}
## TESZT
VÉLEMÉNY: "Telefon jó, de az akksi hamar lemerül. Kamera életlen. Ár magas."

{
  "summary": "Vegyes értékelés: jó telefon, de akksi+kamera gyenge.",
  "pain_points": [
    {"description": "Akkumulátor hamar lemerül", "severity": "high"},
    {"description": "Kamera életlen", "severity": "medium"},
    {"description": "Ár magas", "severity": "medium"}
  ]
}
**TESZT: Akkumulátor = #1 kritika (HIGH)!**
