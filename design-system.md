# MedLens Design System & Clinical Safety Brief

## Color Palette (Clinical & High-Contrast)
- Primary / Header Background: #0F172A (Deep Slate)
- Accent / Actions: #2563EB (Clinical Blue)
- Background: #F8FAFC (Soft Light Grey — avoids screen fatigue)
- Card Surfaces: #FFFFFF (Pure White)
- Status - High/Abnormal: #DC2626 (Muted Red Pill)
- Status - Low: #D97706 (Amber Pill)
- Status - Normal: #16A34A (Muted Green Pill)
- Provenance Badge (User Provided): #3B82F6 (Blue Badge)
- Provenance Badge (AI Extracted): #8B5CF6 (Purple Badge)

## Core UI / UX Rules
- Split-Screen Layout: Left pane = Original source file/input; Right pane = Structured record.
- Visual Provenance: Every single field MUST display a clear tag ("User Input" vs "AI Extracted").
- Flagging: Numerical lab values out of range get a clear indicator tag ("HIGH" / "LOW") based solely on the report's explicitly stated ranges.
- Disclaimers: Sticky footer banner on all views: "MedLens is an information organizing tool and does not provide medical diagnoses or treatment recommendations."
