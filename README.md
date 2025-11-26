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
## Setup
Raspberry pi 5 connected to an camera and 3.5 LCD module
![Image Alt](https://github.com/GaneshKishore01/Smart-Medical-Assistant-Raspberry-Pi-Triage-Assistant-/blob/main/Pi%2B3.5%20LCD.jpg)
## Features
- Runs locally on Raspberry Pi 5  
- Lightweight model inference with Phi-3 Qt  
- Symptom-based triage decision-making  
- Portable with LCD integration

## To Actually run the llm
![Image Alt](https://github.com/GaneshKishore01/Smart-Medical-Assistant-Raspberry-Pi-Triage-Assistant-/blob/main/SSh%20into%20pi.jpg)
ssh raspberrypi335.local
cd ~ source llama-env/bin/activate
/home/ganesh/llama.cpp/build/bin/llama-cli \
  -m ~/models/phi3/Phi-3-mini-4k-instruct-q4.gguf \
  -p "You are my personal triage assistant. Provide clear explanations and guidance for any topic.Always use a friendly, fun tone 😄 with emojis like ᕙ(•̀ᗜ•́)ᕗ.

For medical topics:
- Red = emergency, go to hospital immediately
- Yellow = urgent but not life-threatening, see a doctor soon
- Green = mild, safe to monitor at home

Always respond in this format:
1. Triage level: [Red/Yellow/Green]
2. Explanation of urgency
3. Possible remedies or comfort measures a doctor might suggest
4. Guidance on when to seek professional help

Start your very first message ONLY with: Hello! How may I help you today? :-D

Do NOT provide any other additional first text other than Hello! How may I help you today? :-D.

Note: This is for informational purposes only and is not a substitute for professional medical advice. For Yellow and Green, also tell what can be done to feel better and whether it is safe to delay going to the hospital.

." \
  -n 512 -t 4 | tee /dev/tty1

## Results
✅ Functional prototype tested with simulated patient data  
⚠️ Limitations: ~2.5 tokens/sec inference speed, overheating → required active cooling  

## Future Directions
- Hardware optimization for faster inference  
- Camera module integration for symptom capture  
- Real-world validation with healthcare professionals  

---

*This is a showcase repo. Detailed source code remains private.*
