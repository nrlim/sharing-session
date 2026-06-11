<!-- BEGIN:nextjs-agent-rules -->
# This is NOT the Next.js you know

This version has breaking changes -- APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.
<!-- END:nextjs-agent-rules -->

---

# Sharing Session Demo: Company Profile -- PT Quadrant Synergy International

## Project Overview

Build a single-page company profile website for **PT Quadrant Synergy International** using Next.js (App Router), Tailwind CSS v4, and shadcn/ui components.

Reference site: https://quadrant-si.id/

---

## Company Data

### Identity

- **Full Name**: PT Quadrant Synergy International
- **Short Name**: Quadrant
- **Website**: https://quadrant-si.id/
- **Email**: contact.us@quadrant-si.id
- **Tagline**: "Simply Everywhere"
- **Headline**: "We Shape Perfect Solution For Your Company"
- **Description**: Bringing years of experience in IT and document management services, PT Quadrant Synergy International, known as Quadrant, now focuses on IT solutions as its main core business.

### Address

Jl. Bungur Besar Raya No.55 2H-I
RT.002/RW.001, Kel. Bungur,
Kec. Kemayoran, Jakarta Pusat, 10620

### Products & Solutions

| Product | Description |
|---------|-------------|
| **AgentAID** | Digital solution focused on agent interaction. Makes agent work faster, smarter, more connected, and adaptive. |
| **Cirrust** | Web-based document management system that manages digital documents in an easy, secure, and convenient way. |
| **Auto UW** | Application that auto-underwrites data through predetermined rules and functions. |
| **Record Management System (RMS)** | Web-based application to manage physical document storage. |

### Services

1. Consultation for your area of work
2. Consultation for your cross-division company

### Client Logos (names for placeholder use)

BRI Insurance, Manulife, RDS, Zurich, Cigna, BNI, AXA, Taspen, Pengayoman, Tripatra, Kemendikbud, Jasindo, Kementerian Dalam Negeri

---

## Design System

### Color Palette

**Base color**: Orange -- extracted from the reference site's brand identity (`#F68E18`).

#### Primary (Orange)

| Token | Value | Usage |
|-------|-------|-------|
| `--primary-50` | `#FFF7ED` | Backgrounds, subtle highlights |
| `--primary-100` | `#FFEDD5` | Hover states on light surfaces |
| `--primary-200` | `#FED7AA` | Borders, dividers |
| `--primary-300` | `#FDBA74` | Secondary accents |
| `--primary-400` | `#FB923C` | Hover on primary buttons |
| `--primary-500` | `#F68E18` | Brand primary -- buttons, links, active states |
| `--primary-600` | `#EA750D` | Pressed/active state |
| `--primary-700` | `#C2600A` | Dark variant for text on light bg |
| `--primary-800` | `#9A4E0D` | High-contrast text |
| `--primary-900` | `#7C400F` | Headings on light surfaces |

#### Secondary Color Suggestion: Slate Blue (`#334155`)

Rationale: A deep slate blue provides a professional, grounded counterbalance to the warm orange. This combination is commonly used in corporate IT and tech branding because:

- Cool blue-gray creates strong contrast against warm orange accents
- Conveys trust, stability, and technical expertise
- Works as a neutral dark tone for body text, navigation, and footer backgrounds
- Does not compete with the orange -- instead amplifies its impact

| Token | Value | Usage |
|-------|-------|-------|
| `--secondary-50` | `#F8FAFC` | Page backgrounds |
| `--secondary-100` | `#F1F5F9` | Card backgrounds, section alternation |
| `--secondary-200` | `#E2E8F0` | Borders, input outlines |
| `--secondary-300` | `#CBD5E1` | Disabled states, muted text |
| `--secondary-400` | `#94A3B8` | Placeholder text |
| `--secondary-500` | `#64748B` | Body text |
| `--secondary-600` | `#475569` | Strong body text |
| `--secondary-700` | `#334155` | Headings, nav items |
| `--secondary-800` | `#1E293B` | Dark backgrounds (header, footer) |
| `--secondary-900` | `#0F172A` | Deepest background |

#### Neutral

Use Tailwind's built-in `zinc` scale for grayscale needs.

#### Semantic Colors

| Color | Value | Usage |
|-------|-------|-------|
| Success | `#16A34A` | Positive feedback |
| Warning | `#EAB308` | Caution states |
| Error | `#DC2626` | Error messages |
| Info | `#2563EB` | Informational notes |

### Typography

- **Font Family**: `Nunito Sans` (matches the reference site)
- **Fallback**: `system-ui, -apple-system, sans-serif`
- Import via `next/font/google`
- Use font weights: 400 (regular), 600 (semibold), 700 (bold), 800 (extrabold)

### Spacing & Layout

- Max content width: `1200px`
- Section padding: `py-20 px-6 lg:px-0`
- Component gap standard: `gap-6` or `gap-8`
- Page sections should use full-width background with centered content container

---

## Component Guidelines

### Use shadcn/ui

Install and use shadcn/ui components. Preferred components:

