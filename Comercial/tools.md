---
name: Tools Master
description: Manages the tools and templates for the Cafo commercial team. Focuses on providing HTML/CSS snippets that align with the Cafo design system for use in emails, playbooks, and proposals.
color: "#475569"
emoji: 🧰
vibe: Equips the team with beautiful, functional assets.
---

# Commercial Tools & Templates

This document outlines the tools and design assets available to the commercial team for constructing playbooks, proposals, and outreach materials.

## Cafo Design System - Commercial Assets

All commercial materials must align with the Cafo brand. Below are reusable HTML/CSS snippets for playbook generation.

### Color Palette
- **Primary:** `#E8590C` (Cafo Orange) - Used for emphasis, calls to action, and primary headers.
- **Background (Light):** `#FAFAF9` (Off-white) - Used for callout boxes and secondary areas.
- **Background (Highlight):** `#FFF7ED` (Light Orange) - Used for critical next steps or closing sections.
- **Text (Primary):** `#1C1917` (Dark Stone) - Used for body copy.
- **Text (Secondary):** `#78716C` (Medium Stone) - Used for metadata or subtle info.

### Typography
- Primary Font: `Satoshi` (or modern sans-serif fallback like `Inter` or `sans-serif`).

### Playbook HTML Component Toolkit

Use these components to build playbooks.

#### 1. Standard Playbook Container
```html
<div style="font-family: 'Satoshi', sans-serif; max-width: 800px; margin: 0 auto; color: #1C1917; line-height: 1.6;">
  <!-- Playbook content goes here -->
</div>
```

#### 2. Main Header
```html
<div style="border-bottom: 3px solid #E8590C; padding-bottom: 20px; margin-bottom: 30px;">
  <h1 style="color: #E8590C; margin-bottom: 5px; font-size: 24px;">☕ Cafo Playbook: [Title]</h1>
  <p style="color: #78716C; font-size: 14px; margin-top: 0;">
    <strong>Target:</strong> [Persona] | <strong>Objective:</strong> [Goal] | <strong>Date:</strong> [YYYY-MM-DD]
  </p>
</div>
```

#### 3. Section Divider
```html
<h2 style="color: #E8590C; border-bottom: 1px solid #E5E5E5; padding-bottom: 10px; margin-top: 30px; font-size: 20px;">[Icon] [Section Title]</h2>
```

#### 4. Context/Scenario Box
```html
<div style="background-color: #FAFAF9; padding: 20px; border-radius: 8px; margin-bottom: 30px; border-left: 4px solid #E8590C;">
  <h3 style="margin-top: 0; color: #1C1917; font-size: 18px;">🎯 Quando usar este Playbook?</h3>
  <p style="margin-bottom: 0;">[Context Text]</p>
</div>
```

#### 5. The Pitch Callout
```html
<div style="padding: 15px; font-size: 1.1em; font-style: italic; background-color: #fff; border: 1px dashed #ccc; border-radius: 4px; margin-bottom: 20px;">
  "[The Pitch text goes here]"
</div>
```

#### 6. Discovery Questions List
```html
<ul style="list-style-type: none; padding-left: 0; margin-bottom: 30px;">
  <li style="margin-bottom: 15px; padding-left: 20px; position: relative;">
    <span style="position: absolute; left: 0; top: 0; color: #E8590C;"><strong>Q:</strong></span>
    "[Question Text]"
  </li>
</ul>
```

#### 7. Objection Handling Table
```html
<table style="width: 100%; border-collapse: collapse; margin-bottom: 30px; font-size: 15px;">
  <thead>
    <tr style="background-color: #FAFAF9; border-bottom: 2px solid #E8590C;">
      <th style="padding: 12px; text-align: left; width: 30%;">Objeção (O que dizem)</th>
      <th style="padding: 12px; text-align: left; width: 30%;">Motivo Real (O que significa)</th>
      <th style="padding: 12px; text-align: left; width: 40%;">Reframe (Como responder)</th>
    </tr>
  </thead>
  <tbody>
    <tr style="border-bottom: 1px solid #E5E5E5;">
      <td style="padding: 12px; vertical-align: top;">"[Objection]"</td>
      <td style="padding: 12px; vertical-align: top;">[Real meaning]</td>
      <td style="padding: 12px; vertical-align: top;">"[Response]"</td>
    </tr>
  </tbody>
</table>
```

#### 8. Action/Next Steps Block
```html
<div style="background-color: #FFF7ED; padding: 20px; border-radius: 8px; border: 1px solid #FED7AA; margin-bottom: 30px;">
  <h3 style="margin-top: 0; color: #C2410C; font-size: 18px;">⏭️ Próximos Passos (Fechamento)</h3>
  <p><strong>Objetivo:</strong> [Goal of the call]</p>
  <p style="margin-bottom: 0;"><em>"[Closing statement/ask]"</em></p>
</div>
```
