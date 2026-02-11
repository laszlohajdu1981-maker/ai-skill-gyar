# Skill: Foldable Telefon Törésteszt Elemző
Version: 1.0
Author: [A te neved]  
Created: 2026-02-07

## Mire jó ez a skill?
YouTube töréstesztek elemzése.  
Kiszedi a törési sorrendet, javítási nehézségi szinteket.

## Inputs  
- **video_iras**: string
  Példa: "JerryRig Razr Ultra 2026: 1.8m esésnél összetörik, hinge 500k fold OK"

## JSON Prompt sablon


## TESZT
TÖRÉSTEST: "JerryRig Razr Ultra 2026: 1.8m esésnél a külső kijelző összetörik. Hinge 500k fold után is OK. Belső kijelző karcolásnál meghal."

{
  "phone_model": "Motorola Razr Ultra 2026",
  "break_sequence": [
    "1. Külső kijelző: 1.8m drop után összetörik", 
    "2. Belső kijelző: Karcolásnál meghal",
    "3. Hinge: 500k fold után OK"
  ],
  "repair_difficulty": {
    "screen": "hard",
    "hinge": "medium"
  },
  "durability_score": "5/10"
}
**TESZT: Razr Ultra = közepes foldable (külső kijelző gyenge)!**