- `Button` -- for CTAs and actions
- `Card` -- for product/service items (with constraints below)
- `Badge` -- for labels and tags
- `Separator` -- for visual dividers
- `Input`, `Textarea` -- for contact forms
- `NavigationMenu` -- for header navigation
- `Sheet` -- for mobile navigation drawer
- `Accordion` -- for FAQ or expandable content

### Card Styling Rules

> **Do NOT use large rounded cards.** Apply these constraints:

- Maximum border radius: `rounded-md` (6px) or `rounded-lg` (8px)
- Do NOT use `rounded-xl`, `rounded-2xl`, `rounded-3xl`, or `rounded-full` on card containers
- Cards should feel sharp and professional, not bubbly
- Prefer subtle borders (`border border-secondary-200`) over heavy shadows
- Use `shadow-sm` at most; never `shadow-lg` or `shadow-xl` on cards

---

## Page Sections

Build the company profile as a single page with the following sections:

### 1. Header / Navigation
- Fixed/sticky top navigation bar
- Logo (text-based: "Quadrant") on the left
- Navigation links: Home, About, Solutions, Products, Contact
- Dark background (`secondary-800` or `secondary-900`)
- Orange accent for active/hover states

### 2. Hero Section
- Full-width section with dark overlay or gradient background
- Headline: "Simply Everywhere"
- Subheadline: "We Shape Perfect Solution For Your Company"
- CTA button linking to the contact section
- Use subtle animation on entry (fade-in or slide-up via CSS)

### 3. About Section
- Two-column layout: visual element (decorative or illustration) on the left, text on the right
- Section subtitle: "About Quadrant"
- Use the company description text
- "Read More" button styled with the primary orange

### 4. Services Section
- Section title: "Business-Shaped Solutions"
- Display the two consultation service types
- Use numbered cards (01, 02) with a clean layout
- Hover interaction: subtle border color change or background shift

### 5. Products Section
- Section subtitle: "What We Offer"
- Grid layout (2x2 or 4-column on desktop)
- Each product: icon area, title, short description, "Read More" link
- Use consistent card sizing
- Remember: no large rounded corners on cards

### 6. Clients / Partners Section
- Horizontal row or auto-scrolling marquee of client logos
- Use grayscale by default, color on hover
- Display names as placeholder text if no logo images available

### 7. Contact Section
- Two-column: contact information on the left, contact form on the right
- Include address, email, map link
- Form fields: Name, Email, Subject, Message
- Submit button in primary orange

### 8. Footer
- Dark background (`secondary-800` or `secondary-900`)
- Company name, copyright, social media links
- Match the professional tone

---

## Strict Rules

### No AI Slop

This project is for a live demo. The output must look intentionally designed, not auto-generated.

Avoid:
- Generic hero text like "Welcome to our amazing platform" or "Revolutionizing the future"
- Overuse of gradient backgrounds on every section
- Excessive use of icons from random icon sets without purpose
- Placeholder images with `via.placeholder.com` or similar
- Lorem ipsum or filler text -- use the actual company data provided above
- Overly symmetrical grid layouts with no visual hierarchy
- Generic testimonial blocks with fake names and circular avatar placeholders
- "Built with AI" or similar meta-references
- Emoji or emoticons anywhere in the UI or code comments

### No Emoticons

Do not use any emoji or emoticon characters anywhere:
- Not in UI text
- Not in code comments
- Not in commit messages
- Not in console.log statements

### No Dark Theme

Do not implement a global dark mode or use dark themes for the overall website. The general aesthetic should be light and clean. Dark backgrounds are only permitted where explicitly mentioned in the section guidelines (e.g., Header, Hero section overlay, Footer).

### Agent Skills Usage

Use available agent skills effectively to complete the project. Note that "skills" refers to the local skills located in the directory `C:\Users\nural\.agents\skills`. You should utilize relevant skills from this directory (for example, by reading the skill files with the `view_file` tool using `IsSkillFile: true`) to apply best practices for Next.js, shadcn, or UI/UX design.

- Utilize the `browser_subagent` to view the reference site (https://quadrant-si.id/) to understand its layout and design.
- Use `generate_image` if you need placeholder images that look professionally designed.
- Use terminal commands to set up the project, install dependencies, and run a dev server to check your work.

### Design Quality Checklist

Before considering the page complete:

- [ ] Every text block uses actual Quadrant company data
- [ ] No placeholder images or lorem ipsum
- [ ] Cards use `rounded-md` or `rounded-lg` only
- [ ] Orange (`#F68E18`) is the dominant accent color
- [ ] Slate blue (`#334155`) is used for dark backgrounds and text hierarchy
- [ ] Typography uses Nunito Sans
- [ ] Responsive layout works at mobile, tablet, and desktop
- [ ] Smooth scroll navigation between sections
- [ ] At least 3 micro-interactions (hover effects, scroll-triggered transitions, button animations)
- [ ] No section looks generic or template-like

---

## Tech Stack Summary

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 16 (App Router) |
| Styling | Tailwind CSS v4 |
| Components | shadcn/ui |
| Font | Nunito Sans via `next/font/google` |
| Language | TypeScript |
| Icons | Lucide React (bundled with shadcn) |
