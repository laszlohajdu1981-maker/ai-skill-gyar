# Skill: AR Szemüveg Összehasonlító
Version: 1.0
Author: [László]
Created: 2026-02-07

## Mire jó ez a skill?
AR szemüvegek összehasonlítása.  
Kamera, akksi, ár/érték rangsor.

## Inputs
- **osszehasonlitas**: string
  Példa: "XREAL One Pro: 1080p, 6g, 500eur. RayNeo Air 3s: 720p, 3g, 300eur"

## JSON Prompt sablon


## TESZT
ÖSSZEHASONLÍTÁS: "XREAL One Pro: 1080p, 6g, 500eur, 4h akksi. RayNeo Air 3s: 720p, 3g, 300eur, 3h akksi."


```json
{
  "models": [
    {
      "name": "XREAL One Pro",
      "resolution": "1080p", 
      "weight": "6g",
      "price": "500eur",
      "battery": "4h"
    },
    {
      "name": "RayNeo Air 3s", 
      "resolution": "720p",
      "weight": "3g",
      "price": "300eur",
      "battery": "3h"
    }
  ],
  "winner": "RayNeo Air 3s",
  "value_score": "8/10", 
  "recommendation": "Buy"
}
