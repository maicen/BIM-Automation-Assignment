
# Proposed Solution: Automated & AI-Augmented Clash Detection

## Expected Improvements

The redesigned workflow transforms clash detection from a reactive,
manual process into a proactive, intelligence-driven system. The
most significant improvement is the elimination of manual triggers.
By deploying a Python script that monitors BIM 360 via API every
24 hours, the coordination cycle begins automatically the moment
a new model version is uploaded. This alone removes one of the
most common delays in traditional workflows — the gap between
model upload and clash test initiation.

The AI classification layer delivers the highest efficiency gain.
In a typical project generating 500 to 2,000 clashes per cycle,
a trained machine learning classifier can automatically resolve
80 to 90 percent of low-severity and duplicate clashes without
human review. This allows the BIM coordinator to focus exclusively
on genuinely critical conflicts, reducing review time from days
to hours. The automatic escalation path for critical clashes
ensures high-priority issues are never buried under minor ones.

Automated BCF issue assignment via the ACC API eliminates the
parallel spreadsheet and email chains that typically fragment
coordination data. Every clash becomes a tracked, assigned issue
with a documented resolution — creating a single source of truth
for the entire project team. Finally, the automated reporting
engine produces consistent coordination reports at the end of
every cycle, freeing the BIM coordinator from manual formatting
and enabling real-time visibility for clients and design leads.

## Potential Implementation Challenges

The primary technical challenge is the initial training of the
machine learning classifier. A sufficient volume of labelled
historical clash data is required before the model can classify
with reliable accuracy. For organisations without digitised
project archives, this represents a significant data preparation
effort before deployment.

Integration complexity is a secondary concern. Connecting
Navisworks, BIM 360, ACC, and the project management platform
through APIs requires robust middleware and careful authentication
management. Any API deprecation or platform update from Autodesk
could disrupt the pipeline, requiring ongoing maintenance.

There is also a risk of over-reliance on automated classification.
If the ML model incorrectly labels a critical clash as acceptable
— particularly in early project phases when training data is
limited — this could result in a construction conflict being
missed. Human review checkpoints for high-consequence clash
categories should be retained regardless of automation level.

## Organisational Impact

Adopting this workflow requires a cultural shift within the BIM
team. Coordinators must transition from manual execution roles
to supervisory and quality assurance roles — validating automated
outputs rather than producing them. This demands upskilling in
Python scripting, API management, and basic machine learning
concepts, which may require targeted training investment.

At the organisational level, the workflow creates measurable
competitive advantage. Faster coordination cycles reduce design
freeze delays, lower rework costs, and improve contractor
confidence in model quality. The continuous learning loop — where
resolved clashes feed back into the training dataset — means the
system improves with every project, compounding efficiency gains
over time across the organisation's project portfolio.
