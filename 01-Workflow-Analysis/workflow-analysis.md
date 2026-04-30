
# BIM Workflow Analysis: Clash Detection & Coordination

**Lead Authors:** Mark Shane Haines (problem definition) | Letícia Cristovam Clemente (analysis)

---

## 1. Description of the Original BIM Workflow

Clash detection and coordination is one of the most critical and
time-intensive workflows in any BIM project. The process involves
federating discipline-specific models — Architecture, Structure,
and MEP — into a single environment to identify geometric conflicts
before construction begins.

In a typical project, the BIM coordinator manually imports updated
models from each discipline into Autodesk Navisworks or BIM 360
Coordinate. Clash test rules are then manually configured for each
discipline pair, for example Structure vs MEP or Architecture vs
Mechanical. Once the tests are run, Navisworks generates a raw clash
report that commonly contains between 500 and 2,000 clashes per
coordination cycle.

The coordinator then opens each clash individually, visually inspects
it in the 3D viewer, and assigns a status such as Active, Reviewed,
or Approved. Clashes are manually grouped when they appear to be
duplicates or part of the same system conflict. Each assigned clash
is then communicated to the responsible discipline via BCF export,
email, or a shared spreadsheet. Disciplines resolve their conflicts,
re-upload new model versions, and the entire cycle repeats —
typically on a weekly or biweekly basis.

Final coordination reports are manually compiled by the BIM
coordinator, exporting clash data from Navisworks and reformatting
it into a PDF or Excel document for client and design team review.

---

## 2. Identification of Inefficiencies

### 2.1 Manual Processes

Every clash test must be manually triggered following each model
upload. There is no automated detection of new model versions or
automatic initiation of the coordination process. Clash grouping,
categorisation and status assignment are performed visually and
individually by the coordinator. Report generation requires manual
extraction and reformatting of data outside of the BIM platform.

### 2.2 Repetitive Tasks

The same clash test configurations are re-run each coordination
cycle without modification. Known recurring clashes — such as
structural penetrations or standard MEP crossings — are reviewed
repeatedly despite being previously documented. Report formatting
follows an identical structure each cycle, yet is manually
reproduced every time.

### 2.3 Data Bottlenecks

There is no automated notification system to alert the coordinator
when a new model version has been uploaded by a discipline. Clash
data remains siloed within Navisworks and is not connected to
project management platforms such as Procore or Aconex. Multiple
parallel spreadsheets and email chains create inconsistent clash
status records across the project team.

### 2.4 Coordination Challenges

High clash volumes make prioritisation extremely difficult. A
critical structural conflict can easily be buried among hundreds
of minor soft clashes or duplicates. The current process lacks
intelligence to distinguish hard clashes from acceptable
penetrations with sleeves or pre-approved crossings.
Cross-discipline coordination meetings frequently waste time
revisiting already-closed issues due to unreliable status
tracking. The absence of historical clash data analysis means
recurring design errors are not identified or fed back to
design teams as lessons learned.
