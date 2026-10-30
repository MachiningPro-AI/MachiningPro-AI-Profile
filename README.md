
PROJECT: SpotWeldPro AI
TASK: ENERGY-P2-FUNCTIONAL-UAT-01
MODE: SAFE ENGINEERING VALIDATION

CONTEXT:
- GitHub: Bursa-16/SpotWeldPro-AI
- Production commit: 503a818
- Render backend: https://spotweldpro-ai-api.onrender.com
- Demo frontend: https://spotweldpro-ai-demo.onrender.com
- Neon Alembic head: 0019_import_batches
- weld_groups and import_batches tables: verified
- All 12 ENERGY-P2 routes: registered and responding
- python-multipart hotfix: deployed

OBJECTIVE:
Validate the engineering correctness, API behavior,
frontend integration and reporting capabilities of
ENERGY-P2 before customer demonstrations.

PHASE 1 — BASELINE
1. Inspect repository and current Git state.
2. Identify all ENERGY-P2 backend and frontend modules.
3. Inspect existing tests and engineering formulas.
4. Identify all required inputs, units and outputs.
5. Do not assume that HTTP 401 proves functional correctness.

PHASE 2 — ENGINEERING CALCULATIONS
Independently verify:
- Single weld energy estimation
- Multi-spot energy aggregation
- Current, voltage, resistance and time calculations
- Unit conversions
- Energy totals and averages
- Electrode and process assumptions
- Cost calculations
- Optimization objective functions
- Engineering constraints and boundary conditions

Use deterministic reference cases and independently
calculated expected results.

Distinguish electrical input energy, estimated weld
energy and any model-derived efficiency assumptions.

Do not invent experimental measurements.

PHASE 3 — OPTIMIZATION
Verify:
- Optimization algorithms and constraints
- Feasibility checks
- Minimum and maximum parameter limits
- Objective function calculations
- Infeasible input handling
- Numerical stability
- Deterministic repeatability
- Behavior near engineering limits

Optimization must not recommend unsafe parameters
without appropriate engineering warnings.

PHASE 4 — DASHBOARD
Verify:
- Project-level aggregation
- Weld group aggregation
- Energy KPIs
- Cost KPIs
- Charts and summaries
- Correct handling of empty datasets
- Consistency between backend and frontend
- TR/EN terminology and engineering units

PHASE 5 — IMPORT AND EXPORT
Verify:
- Excel import templates
- XLSX parsing
- CSV report generation
- XLSX report generation
- PDF report generation
- Field mapping and validation
- Missing or invalid values
- Formula and unit consistency
- Exported results versus calculated results

Use local synthetic test fixtures only.

PHASE 6 — SECURITY AND DATA SAFETY
Verify:
- Authentication and authorization
- READ_ONLY role restrictions
- Invalid token handling
- Input validation
- File upload validation
- No secret leakage
- No unauthorized database writes

Do not execute authenticated production write requests.
Do not upload files to production.
Do not create or delete production records.

PHASE 7 — TEST EXECUTION
1. Run relevant local backend tests.
2. Run relevant frontend tests.
3. Run production build checks.
4. Independently verify key numerical results.
5. Investigate failures without hiding or excluding them.
6. Distinguish confirmed pre-existing failures from new regressions.
7. Perform production read-only probes only.

PHASE 8 — FINAL REPORT
Produce:

A. Functional coverage matrix
B. Engineering formula validation
C. Optimization validation
D. Dashboard validation
E. Import/export validation
F. Authentication and security findings
G. Test execution results
H. Defects ranked P0/P1/P2/P3
I. Missing capabilities
J. Recommended corrective actions

For every finding include:
- Exact file path
- Relevant function or line number
- Expected behavior
- Actual behavior
- Supporting evidence
- Severity
- Recommended correction

FINAL VERDICT:
PASS / CONDITIONAL PASS / FAIL

Explicitly distinguish:
1. Deployment readiness
2. API accessibility
3. Software functional correctness
4. Engineering model validation
5. Customer-demo readiness

STRICT SAFETY RULES:
- Do not modify production database.
- Do not modify production configuration.
- Do not commit.
- Do not push.
- Do not deploy.
- Do not execute destructive commands.
- Do not modify source files in this phase.
- Do not claim physical welding validation from
  synthetic data or unit tests.
- Stop after delivering the audit report.

