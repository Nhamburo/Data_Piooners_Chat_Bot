# Wendy's & Co. — AI Customer-Service Chatbot

> **Style Made For You.**
> An intelligent, multilingual e-commerce platform with a fully functional AI customer-service assistant named **Bella**.

---

## 📖 Overview

Wendy's & Co. is a premium South African fashion e-commerce website built around an intelligent customer-service chatbot. Unlike a typical "chat widget," **Bella** is the core feature of the platform — she handles product discovery, sizing, order tracking, returns, and human escalation in **11 official South African languages**, with both text and voice support.

The entire application is delivered as a **single, self-contained HTML file** — no build step, no npm install, no backend server required. Open it in a browser and it works.

---

## ✨ Features

### 🛍 E-Commerce Platform
- Responsive product catalogue with 25+ items across 7 categories
- Advanced search, filter (category, size, colour, price, availability), and sort
- Product detail modals with size/colour selection, material info, and stock status
- Shopping cart with quantity management, live totals, and free-delivery threshold
- Simulated checkout flow

### 🔐 User Accounts
- Registration and login system (stored in `localStorage`)
- Role-based access: **Customer** vs **Administrator**
- Personalised account page: profile, orders, support tickets, wishlist
- Session persistence across page reloads

### 🧠 AI Chatbot — Bella *(Core Feature)*
- **Intent detection** across 14 categories (order tracking, returns, sizing, delivery, payments, escalation, etc.)
- **Entity extraction** — recognises order IDs, prices, colours, sizes, and categories from natural language
- **Multi-turn conversation flows**:
  - Product recommendation (asks occasion → budget → size → colour → recommends)
  - Size assistant (asks measurements → recommends size)
  - Order tracking (asks order number → returns status with timeline)
  - Returns & refunds (validates eligibility → starts return process)
  - Human escalation (collects details → creates support ticket)
- **Context memory** across the current session
- **Product cards** rendered directly inside the conversation
- **Order status timeline** with colour-coded stages
- **Personalised greetings** by name and time of day
- **Graceful fallback** — never hallucinates; offers human escalation instead

### 🌍 Multilingual Support
- **11 official South African languages**: English, Afrikaans, isiZulu, isiXhosa, Sesotho, Setswana, Xitsonga, siSwati, Tshivenda, isiNdebele, Sepedi
- Language picker accessible from the chat header
- Intent detection recognises keywords in all supported languages
- **Voice input** — speak to Bella via microphone (Web Speech API)
- **Voice output** — Bella speaks replies aloud (Speech Synthesis API)
- UI phrases (greetings, quick replies, farewells) translated per language

### 👩 Human Escalation & Support
- Recognises escalation triggers in multiple languages
- Collects customer name, email, optional phone, reason, and order number
- Creates simulated support ticket (e.g. `WC-SUPPORT-4821`)
- **Admin dashboard** with live ticket management
- Support metrics: total conversations, AI resolution rate, escalations, average response time, satisfaction

### 🎨 Design & Branding
- Elegant, premium aesthetic inspired by modern fashion brands
- Burgundy `#6E1F2E` primary, cream `#FAF7F2` background, gold `#C6A15B` accents
- Playfair Display (headings) + Inter (body)
- Smooth animations, generous spacing, rounded cards, subtle shadows
- Fully responsive across desktop, tablet, and mobile

### ♿ Accessibility
- Keyboard navigable
- ARIA labels on interactive elements
- High-contrast text
- Focus states preserved
- Mobile-optimised chat interface (full-screen on small devices)

---

## 🚀 Getting Started

### Requirements
- Any modern web browser (Chrome, Edge, Safari, Firefox)
- For **voice features**: Chrome, Edge, or Safari 14.1+ (Web Speech API support)

### Installation

1. Download the `index.html` file
2. Double-click to open it in your browser
3. That's it — no installation, no dependencies, no server

### Optional: Run via Local Server

If you prefer to serve it locally:
```bash
# Python 3
python -m http.server 8000

# Node.js (with npx)
npx serve
