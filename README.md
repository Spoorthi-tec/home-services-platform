# HomeEase – Home Services Platform

A responsive home services booking platform built with **React.js, TypeScript, HTML and CSS**.

## Features

- **Service catalogue** with category chips, sort options (recommended, top rated, price) and a live result count.
- **Search** across service names, descriptions, categories and keywords (multi-word, debounced).
- **Booking flow** in an accessible modal: name, phone, email, address, date, time slot and optional notes.
- **Client-side form validation** with inline errors on blur, a full check on submit, focus moved to the first invalid field, date range limits and a notes counter.
- **My bookings** panel with two-step cancellation; bookings persist in `localStorage`.
- **Reusable UI components** (`Button`, `Modal`, `Field`, `ServiceCard`, …), custom hooks and typed data models.
- **Responsive** layout (mobile bottom-sheet modal), keyboard accessible, focus trapped in dialogs, reduced-motion friendly.

## Getting started

```bash
npm install
npm run dev        # start the dev server
npm run build      # type-check and create a production build in dist/
npm run preview    # preview the production build
```

## Project structure

```
src/
├── components/   Reusable UI (Button, Modal, Field, SearchBar, ServiceCard, BookingModal, …)
├── data/         Service catalogue and time slots
├── hooks/        useBookings (localStorage), useDebounce
├── types/        Shared TypeScript interfaces
├── utils/        Validation rules and formatting helpers
├── App.tsx       Page composition, search / filter / sort state
├── main.tsx      Entry point
└── styles.css    Design tokens and styles
```

## Git & GitHub

```bash
git init
git add .
git commit -m "feat: initial home services booking platform"
git branch -M main
git remote add origin https://github.com/<your-username>/home-services-platform.git
git push -u origin main
```

## Customising

- Add or edit services in `src/data/services.ts`.
- Change validation rules in `src/utils/validation.ts`.
- Swap the colour palette via the CSS variables at the top of `src/styles.css`.
- To connect a real backend, replace `addBooking` / `cancelBooking` in `src/hooks/useBookings.ts` with API calls.
