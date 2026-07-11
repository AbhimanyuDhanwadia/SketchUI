# ▶️ Running Guide — SketchUI

> Complete step-by-step guide to get SketchUI running locally.

---

## Prerequisites

| Requirement | Version | Check |
|---|---|---|
| Python | 3.10+ | `python --version` |
| pip | latest | `pip --version` |
| Node.js / npm | latest | `npm -v` |
| Tesseract OCR | any | `tesseract --version` |

> **Node.js** is required because the tool automatically provisions a Next.js frontend using `npx degit` and `npm install`.

---

## 1. Clone & Enter the Repo

```bash
git clone https://github.com/AbhimanyuDhanwadia/SketchUI.git
cd SketchUI
```

---

## 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate        # macOS / Linux
# venv\Scripts\activate         # Windows
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> **Note:** The layout pipeline also requires `apiinference`, `inference`, and `tesseract_infer` modules to be accessible in your environment or present in the repository root.

---

## 4. Run the Application

You can launch the desktop canvas directly:

```bash
python generate_png.py
```

### Initializing the Next.js Workspace
If you want the application to automatically bootstrap the target Next.js repository (cloning a template, installing dependencies like `@mantine/core`, `nextui-org`, `shadcn/ui`, etc.), start the application with the `--fresh` flag:

```bash
python generate_png.py --fresh
```

This creates a `websiteTemp` folder and prepares all aliases and dependencies before opening the canvas.

---

## 5. Workflow Instructions

1. Select **File** in the toolbar to switch between multiple sketches (e.g., `landing.png`).
2. Use the **Tools** (Brush, Eraser, Text, Line, Rectangle, Ellipse) to draw your desired UI.
3. Once satisfied, click **📸 Save PNG**.
4. The system will save the image to `./images/`, run OCR and element detection to build a `layout_output.json`.
5. It will then pass the layout to the LLM to generate the React component and write it to `websiteTemp/app/[filename]/page.tsx`.
