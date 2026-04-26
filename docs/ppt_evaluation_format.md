# PPT Format for Case Study Evaluation

## Project
**Civic Resolve – Intelligent Complaint Routing**  
(Flask + MySQL + Scikit-learn NLP Routing)

---

## Evaluation Mapping (Total: 30 Marks)
- **Idea**: 10 marks
- **Presentation**: 10 marks
- **Working Prototype**: 5 marks
- **Viva**: 5 marks

> Suggested presentation length: **10–12 slides** in **8–10 minutes**.

---

## Slide-by-Slide Format

### Slide 1 — Title Slide
- Project title
- Team member names and roles
- Course / faculty / date
- One-line value proposition: *"AI-assisted routing of campus maintenance complaints to the right department in real time."*

---

### Slide 2 — Problem Statement
- Current issue in manual complaint handling:
  - Delayed routing
  - Wrong department assignment
  - Poor visibility for users/admin
- Why this matters:
  - Slower resolution time
  - User dissatisfaction
  - Operational inefficiency
- Target context: campus/community complaint system

---

### Slide 3 — Proposed Solution (Idea Focus)
- **Civic Resolve** as an intelligent complaint management platform
- Key concept:
  1. User submits text complaint
  2. ML model predicts wing/category
  3. Ticket is auto-assigned and tracked
- Stakeholders supported:
  - User (student/faculty/staff)
  - Maintenance team
  - Superadmin

---

### Slide 4 — Objectives and Scope
- Build a role-based complaint portal
- Auto-categorize complaints with NLP
- Track lifecycle: Pending → In Progress → Resolved/Referred
- Provide admin-level oversight and reassignment
- Keep architecture lightweight and extensible

---

### Slide 5 — Methodology / System Workflow
- Development methodology (iterative prototype)
- Pipeline:
  1. Data collection (`complaints.csv`, `users.csv`)
  2. Text preprocessing
  3. TF-IDF vectorization
  4. Multinomial Naive Bayes training
  5. Model export (`model.pkl`, `vectorizer.pkl`)
  6. Flask inference integration (`/api/submit_ticket`)

---

### Slide 6 — Architecture and Tech Stack
- **Backend**: Flask, Python
- **Database**: MySQL (tickets, logs, users)
- **ML**: Scikit-learn (TF-IDF + MultinomialNB)
- **Frontend**: HTML, CSS, JavaScript
- **Security**: Session-based auth + role-based route access
- Add a flow diagram: User input → Prediction → Storage → Dashboard actions

---

### Slide 7 — Working Prototype (User Module)
- Screens to show:
  - Login/role selection
  - User dashboard complaint form
  - Ticket list with status badges
- Demo points:
  - New complaint submission
  - Auto-predicted wing returned in backend
  - Feedback form submission

---

### Slide 8 — Working Prototype (Staff/Admin Module)
- **Staff dashboard**:
  - Aging complaints view
  - Priority/status updates
  - Resolve/Refer actions
- **Admin dashboard**:
  - Active tickets, resolution rate
  - Escalated/referred tickets
  - Wing reassignment + system logs

---

### Slide 9 — Data & Model Highlights
- Dataset snapshot:
  - Complaint text + label (`true_wing`)
  - Multiple categories (Electrical, Plumbing, IT, HVAC, etc.)
- Notebook highlights:
  - Train/test split
  - Accuracy + classification report
- Mention observed data issues / limitations:
  - Label noise/mismatch in some rows
  - Scope for more cleaning and re-training

---

### Slide 10 — Results, Benefits, and Impact
- Practical outcomes:
  - Faster complaint routing
  - Reduced manual effort
  - Better accountability through ticket lifecycle
- Institutional impact:
  - Improved service quality
  - Better decision support via dashboard/logs

---

### Slide 11 — Challenges, Limitations, and Future Work
- Current limitations:
  - Basic model baseline
  - Dependence on data quality
  - Local deployment assumptions
- Future enhancements:
  - Better NLP models (e.g., transformer-based classifier)
  - Multilingual complaint support
  - Notification system (email/SMS)
  - Analytics dashboard with trends and SLA tracking

---

### Slide 12 — Conclusion + Viva Prep Backup
- 3-line conclusion:
  - Problem solved
  - Working prototype delivered
  - Scalable path ahead
- Add final “Thank You / Questions”
- Keep backup slides for viva:
  - DB schema
  - API list
  - Model training details
  - Team contribution split

---

## How to Maximize Marks (Checklist)

### For **Idea (10 marks)**
- Clearly define pain point and gap in existing process
- Justify ML-based routing over manual triage
- Show novelty: role-wise dashboards + intelligent assignment

### For **Presentation (10 marks)**
- Keep each slide focused (no text wall)
- Use screenshots from actual prototype
- Use one consistent theme and visual hierarchy
- Maintain clear narrative: Problem → Method → Prototype → Impact

### For **Working Prototype (5 marks)**
- Live demo flow:
  1. Login as user and submit complaint
  2. Show assigned wing/status in system
  3. Login as maintenance and update ticket
  4. Login as admin and show escalations/reassignment

### For **Viva (5 marks)**
Be ready for:
- Why TF-IDF + Naive Bayes?
- How role-based access is enforced?
- How misclassified tickets are handled?
- What are scalability and security considerations?

---

## Suggested Time Split (8–10 mins)
- Problem + Idea: 2.5 min
- Methodology + Architecture: 2.5 min
- Prototype Demo: 3 min
- Results + Future Work + Conclusion: 1.5–2 min
