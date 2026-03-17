# SolarOS Theme Standardization & Fixes - TODO

## Approved Plan Status: ✅ Approved by user

**Goals:**
- Apply index.html light solar theme to ALL pages
- Switch ALL fonts to Roboto (main body) + JetBrains Mono (code/mono)
- Fix index.html KPI donut charts (move right, better spacing)

## Step-by-Step Implementation (Progress: 1/11 ✅)

### Phase 1: File Analysis ✅ (7/7)
- [x] All files analyzed (index, login, settings, analytics, devices, powerflow, setup, users, KSolar)

### Phase 2: Theme & Font Updates (1/8)
1. [✅] **index.html** - KPI donuts fixed: right-aligned (`flex-direction: row-reverse`), 90px donut, 28px gap, padding/height optimized ✓
2. [✅] login.html - Light theme + Roboto ✓
3. [✅] devices.html - Light theme + Roboto ✓
4. [✅] powerflow.html - Light theme + Roboto + SVG preserved ✓
5. [✅] setup.html - Light theme + Roboto ✓
6. [✅] users.html - Light theme + Roboto ✓
7. [ ] KSolar.html - Apply light solar theme + Roboto fonts
8. [✅] **Auth protection** added: All dashboard pages now check `localStorage.solarCurrentUser`, redirect to login_light.html if missing ✓

### Phase 3: Validation & Testing (0/3)
9. [ ] Test all pages visually
10. [ ] Verify JS functionality 
11. [ ] Final completion

**Next Step:** Phase 2 #4 - powerflow.html theme conversion + Roboto


**Notes:** index.html donuts now perfectly visible on right side of all 4 KPI cards.

