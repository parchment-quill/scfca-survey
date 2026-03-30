# Sonoma County
Family Court 
Accountability Survey

A privacy-first, anonymous reporting tool designed to document patterns of judicial and attorney misconduct in Sonoma County, California family court.

Built to support real-time advocacy, not just retrospective research.

---

## Why This Matters

Family court decisions can have life-altering consequences, yet patterns of bias, misconduct, or systemic failure are often difficult to document and quantify.

This project creates a structured, anonymous way to:

- Identify patterns across cases  
- Surface systemic issues across judges and attorneys  
- Support accountability efforts  
- Amplify the experiences of affected families  

---

## Project Overview

The Family Court Accountability Survey collects anonymous, structured responses from family court participants regarding their experiences.

It is designed to:

- Protect respondent identity by default  
- Capture consistent, analyzable data  
- Enable pattern recognition across multiple cases  
- Support ongoing advocacy efforts while cases are still active  

---

## Status

🚧 In active development  
✅ Backend (Supabase) configured  
🟡 Frontend complete (HTML-based interface)  
⏳ Pending deployment via Vercel  
⏳ Repository integration via GitHub  

---

## Technical Architecture

### Backend: Supabase

Two primary tables with Row Level Security (RLS) enabled:

- `access_codes`  
  - Stores generated survey access codes  
  - Tracks distribution status  

- `survey_responses`  
  - Stores anonymous survey submissions  

**Access Code Format:**  
```
XXXX-XXXX-XXXX
```

**Distribution Model:**  
Codes are generated in batches and distributed through trusted intermediaries to control access and prevent abuse.

---

### Frontend Components

| Component | Description |
|----------|-------------|
| Survey (HTML, 6 sections) | Mobile-first, privacy-centered respondent interface |
| Access Code Manager | Code generation, upload, and tracking |
| Response Viewer | Filtering, visualization (bar charts), export tools |

---

### Data Design

- Anonymous by default  
- Contact information is fully optional  
- Language is intentionally non-institutional and protective  
- Designed to support both active and closed cases  

---

### Attorney Dataset

- 144 deduplicated Sonoma County family law attorneys  
- Compiled from:
  - California State Bar records  
  - Sonoma County Bar Association directory  
- Standardized format:
  First Last  
- Integrated into survey selection interface  

---

## Setup & Deployment

### 1. Clone the Repository
```
git clone <your-repo-url>
cd <your-repo-folder>
```

---

### 2. Configure Supabase

- Create a Supabase project  
- Run your SQL schema  

If you encounter existing table errors:

```
DROP TABLE IF EXISTS survey_responses;
DROP TABLE IF EXISTS access_codes;
-- Then run full CREATE TABLE sequence
```

---

### 3. Run Locally

This project uses static HTML interfaces:

- Open files directly in browser  
or  
- Use a simple local server  

---

### 4. Deploy

- Push repository to GitHub  
- Import project into Vercel  
- Deploy as static frontend  

---

## Development Notes

- System designed for controlled access, not open public submission  
- Emphasis on data integrity over volume  
- Architecture supports future expansion:
  - Additional counties  
  - Expanded datasets  
  - Advanced analytics  

---

## Design Principles

- Privacy-first  
- Survivor-aware language  
- Non-institutional tone  
- Structured but flexible data collection  
- Built for real-world use during active legal processes  

---

## Contributing

This project is currently controlled and in active development.

Potential collaboration areas:

- Data analysis  
- UI/UX improvements  
- Security review  
- Advocacy alignment  

---

## License

To be determined.

---

## Contact

For questions or collaboration inquiries, connect via GitHub.

---

## Notes

This repository focuses on the tooling and system design.  
Contextual background and case-specific details are intentionally limited in this document.
