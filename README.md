# ⛈️ The BZPro "Franklin" Weather Boy Edition
**A Decentralized, High-Precision Meteorological Mesh Network**

## 🚧 Status: **WORK IN PROGRESS**
*This project is currently in the active prototyping and hardware debugging phase. Documentation is updated live as the "V1.0" prototype is not fully built yet.*
*Also note that all of the data is from South Bend, Indiana weather so if you live in Wisconsin, California, Colorado etc. then your weather and data will possible be significantly different than my data*

---

## 🌦️ The Mission
Corporate weather apps are the "consoles" of meteorology—locked, subscription-based, and inaccurate. **The BZPro** is a one-and-done purchase that offers:
* **Hyper-Local Reality:** Outperforming airport-based reports with backyard-specific data.
* **Total Sovereignty:** No ads, no paywalls, and 100% data ownership.
* **Contractor-Grade Alerts:** Integrated with IFTTT for phone call/SMS storm warnings.

---

## 🛠️ Hardware Stack (The "PC" Components)

### Base Station (The Server)
* **Raspberry Pi 4 (4GB):** Running Home Assistant & MQTT.
* **Cloudflare Tunnels:** Secure Zero-Trust remote access.

### Node: "Franklin" (The Main Node)
* **MCU:** ESP32-S3 Thing Plus.
* **Radio:** nRF24L01+PA+LNA (2.4GHz) with 100uF stability capacitors.
* **Sensing:** BME280 (Atmos), AS3935 (Lightning), INMP441 (Acoustic Thunder).
* **Power:** 6V 5Ah Miady Lead-Acid Battery + 6V 4.5W Solar + Acixo PWM Controller.
* **UI:** 4-LED Diagnostic Dashboard (Blue, Orange, Yellow, Red-Blink).

### Node: "Artemis" (The Garden Node)
* **MCU:** SparkFun Artemis Thing Plus (Ultra-low power).
* **Sensing:** Qwiic Soil Moisture + Remote Temperature.
* **Security:** ATECC508A Cryptographic Co-processor (Hardware-backed ID).

---

## 🗺️ Project Roadmap

### Phase 1: Prototype (V1.0)
- [ ] Establish Encrypted Handshake between Artemis & Franklin.
- [ ] Calibrate "South Bend Accuracy" vs. Airport ASOS data.
- [ ] Implement "About To" 5.9V slow-blink power-off logic.

### Phase 2: Professional Hardening (V2.0)
- [ ] Transition to high-efficiency Buck Converters.
- [ ] Integrate IFTTT Webhooks for emergency phone call alerts.
- [ ] Add E-Paper (E-Ink) internal temp monitoring.

### Phase 3: The Community Mesh (V3.0+)
- [ ] Deploy multiple nodes for Lightning Triangulation (ToA Math).
- [ ] Launch an ad-free, community-driven live weather map.
- [ ] Open-source custom PCB designs (KiCad).

---

## 🔐 Security & Privacy
* **Hardware Auth:** ATECC508A ensures only genuine BZPro nodes can join the mesh.
* **Encryption:** AES-128 bit software encryption on all radio packets.
* **Zero Trackers:** No third-party data selling. Your data stays on your Pi.

## 🤝 Community & Support
* **Discussions:** Use the GitHub Discussions tab for "How-to" and build showcases.
* **Issues:** Report hardware bugs or sensor failures here.
* **Manual:** See `/docs` for assembly and the "Franklin" wiring guide.

**License:** MIT License — Build it. Own it. Expand it.
