<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,8,30&height=160&section=header&text=⚡%20Bill%20%26%20Rent%20Calculator&fontSize=34&fontColor=fff&animation=twinkling&fontAlignY=35&desc=TNEB+Electricity+%26+Home+Rent+Estimation+Engine&descAlignY=60&descSize=16" width="100%"/>

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Agile](https://img.shields.io/badge/Agile_Team-0052CC?style=flat-square&logo=jira&logoColor=white)
![Cross Browser](https://img.shields.io/badge/Cross--Browser_Tested-4285F4?style=flat-square&logo=googlechrome&logoColor=white)

**Nov 2023 – Dec 2023 · Team Project (3 Members)**

</div>

---

## 📌 Overview

A dual-purpose calculator application that implements **TNEB (Tamil Nadu Electricity Board) domestic slab-rate billing logic** and a **home rent estimation engine** using pure JavaScript. Built by a 3-member Agile team with iterative sprints, cross-browser testing, and real-world billing rules.

> 🎯 Real-World Value: TNEB uses a progressive slab system where different units are billed at different rates. This tool accurately computes bills for any consumption level, saving citizens time and confusion.

---

## ✨ Features

### ⚡ Electricity Bill Calculator
- 📊 **TNEB Domestic Slab-Rate Logic** — Accurate billing across all consumption tiers
- 🧾 **Detailed Bill Breakdown** — Shows units per slab, rate, and sub-total per tier
- 💡 **Fixed Charges** — Includes meter rent and fixed charges as per TNEB norms
- 🔁 **Reset & Recalculate** — Easy re-entry for multiple calculations

### 🏠 Home Rent Calculator
- 📐 **Area-based Estimation** — Calculate rent based on carpet area / built-up area
- 📍 **Location Factor** — Adjust estimates by locality type (urban/semi-urban/rural)
- 🏘️ **Property Type** — Flat, independent house, or PG options
- 📋 **Rent Receipt Summary** — Formatted output for record-keeping

---

## 🏗️ Project Structure

```
bill-rent-calculator/
├── index.html              # Main HTML — tab navigation
├── electricity.html        # Electricity bill calculator page
├── rent.html               # Home rent calculator page
├── style.css               # Shared responsive styling
├── electricity.js          # TNEB slab-rate billing logic
├── rent.js                 # Rent estimation engine
└── README.md
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Semantic forms, tab structure |
| CSS3 | Responsive layout, print-friendly bill view |
| JavaScript | Slab-rate logic, estimation engine, DOM |

---

## ⚡ TNEB Slab Rate Logic

```javascript
// TNEB Domestic Slab Rate (as of 2023)
function calculateElectricityBill(units) {
  let bill = 0;
  const slabs = [
    { limit: 100, rate: 0.00 },   // First 100 units — free
    { limit: 200, rate: 1.50 },   // 101–200 units
    { limit: 500, rate: 3.00 },   // 201–500 units
    { limit: Infinity, rate: 5.00 } // Above 500 units
  ];

  let remaining = units;
  let prev = 0;

  for (const slab of slabs) {
    if (remaining <= 0) break;
    const inThisSlab = Math.min(remaining, slab.limit - prev);
    bill += inThisSlab * slab.rate;
    remaining -= inThisSlab;
    prev = slab.limit;
  }

  const fixedCharge = 30; // Meter rent
  return bill + fixedCharge;
}
```

---

## 🚀 Getting Started

No setup or installation required:

```bash
# Clone the repository
git clone https://github.com/RenugaSuganthi/Bill-Rent-Calculator.git
cd Bill-Rent-Calculator

# Open in browser
open index.html
```

---

## 👥 Team & Agile Process

This was a **3-member team project** following Agile methodology:

| Sprint | Focus |
|---|---|
| Sprint 1 | Requirements gathering, UI wireframe design |
| Sprint 2 | TNEB slab logic implementation + testing |
| Sprint 3 | Rent estimation engine + UI integration |
| Sprint 4 | Cross-browser testing, bug fixes, final review |

**My Contributions:**
- 🎨 UI design — layout, forms, result display
- ⚡ Core TNEB billing logic implementation
- 🔬 Cross-browser compatibility testing (Chrome, Firefox, Edge, Safari)

---

## 🌐 Cross-Browser Compatibility

| Browser | Status |
|---|---|
| Google Chrome | ✅ Tested |
| Mozilla Firefox | ✅ Tested |
| Microsoft Edge | ✅ Tested |
| Safari | ✅ Tested |

---

## 📸 Screenshots

> _Add screenshots here by dragging images into the GitHub editor_

| Electricity Calculator | Bill Result Breakdown | Rent Estimator |
|---|---|---|
| _(screenshot)_ | _(screenshot)_ | _(screenshot)_ |

---

## 🧠 Key Learnings

- Implemented **real-world progressive slab-rate logic** used by a state utility provider
- Collaborated in a **3-member Agile team** with sprint planning and iterative delivery
- Performed **cross-browser compatibility testing** — learned about CSS vendor prefixes and JS quirks
- Managed **UI ownership** end-to-end: from wireframe to final polished output

---

## 👩‍💻 Author

**Renuga K** — Full Stack Developer  
📧 lakshitharenuga@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/renuga-k-a847b828b) · [GitHub](https://github.com/RenugaSuganthi)

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,8,30&height=100&section=footer&animation=twinkling" width="100%"/>
