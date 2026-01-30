# Implementation Plan - Stemon Design Reproduction

The goal is to inject the "Stemon" (STEM education) design essence into a Bootstrap-based HTML structure.
Since the target workspace `d:/antigravity/minicity` appears to operate in a fresh state (directory not found), I will create a **demonstration file** `stemon_demo.html` that embodies the requested design on a standard Bootstrap skeleton.

## User Review Required
> [!WARNING]
> I could not locate the "currently edited HTML code" in `d:\antigravity\minicity`.
> **Action**: I will create `stemon_demo.html` from scratch with a Bootstrap structure to demonstrate the design. You can copy the `<style>` block and structure into your actual file later.

## Design Tokens (Extracted from Stemon.net)

### 1. Colors & Atmosphere
*   **Primary Key (Energy)**: `#EA8000` (Vibrant Orange) - Used for CV buttons, "Point" indices, strong highlights.
*   **Secondary Key (Trust)**: `#0070BB` (Intellectual Blue) - Used for accents, logos, trust markers.
*   **Backgrounds**: White `#FFFFFF` contrasted with Light Gray `#F9F9F9` or Pale Orange `#FFF8F0` for section distinctness.

### 2. Shapes & UI "Softness"
*   **Corner Radius**:
    *   Buttons: `50px` (Pill shape) - User friendly.
    *   Cards/Images: `15px` - `20px` (Soft rects) - Safe for children context.
*   **Shadows**: Soft, diffuse shadows `0 4px 15px rgba(...)` to make elements pop gently (Paper-like material).

### 3. Typography
*   **Font**: `Noto Sans JP` (Google Fonts)
*   **Hierarchy**:
    *   Headings: Bold, high contrast.
    *   Body: Readable, comfortable spacing.
    *   English Subtitles: Small, tracking-wide, decorative (e.g., "REASON 01").

### 4. Layout & "Movement"
*   **Section Dividers**: Slanted lines or subtle curves (via CSS `clip-path` or borders) to avoid blocky look.
*   **Spacing**: Generous padding (`py-5` equivalent).

## Proposed Changes

### [New File] `stemon_demo.html`
Will contain:
1.  **Header**: White with Logo (Text based for now) + "Free Trial" Orange Button.
2.  **Hero**: Dynamic, with "Future Learning" catchphrase.
3.  **Features (3 Reasons)**:
    *   Index `01`, `02`, `03` in Orange.
    *   Cards with soft corners and icons.
4.  **Floating/Sticky CV Button**: Mimicking the "Always accessible" conversion point.

## Verification Plan
1.  **Manual Check**: Open `stemon_demo.html` in browser (or ask user to).
2.  **Visual Verify**: Check against `stemon.net` screenshot for color accuracy and "vibe".
