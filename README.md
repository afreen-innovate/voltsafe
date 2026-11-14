# 🔋 VoltSafe

**Scan it. Store it. Drop it safely.**

VoltSafe helps people spot risky lithium-ion batteries at home, store them safely, and take them to a proper collection point, instead of throwing them in household waste.

**Live demo:** https://afreen-innovate.github.io/voltsafe/

---

## The problem (P13, Track 4: Batteries, Energy and Awareness)

Damaged or old lithium-ion batteries (phones, power banks, earbuds, toys) are often thrown into household waste. They cause fires in garbage trucks and landfills, leak toxic chemicals, and are hard to tell apart from normal waste. Most people can't tell a risky battery from a normal one, don't know how to store it safely, and don't know where to take it.

## How VoltSafe works

**Check → Act → Drop → Proof**

1. **Check:** Pick the battery type and answer 5 quick questions (swollen? hot while idle? leaking or smell? dropped or water damaged? older than 3 years?). A rule-based engine gives a **Green / Amber / Red** risk level.
2. **Act:** A Safety Card shows clear steps for that level, in English and Tamil.
3. **Drop:** Smart Routing shows the nearest suitable drop-off point. Red batteries go only to hazardous-handling points.
4. **Proof:** A Safe Drop QR token is scanned at the collection point to confirm the battery arrived safely, and the Impact Dashboard updates.

## Risk levels

| Level | Meaning | What to do |
|---|---|---|
| ✔ **Green** | OK | Keep using it. Recycle at end of life. |
| ! **Amber** | Risky | Keep in a cool, dry, non-metal box. Tape the terminals. Dispose within 7 days. |
| ✖ **Red** | Needs special handling | Stop charging. Keep away from flammables. Store in sand or a ceramic container. Tape the terminals. Do not bin it. Take it to a hazardous-handling point. |

> If a battery is hot, smoking or hissing: move away, don't touch it, and call the fire service (**101**).

## Features

- Risk Scanner with Green / Amber / Red result
- Safety Card with step-by-step guidance (English / Tamil)
- Smart Routing to the nearest drop-off point (sample data)
- Safe Drop QR token for verified drop-offs
- Impact Dashboard: scans, red alerts caught, verified drop-offs, kg diverted, risk before vs. after
- Mobile-first, single-file web app

## Planned hardware (prototype)

- **Battery Checker (ESP32):** INA219 (voltage/current), MLX90614 (temperature), VL53L0X (swelling thickness), MQ-2/VOC gas sensor, OLED and RGB LED showing the risk level.
- **SafeBin Node:** sand-lined metal compartment, temperature and smoke sensors, buzzer, HX711 load cell, servo lock that opens only on a valid QR token, WiFi/MQTT alerts to the dashboard.

The app works fully without hardware. The sensors add measured data on top of the questions.

## What makes it different

Existing tools only locate or collect batteries. VoltSafe assesses risk and verifies safe disposal from start to finish: risk scan, guidance, routing, QR-verified drop, and a measured risk reduction.

## Impact measure

- Fewer batteries entering household waste
- Lower risk level (before vs. after drop-off)

## Tech stack

- HTML, CSS and JavaScript (single-file PWA-style web app)
- Sample JSON data for drop-off points
- Planned: Firebase or Node + SQLite backend, ESP32 with MQTT

## Run it locally

1. Download `index.html`.
2. Open it in any browser.

No install or build step is needed.

## Note

Drop-off locations and dashboard numbers in this demo are **sample data**.

## Author

Built by **afreen-innovate** for the hackathon, Problem P13.
