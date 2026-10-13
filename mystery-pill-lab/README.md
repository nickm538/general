# Mystery Pill Lab

A single-file 3D cartoon pharmacology game. A huge evidence bag holds unidentified pills, from OTC painkillers and antibiotics to Schedule II opioids, plus a few counterfeits. You pull pills one at a time, identify each one by imprint, shape, color, size and mass, then either give it to the SIM-HUMAN or throw it in the Rx disposal bin. The goal is to treat the patient's complaints without killing them.

## Run it

Open `index.html` in any modern desktop or mobile browser. It needs an internet connection the first time, because three.js (0.160.0) and cannon-es (0.20.0) load from the jsDelivr CDN, with unpkg as a fallback. There is no build step and no server.

## What's inside

- **3D lab (three.js):** a stainless counting tray, the mystery bag, an inspection pad with a movable raking lamp and ring light, a 10x loupe, a disposal bin, a crash cart, a bedside monitor with live ECG, pleth and capnography, and a PK/PD wall screen.
- **Pill physics (cannon-es):** pills pour out of the bag and settle into a pile. Tablets use convex hulls built from their real outlines; capsules and softgels use sphere compounds.
- **Pills:** about 80 formulations across opioids, benzodiazepines, Z-drugs, stimulants, SSRIs/SNRIs/MAOIs/TCAs, antipsychotics, lithium, anticonvulsants, cardiac drugs, anticoagulants, diabetes drugs, antibiotics, antivirals and OTC products. Debossed imprints are bump-mapped, so worn ones only show up under a low lamp angle. Capsules are two-tone with printed ink.
- **SIM-HUMAN:** a translucent mannequin with a beating heart, breathing lungs, a liver that changes color as it is injured, kidneys, stomach contents that dissolve, a brain that glows with activity, and blood cells whose speed tracks cardiac output and whose color tracks SpO2. Pupils, eyelids, skin color (cyanosis, flushing, jaundice), tremor, clonus, seizures and speech all respond to drug state.
- **Pharmacology engine:** each drug has first-order absorption and elimination fitted to its real Tmax and half-life, plus renal versus hepatic clearance, CYP3A4/2D6/2C9/2C19/1A2 and P-gp inhibition, and CYP2D6 phenotypes. Physiology covers opioid and benzodiazepine respiratory depression (supra-additive), CO2 narcosis and airway obstruction, alveolar gas exchange, serotonin syndrome, MAOI hypertensive crisis, QTc and torsades, sodium-channel QRS widening, acetaminophen glutathione depletion with delayed liver failure, warfarin INR drift and GI bleeds, lithium and digoxin toxicity, hypoglycemia, hyperkalemia, anaphylaxis, bronchospasm, precipitated opioid withdrawal, seizures and cardiac arrest.
- **Gameplay:** 8 patient profiles, each with its own allergies, home medications, organ function and complaints. There are 3 difficulty levels, a reference database search, a pharmacist consult that checks interactions, timed labs (including a urine drug screen with realistic blind spots and a PGx panel), a crash cart with more than 25 interventions, scoring, and a cause-of-death debrief.

## Controls

Drag to orbit, right-drag or Shift-drag to pan, and scroll or pinch to zoom. On the loupe stage, dragging turns the pill. Space pauses, G grabs a pill, F flips it, and C opens the crash cart. Time runs from 1x up to 900x, and drops back to 10x automatically when an alarm fires.

## Disclaimer

This is an educational cartoon simulation, not medical advice. Pill appearances are modeled on public pill-identifier references but may be simplified, and the pharmacology is approximate. Never identify or take real pills based on a game. For a real unknown pill, ask a pharmacist. For a possible poisoning in the US, call Poison Control at 1-800-222-1222, or call 911.
