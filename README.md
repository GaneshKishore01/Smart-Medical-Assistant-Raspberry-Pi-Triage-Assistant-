# raspberry-pi-triage
A Raspberry Pi 5–based triage assistant with LCD display .   Classifies patients into categories (Red/Yellow/Green) for emergency response.   Designed for **offline, low-resource healthcare settings**.
# Compact Medical Triage Device

![Image Alt](https://github.com/GaneshKishore01/raspberry-pi-triage/blob/main/Triage%20color%20system.jpg)
## Overview
https://github.com/GaneshKishore01/raspberry-pi-triage/blob/main/Triage%20color%20system.jpg
A Raspberry Pi 5–based medical triage assistant with a 3.5-inch LCD display.  
The system uses a lightweight LLM (Phi-3 Qt) to classify patients into categories:
- 🔴 Red (immediate urgency)  
- 🟡 Yellow (moderate urgency)
- 🟢 Green (low urgency)

Designed for **offline, low-resource healthcare settings**.

## Features
- Runs locally on Raspberry Pi 5  
- Lightweight model inference with Phi-3 Qt  
- Symptom-based triage decision-making  
- Portable with LCD integration

## Results
✅ Functional prototype tested with simulated patient data  
⚠️ Limitations: ~2.5 tokens/sec inference speed, overheating → required active cooling  

## Future Directions
- Hardware optimization for faster inference  
- Camera module integration for symptom capture  
- Real-world validation with healthcare professionals  

---

*This is a showcase repo. Detailed source code remains private.*
