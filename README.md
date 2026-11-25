# QR Forge — QR Code Creator

A fast, client-side QR code generator for creating customizable, high-resolution QR codes with real-time live preview and instant PNG/PDF export.

## Features

- **Destination URL**: Enter any link and see the QR code update instantaneously.
- **Custom Colors**: Independently customize Foreground, Background, Finder Border, and Finder Dot colors.
- **Design Styles**:
  - **Patterns**: Square, Dots, Rounded, Extra Rounded, Classy, Classy Rounded
  - **Corner Squares**: Square, Dot, Extra Rounded
- **Center Logo**: Upload a custom image logo placed cleanly in the center with high error correction (`H`).
- **Frames & Call-to-Action**: Choose from No Frame, Bottom Text, Top Text, or Speech Bubble frames with customizable CTA text and frame color.
- **High-Quality Export**: Download your styled QR code (including frame and CTA) as a high-resolution **PNG** or **PDF**.
- **One-Click Reset**: Quickly clear all customizations and start fresh from the live preview panel.

## Tech Stack

- **Framework**: React 19 + TypeScript + Vite
- **Styling**: Tailwind CSS v4
- **QR Engine**: `qr-code-styling`
- **Export**: `html2canvas` & `jspdf`
- **Animations & Icons**: `motion` & `lucide-react`

## Getting Started

### Prerequisites

- Node.js (v18 or higher recommended)
- npm

### Installation

```bash
npm install
```

### Run Locally

```bash
npm run dev
```

The development server runs at `http://localhost:3000`.

### Build for Production

```bash
npm run build
```

The production bundle is output to the `dist/` directory.

### Type Check

```bash
npm run lint
```

## Project Structure

```text
├── index.html
├── package.json
├── vite.config.ts
└── src/
    ├── App.tsx                       # Main layout, state management, and reset controls
    ├── types.ts                      # TypeScript types for QR configuration
    ├── lib/
    │   └── utils.ts                  # Utility helpers
    └── components/
        ├── SidebarControls.tsx       # Customization controls sidebar
        └── QRCodePreview.tsx         # Live QR canvas preview, frames, and PNG/PDF export
```

## Deployment

Because QR generation, styling, and PNG/PDF exporting happen entirely in the browser, you can deploy the built `dist/` folder to any static hosting provider such as **GitHub Pages**, **Netlify**, or **Vercel**.
