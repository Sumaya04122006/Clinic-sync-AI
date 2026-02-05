CLINIC-SYNCH AI
Clinical Note → SOAP Report + Red Flag Alerts (Hospital Documentation Assistant)

CLINIC-SYNCH AI is a clinical documentation tool that converts messy nurse notes, triage notes, and lab observations into a clean SOAP note format (Subjective, Objective, Assessment, Plan).
It also detects high-risk red flags (ex: chest pain, SOB, low SpO₂, rising troponin) and highlights contradictions or missing information to support faster clinical review.
This is a documentation support system, not a diagnostic tool.

Why this exists
Clinical notes are often written under pressure. They are inconsistent, incomplete, and hard to review quickly. That causes:
delays in decision-making
missed high-risk symptoms buried in text
poor documentation quality
higher workload for nurses/doctors
This app solves that by producing a structured SOAP report instantly.

What it does
Core features
SOAP Note Generator (EMR-style formatting)
Red Flag Detection (Critical/High/Moderate)
Evidence Citation (every extracted item references the exact phrase from the input)
Contradiction Detection (ex: “denies CP” + “mild CP at rest”)
Missing Data Flags (ex: allergies not mentioned, onset unclear)
Confidence Levels (High / Medium / Low)

Example input (messy note)
SOB x2d, mild CP @rest. confused at times.
SpO2 91% RA, HR 112, BP 142/88.
troponin trending up. ECG sinus tach.
+edema LLE. forgot ASA this morning.
pt feels weird.
Example output (summary)
CRITICAL: chest pain + rising troponin
HIGH: hypoxia (SpO₂ 91%), SOB, confusion
Contradiction detected: chest pain reported + denied
SOAP note generated with evidence citations

Tech stack
Built entirely using Lovable AI (no-code)
AI model: Google Gemini Flash
Storage: localStorage (demo mode)
Export: Copy + PDF download

How the workflow works
User pastes a raw clinical note
Model extracts symptoms/vitals/labs strictly from the text
System flags red alerts + contradictions
Output is formatted into SOAP structure
Report can be copied/exported

Safety & guardrails
Output is restricted to what is mentioned in the note
Any unclear statement is pushed into “Requires Review”
No diagnosis is claimed as a fact
Injection attempts in input are ignored

Current limitations
Works best for short-to-medium triage notes
Not connected to real EMR systems (FHIR/HL7 not implemented yet)
Demo version does not store patient identity (only synthetic testing)

Future upgrades (if deployed in real hospitals)
FHIR/HL7 export support
ICD-10 suggestion mode
Doctor sign-off workflow + revision tracking
Hospital dashboard analytics (alerts per day, trends)

Author
Sumaya
DDS AI Application Building Challenge (Lovable AI Build)
