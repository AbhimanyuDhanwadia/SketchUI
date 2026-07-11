# SketchUI

**Author:** [Abhimanyu Dhanwadia](https://github.com/AbhimanyuDhanwadia)  
**Repository:** https://github.com/AbhimanyuDhanwadia/SketchUI  
**License:** Proprietary — All Rights Reserved

---

## Overview

**SketchUI** is an AI-powered desktop application that lets you draw UI wireframes and instantly convert them into functional, styled **Next.js** code using **React** and **shadcn/ui**.

It provides a lightweight "Mini MS-Paint" style canvas built with `customtkinter`. Once you finish sketching a UI layout, the tool analyzes the drawing (via object detection and OCR), constructs a layout JSON, and feeds it to an LLM to generate production-ready frontend code. It can also automatically provision a Next.js project and install the necessary `shadcn/ui` components.

---

## Features

- **Built-in Drawing Canvas:** Intuitive MS-Paint style desktop interface (draw shapes, lines, text).
- **AI Vision Pipeline:** Uses layout detection and OCR to understand the sketched layout and ordering.
- **Code Generation:** Generates responsive React code tailored for Next.js.
- **Shadcn/ui Integration:** Automatically initializes `shadcn/ui` and installs required components (buttons, cards, dialogs, etc.).
- **Local Project Provisioning:** Can bootstrap a fresh Next.js template locally before generating code.

---

## Technology Stack

- **Desktop App:** Python, `customtkinter`, `Pillow`
- **Vision/AI Pipeline:** OCR (`tesseract`), Object Detection, LLM inference API
- **Target Stack (Generated Code):** Next.js, React, Tailwind CSS, `shadcn/ui`

---

For setup and running instructions, please see the [RUNNING.md](./RUNNING.md) guide.
