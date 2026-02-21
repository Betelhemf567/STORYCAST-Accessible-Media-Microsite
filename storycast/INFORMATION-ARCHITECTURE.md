# StoryCast - Information Architecture (IA)

## 📐 SITEMAP

```
┌────────────────────────────────────────────────────────────────┐
│                        StoryCast                                │
│                    (Accessible Media Site)                      │
└────────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
        ▼                     ▼                     ▼
┌───────────────┐    ┌───────────────┐    ┌───────────────┐
│  HOME PAGE    │    │  ABOUT PAGE   │    │  STORY PAGES  │
│  index.html   │    │  about.html   │    │  story/*.html │
└───────────────┘    └───────────────┘    └───────────────┘
        │                     │                     │
        │                     │                     │
    [SECTIONS]           [SECTIONS]          [3 STORY FILES]
        │                     │                     │
        ├─ Hero              ├─ Page Hero          ├─ story1.html
        ├─ Featured          ├─ Mission               "The Voice of Change"
        │  Stories            ├─ Values                (Audio - 25 min)
        ├─ Features          ├─ Accessibility       │
        ├─ CTA               │  Commitment          ├─ story2.html  
        └─ Footer            ├─ Standards             "Beyond the Lens"
                             ├─ Feedback              (Video - 18 min)
                             └─ Footer             │
                                                    └─ story3.html
                                                       "Sounds of Heritage"
                                                       (Audio - 32 min)
```

---

## 🗺️ NAVIGATION STRUCTURE

### Primary Navigation (Global Header)
```
[StoryCast Logo] ────────────────── [Home] [Stories] [About] [Accessibility]
                                       ↓        ↓        ↓          ↓
                                  index.html  #stories about.html #accessibility
```

### User Flows

#### Flow 1: Discover and Listen to a Story
```
Home → Click "Explore Stories" → Stories section → Click story card 
→ Story detail page → Play video/audio → Read transcript
```

#### Flow 2: Learn About Accessibility
```
Home → Click "Accessibility" in nav → About page (#accessibility anchor) 
→ Read features → View standards → Contact for feedback
```

#### Flow 3: Explore Related Stories
```
Story detail page → "Related Stories" section → Click another story card 
→ New story detail page → Play → Explore more
```

---

## 📊 PAGE HIERARCHY

### Level 1: Home (index.html)
- **Purpose:** Introduction, featured content, navigation hub
- **Key Actions:** 
  - Browse featured stories
  - Navigate to story detail pages
  - Learn about platform
  - Access accessibility info

### Level 2A: About (about.html)
- **Purpose:** Mission, values, accessibility commitment
- **Key Actions:**
  - Understand platform mission
  - Learn about values
  - Review accessibility features
  - Contact for feedback

### Level 2B: Story Pages (story/*.html)
- **Purpose:** Consume individual stories with full media
- **Key Actions:**
  - Play video/audio
  - Toggle captions
  - Read transcript
  - Download transcript
  - Explore related stories

**Story Pages:**
1. `story/story1.html` - The Voice of Change
2. `story/story2.html` - Beyond the Lens
3. `story/story3.html` - Sounds of Heritage

---

## 🔗 LINK RELATIONSHIPS

### Internal Links

#### From Home Page:
- **Header:**
  - Logo → `index.html` (self)
  - Home → `index.html` (self)
  - Stories → `#stories` (anchor)
  - About → `about.html`
  - Accessibility → `about.html#accessibility` (anchor)

- **Hero:**
  - "Explore Stories" button → `#stories` (anchor)

- **Story Cards:**
  - Story 1 → `story/story1.html`
  - Story 2 → `story/story2.html`
  - Story 3 → `story/story3.html`

- **CTA:**
  - "Learn More About Us" → `about.html`

- **Footer:**
  - Quick Links → All nav destinations
  - "View Accessibility Statement" → `about.html#accessibility`

#### From Story Pages:
- **Breadcrumb:**
  - Home → `../index.html`
  - Stories → `../index.html#stories`
  - Current story (not linked)

- **Related Stories:**
  - Other 2 stories → `story2.html`, `story3.html` (relative)

- **Footer:**
  - Same as home (with `../` prefix)

#### From About Page:
- **Navigation:** Same as home
- **Internal Anchor:** `#accessibility` section
- **Footer:** Same as home

---

## 🎯 CONTENT STRATEGY

