# 🚀 WordPress & Elementor Pro Implementation Guide
**Project:** Wellness Pro — 3 New Pages Implementation  
**Base Site:** [wellnesspro.in](https://wellnesspro.in/)  
**Theme:** Hello Elementor  
**Page Builder:** Elementor Pro  

---

## 📌 Page URLs & Architecture

| Page Title | Target Slug / Permalinks | Google Drive Asset Source |
|------------|--------------------------|---------------------------|
| **Our Technology & Machinery** | `/our-technology/` | `Drive Folder 1 (Machine videos)` |
| **Center Openings & Launches** | `/center-openings/` | `Drive Folder 2 (Openings videos)` |
| **Patient Stories & Reviews** | `/patient-stories/` | `Drive Folder 3 (patients videos)` |

---

## 🛠️ Step-by-Step Implementation Instructions

### 1. Global Brand Styling Tokens (Hello Elementor & Kit 6)
- **Headings Font:** `Montserrat` (600, 700)
- **Body & Menu Font:** `Open Sans` (400, 500)
- **Primary Navy:** `#20265B` (`--e-global-color-05d1900`)
- **Royal Navy:** `#0F256C` (`--e-global-color-871e09b`)
- **Active Accent Coral:** `#FE6347` (`--e-global-color-3565630`)
- **Topbar Background:** `#F1F5FF`
- **Buttons:** 100px Pill radius (`border-radius: 100px;`)

---

### 2. Asset Preparation & Media Management
1. **Video Hosting Strategy:**
   - For fast page loading and SEO score preservation (Core Web Vitals), compress videos to WebM / MP4 (H.264) or host on YouTube (Unlisted) / Vimeo / BunnyCDN.
   - Use poster images (WebP format, under 150KB) as video covers so the initial page loads instantly.
2. **Image Optimization:**
   - Convert WhatsApp JPEG images to WebP with 80% quality.
   - Resize hero and banner images to max 1920px width.
   - Resize card and gallery images to max 800px width.

---

### 2. Elementor Pro Container Layout Setup

#### Page 1: `/our-technology/`
* **Section 1: Hero Container**
  - Direction: Row / Column (Mobile)
  - Background: Gradient `#001d35` to `#093259`
  - Elements: Heading, Subheading, Call to Action button.
* **Section 2: 3 Core Technology Cards (Container Grid)**
  - Columns: 3 equal width flex containers.
  - Card 1: 3D Scanner (FootBalance)
  - Card 2: 10-Min Thermal Molding Station
  - Card 3: Kineon Move+ Laser Joint Therapy
* **Section 3: Video Showcase (Elementor Video / Media Carousel)**
  - Insert Elementor Video widgets with lightbox popups enabled.
* **Section 4: 4-Step Journey (Timeline / 4 Columns)**
  - Numbered cards: 01 Scan → 02 Biomechanics → 03 Custom Molding → 04 Instant Relief.
* **Section 5: Appointment CTA**

---

#### Page 2: `/center-openings/`
* **Section 1: Expansion Hero Banner**
* **Section 2: Metrics Counter (Elementor Counter Widget)**
  - 4+ Cities Launched, 65+ Event Assets, 10k+ Scans, 100% Certified.
* **Section 3: Nested Tabs or Filterable Gallery (Elementor Nested Tabs)**
  - Tab 1: **Gambol Store, Ahmedabad** (21 photos & videos)
  - Tab 2: **Gwalior Clinic** (21 photos & videos)
  - Tab 3: **Jabalpur Experience Center** (15 photos & videos)
  - Tab 4: **Lokhandwala, Mumbai Flagship** (8 photos & videos)
* **Section 4: Franchise CTA Container**
  - Linking directly to existing `/franchisee-partner/` URL.

---

#### Page 3: `/patient-stories/`
* **Section 1: Hero Banner & Trust Badges**
  - Rating badge: 4.9★ from 10,000+ happy feet.
* **Section 2: Filterable Video Grid (Elementor Loop Grid / Filter Tabs)**
  - Filter by condition: Plantar Fasciitis, Sports/Athletes, Post-Surgery Rehab, Posture/Back Pain.
  - Video play overlay + direct patient quote + city badge.
* **Section 3: Clinical Proof Stats**
  - 98% pain reduction, 100% custom molded.
* **Section 4: Consultation Booking Form Widget**
  - Elementor Pro Form connecting to email notification and WhatsApp API redirection (`https://wa.me/919820647062`).

---

### 3. Updating the WordPress Menu Navigation

In `WordPress Admin` → `Appearance` → `Menus` (or via Elementor Header Builder #200):
1. Under **Main Menu**, add:
   - **Technology** (`/our-technology/`)
   - **Openings** (`/center-openings/`)
   - **Patient Stories** (`/patient-stories/`)
2. Or group them cleanly under a new dropdown menu titled **"Experience"** or **"Discover"**:
   - Discover
     - ├─ Our Technology & Machines
     - ├─ Center Openings & Expansion
     - └─ Patient Stories & Testimonials

---

### 4. Testing & Verification Checklist
- [ ] Mobile responsive check on iOS & Android devices.
- [ ] Video playback lightbox popups functioning without layout shift.
- [ ] Phone call links (`tel:9820647062`) and WhatsApp buttons tested.
- [ ] Page speed test on Google PageSpeed Insights (aiming for 90+ performance score).
