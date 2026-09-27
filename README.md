# MicroEye — Sub-Millimeter AI Vision Inspection

**A plug-in camera + AI module that catches 0.1–0.3mm solder cracks at full line speed — defects no human inspector can reliably catch.**

Built for the **GITAM Innovation Challenge 2026** by team **Mind Matrix**.

---

## 🎯 The Problem

Manual and semi-automated inspection on PCB assembly lines (running 3,000–6,000 units/hour) catches only large defects. Sub-millimeter solder cracks — 0.1 to 0.3mm — are invisible to the human eye and surface later as field failures and warranty claims. Traditional AOI (Automated Optical Inspection) machines can catch these, but cost lakhs of rupees — out of reach for small and mid-size manufacturers.

## 💡 The Solution

MicroEye is a **retrofit vision layer** that scans every board in real time, without replacing existing lines:

1. **Camera** — mounted above the line
2. **YOLO** — custom-trained vision model detects cracks, cold joints, misalignment, bridging
3. **Defect classification** — flags the specific defect type
4. **Route** — auto-routes defective boards to a reject bin
5. **Log** — timestamped image + defect class logged to a dashboard

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Vision model | YOLOv8 (transfer-learned) |
| Image processing | OpenCV |
| Inference hardware | Jetson-class edge inference box |
| Camera | Industrial camera |
| Dashboard | Web dashboard (defect logs, confidence scores) |

## 📊 Market

- **TAM:** India's EMS/PCB assembly market — multi-billion-dollar, growing under the PLI push for electronics manufacturing
- **SAM:** Small/mid-size PCB assemblers who need sub-mm defect coverage but can't afford lakhs-worth AOI machines
- **SOM:** First cohort of regional EMS units, priced as an affordable add-on module

## 🏆 Competitive Positioning

| Approach | Trade-off |
|---|---|
| Large AOI machine vendors | Accurate, but priced in lakhs, built for big factories |
| Manual visual inspection | Cheap, but can't catch 0.1–0.3mm defects at line speed |
| **MicroEye (us)** | AOI-grade sub-mm detection, priced for manufacturers shut out of traditional AOI |

## 💰 Business Model

**Hardware-as-a-Service** — one-time camera install + monthly subscription for detection, dashboard, and updates.

**Roadmap:**
- **v1 (hackathon):** Single-defect-class detection
- **v2:** Multi-class taxonomy, higher-resolution imaging
- **v3:** On-device continual learning
- **Future:** ResonX — acoustic-resonance sensing for hidden/internal defects beyond vision

## ✅ Current Status

- YOLOv8 trained and tested on a sample solder-defect image set, running **live inference**
- Validated: the model reliably flags sub-mm defects difficult to catch by eye, on a repeatable test set

**Next steps:**
- Expand dataset with real manufacturer samples
- Move inference to an edge device
- Run a pilot with a local EMS unit

## 👥 Team — Mind Matrix

| Role | Name | College | Program |
|---|---|---|---|
| Lead | Eranki Giridhar Goud | Sphoorthy Engineering College | AIML 2nd Year |
| Co-Lead | Madharapu Charan Tej | Sphoorthy Engineering College | AIML 2nd Year |

> "Defect detection shouldn't be priced out of reach for small manufacturers."

---

*Submitted to the GITAM Innovation Challenge 2026.*