### Home Page Content:
1. **Hero:** Emotional value proposition
2. **Featured Stories:** 3 curated stories with preview
3. **Features:** 4 key accessibility features
4. **CTA:** Join community call-to-action
5. **Footer:** Links, accessibility statement, contact

### Story Page Content:
1. **Hero:** Story title, description, metadata
2. **Media Player:** Video/audio with CC button
3. **Description:** Detailed story context
4. **Transcript:** Full text version
5. **Related:** 2 other stories
6. **Footer:** Navigation

### About Page Content:
1. **Hero:** Mission statement
2. **Mission/What We Do:** Dual column explanation
3. **Values:** 4 core principles
4. **Accessibility:** 8 feature cards
5. **Standards:** Compliance list
6. **Feedback:** Contact information
7. **Footer:** Navigation

---

## 🏗️ COMPONENT ARCHITECTURE

### Shared Components (All Pages):
- **Header** (sticky navigation)
- **Skip Link** (accessibility)
- **Footer** (3-column layout)

### Page-Specific Components:

#### Home:
- Hero Banner
- Story Card (×3)
- Feature Item (×4)
- CTA Banner

#### Story:
- Story Header (dark background)
- Video Player (with CC)
- Audio Player (alternative)
- Transcript Box
- Breadcrumb

#### About:
- Page Hero (gradient)
- Two-Column Content
- Value Card (×4)
- Accessibility Card (×8)
- Standards List
- Contact Box

---

## 📱 RESPONSIVE BEHAVIOR

### Breakpoints:
- **Mobile:** 320px - 639px (1 column)
- **Tablet:** 640px - 1023px (2 columns)
- **Desktop:** 1024px+ (3 columns for cards, 2-3 for content)

### Layout Changes:
- **Navigation:** Full → Hamburger (mobile)
- **Story Grid:** 3 → 2 → 1 columns
- **Features:** 4 → 2 → 1 columns
- **Footer:** 3 → 2 → 1 columns
- **Content Sections:** 2 → 1 columns

---

## ♿ ACCESSIBILITY ARCHITECTURE

### Navigation Aids:
- Skip link (keyboard users)
- Breadcrumbs (orientation)
- Clear focus states (keyboard)
- Logical tab order (sequential)

### Content Structure:
- Semantic HTML (screen readers)
- Heading hierarchy (navigation)
- ARIA labels (clarity)
- Alt text (images)

### Media Access:
- Captions (deaf/HoH users)
- Transcripts (screen readers)
- Audio descriptions (blind users)
- Keyboard controls (motor disabilities)

---

## 📐 VISUAL HIERARCHY

### Typography Scale:
```
H1 (Hero)     → 56px (Desktop) / 36px (Mobile)
H2 (Section)  → 36px (Desktop) / 30px (Mobile)
H3 (Card)     → 20px
Body          → 16px
Small/Meta    → 14px
Label         → 12px
```

### Spacing Scale:
```
Section Gap   → 96px (Desktop) / 64px (Mobile)
Card Gap      → 24px
Element Gap   → 16px
Internal      → 8px / 4px
```

### Color Hierarchy:
```
Primary (Indigo)   → Buttons, links, accents
Secondary (Cyan)   → Secondary actions
Dark (Gray 900)    → Body text
Gray 600/500       → Secondary text
White              → Background
```

---

## 🎨 DESIGN PATTERNS

### Card Pattern:
- Image (16:9 ratio)
- Badge (content type)
- Title (H3)
- Description (2 lines)
- Meta (duration)
- Link (CTA)

### Section Pattern:
- Label (eyebrow)
- Heading (H2)
- Introduction (lead text)
- Content (grid/columns)
- Optional CTA

### Navigation Pattern:
- Logo (left)
- Links (right)
- Active state (color + weight)
- Focus state (outline)
- Mobile (collapse to menu)

---

## 🔍 SEO ARCHITECTURE

### Page Titles:
- Home: "StoryCast - Accessible Media Storytelling"
- Story 1: "The Voice of Change - StoryCast"
- Story 2: "Beyond the Lens - StoryCast"
- Story 3: "Sounds of Heritage - StoryCast"
- About: "About & Accessibility - StoryCast"

### Meta Descriptions:
All pages include descriptive meta descriptions for search engines

### Semantic Structure:
- Proper heading hierarchy
- Descriptive link text
- Structured data ready
- Clean URL structure

---

**Information Architecture Status: COMPLETE** ✅

This IA ensures:
- Clear navigation paths
- Logical content hierarchy
- Accessible structure
- Scalable organization
- Professional standards
