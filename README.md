# AI-Powered Smart Grid & Predictive Energy Management Agent

An event-driven, autonomous AI Agent orchestration system built to optimize micro-grid energy efficiency in heavy manufacturing sectors. This framework is explicitly mapped to fulfill **UN Sustainable Development Goals: SDG 7 (Affordable and Clean Energy)** and **SDG 9 (Industry, Innovation, and Infrastructure)**.

---

##  Live Project Artifacts
- **Presentation Deck :** https://drive.google.com/drive/folders/1qQTumgSNCD8OGS9VxWa95vkR92yQq-LN?usp=drive_link
- **Project Concept Note :** https://drive.google.com/drive/folders/1tYNVDOzmCg0p-FzQDsip219waZ0P5sSN?usp=drive_link
- **Prototype Live Demo Video:** https://drive.google.com/drive/folders/1c7OAqMuoHGvctQHHEjNBouUTkltgRRaK?usp=drive_link

---

##  System Overview & Architecture
The system functions as a fully closed-loop autonomous pipeline deployed via **n8n orchestration**:
1. **Data Ingestion:** Automatically fetches real-time localized environmental variables (Cloud Cover, Temp) from the Open-Meteo API alongside simulated industrial metrics (Factory Load, Battery SoC).
2. **AI Decision Brain:** Routes parameters through **Google Gemini (models\gemini-3-flash-preview)** using a strict `Structured Output Parser` to ensure deterministic, enterprise-ready raw JSON decisions.
3. **Telemetry Logging:** Appends clean tabular outputs immediately to Google Sheets.
4. **HTML Alerts:** Dispatches crisp, scannable corporate notification tables to factory managers via Gmail during critical grid shifts.

---

##  Project Lean Canvas

### Problems
- Volatile electricity tariffs and heavy financial penalties when industrial machinery spikes over 250 kW.
- Unpredictable solar energy supply caused by sudden weather changes and cloud cover exceeding 70%.
- Delayed manual response from human operators trying to monitor meters and switch power sources.

### Solutions
- Automated n8n workflow for instant peak-shaving when factory consumption hits critical thresholds.
- AI logic that tracks live weather APIs to predict solar drops and safely switch loads beforehand.
- End-to-end telemetry system that logs data to Google Sheets and emails clean HTML tables to managers.

### Unique Value Propositions
- Autonomous zero-lag grid management that balances factory loads against local weather without human intervention.
- Auditable cost reduction system that proves power savings while directly mapping to UN SDG 7 and SDG 9 benchmarks.

### Unfair Advantage
- Low-overhead cloud workflow setup that cuts out the massive licensing costs of traditional industrial energy software.
- Hardcoded structural JSON validation that restricts the AI to strict engineering boundaries and prevents any logical errors.

### Customer Segments
- Medium-scale heavy manufacturing plants facing high demand charges during peak daytime operational shifts.
- Commercial micro-grid hubs running localized solar arrays paired with industrial battery banks.

### Existing Alternatives
- Manual monitoring where factory floor technicians manually track multi-meters and pull breaker switches.
- Rigid legacy enterprise energy software requiring heavy hardware modification and expensive developer retainers.

### Early Adopters
- Solar-integrated manufacturing plants that have on-site batteries but lack the software automation to utilize them dynamically.
- Energy-intensive fabrication units working fixed daytime shifts looking to cut peak power penalties immediately.

### Key Metrics
- Peak tariff cost savings achieved by diverting loads away from the grid during high consumption spikes.
- Localized green energy yield tracking the total increase in solar consumption over main grid reliance.
- Workflow execution time measured from live API data capture down to database entry and email delivery.

### Channels
- Direct technical consulting targeting Plant Heads and Operational Managers showing direct power bill savings.
- Networks of industrial automation vendors who handle standard factory layouts but lack an active AI layer.
- Industrial tech communities and marketplaces where factory owners look for pre-built workflows.

### Cost Structure
- Minimal cloud infrastructure fees required to keep the active n8n automation pipeline running continuously.
- Light API token compute costs generated when passing core telemetry variables through the LLM.

### Revenue Streams
- Value-share monetization taking a small percentage cut out of the factory's verified monthly electricity bill savings.
- Fixed technical integration fees charged for deploying and connecting the n8n model to specific factory APIs.

---

##  How to Run This Workflow
1. Download the `workflow.json` file from this repository.
2. Open your n8n dashboard, create a blank workflow.
3. Click on the top-right menu and select **Import from File**, then choose the `workflow.json`.
4. Configure your Google Gemini API Node with your personal credentials.
5. Setup your Google Sheets and Gmail node OAuth2 authentications.
6. Click **Execute Workflow** to run the live simulation layer.
