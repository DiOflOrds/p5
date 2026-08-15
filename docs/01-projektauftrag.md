# Projektauftrag P5 — „Genesis 2.0: Organisationsrahmen" (v0.1, zur G0-Freigabe)

*2026-08-15, PL. Eingang per Intake nach Auftraggeber-Update (Diagramm + Beschreibungen PM-Team/Projekt-Teams). Grundlage: Orgkonzept v1.0 (`process/docs/02-genesis-2.0-orgkonzept.md`) mit den entschiedenen Kernfragen F14–F17 (p0/D027): Session-Takt als Ausführungsmodell, Klasse B an PM, Pilot-Team Mail-Zusammenfassung (→ P6), harte Guardrails zu Außenwirkung und sensiblen Daten. G0-Freigabe: Inbox-DR T-0001.*

## Was und Warum

Aus dem Ein-Team-Betrieb wird eine Organisation: neben dem ASPICE-Team entstehen ein **Projektmanagement-Team** (Drehscheibe zwischen Mensch und allen Teams) und beliebig viele **Projekt-Teams** (Steuer, Mail, Trading-Analyse, Wissenschaft …). P5 baut dafür den **Rahmen** — Governance und die kleine Mechanik, damit Team-Gründung später Routine ist statt Einzelfall-Bastelei. Die Teams selbst (ab P6) sind ausdrücklich NICHT Teil von P5. Leitidee aus dem Orgkonzept: generalisieren statt neu erfinden — die Repo-Konvention (`tickets/` + Discovery) macht jedes Team-Repo automatisch zum vollwertigen Mission-Control-Projekt.

**Zielprodukt-Typ:** Governance (Playbook/Registry/Template) + kleine Plattform-Mechanik (SW, F6) · **Nutzerkreis:** Auftraggeber + Registry-Nutzer (F9) · **Vertraulichkeit:** privat (F10); sensible Team-Daten regelt die F17-Datenklassen-Guardrail · **Budget:** 0 € API (F14: Session-Takt).

## Epics

| Epic | Inhalt | Konzept-Bezug |
|---|---|---|
| P5-E1 | **Prozessprofile ins Playbook:** `entwicklung` (heutiges Voll-ASPICE), `dienstleistung` (MAN.3 + SUP light, G0/G4), `wiederkehrend` (Kanban mit Takt, SLA statt G4) — je Profil Gates, Pflicht-Artefakte, DoD | Kap. 2.1 / L… Profile |
| P5-E2 | **Entscheidungsklassen + Guardrails:** Klasse A (immer Mensch), B (PM allein, geloggt + sichtbar), C (Teams); F17-Guardrails („KI handelt nie mit Außenwirkung", „sensible Daten nie in Repos mit GitHub-Remote") mit gleicher Härte wie „Sandbox pusht nie" | F15/F17, L3–L5 |
| P5-E3 | **Team-Registry + Team-Template:** `process/teams/registry.yaml` (Team, Typ, Profil, Rollen, Status) + Gründungs-Template (Repo-Skelett `team-*`, Checkliste als Erweiterung von intake.md auf Teams — Gründung ist Klasse A) | Kap. 2.4, L7 |
| P5-E4 | **PM-Team-Repo `pm`:** Kanban-Dauerbetrieb (keine Sprints), Intake-Queue, Session-Agenda („welche Teams tickt die heutige Session, in welcher Reihenfolge"), eigenes Decision-Log für Klasse-B-Entscheidungen; erscheint per Discovery automatisch in Mission Control | Kap. 2.2, F14/F15 |
| P5-E5 | **Kleine Mechanik, nur wo nötig:** Verträglichkeit von board/Discovery/Cockpit mit sprintlosem Kanban-Betrieb; etwaige Plattform-Änderungen requirements-first (ab SWR-053) — erwartet: minimal | L6 (nur der P5-Anteil) |

**Nicht in P5:** reale Team-Gründung (P6, Pilot Mail-Zusammenfassung), Takt-Automatik/Autopilot (per CR nach F14), HMI-Skalierung L9, Zugangs-Register L2 in voller Breite (Pilot klärt das Muster).

## Abnahmekriterien

1. **Profile:** Playbook enthält die drei Prozessprofile mit Gates/Artefakten/DoD je Profil; Review-Stichprobe durch Auftraggeber.
2. **Klassen + Guardrails:** A/B/C verankert; die zwei F17-Guardrails stehen als harte Regeln im Playbook/guardrails; Klasse-B-Entscheidungen haben ein append-only PM-Decision-Log, über Mission Control einsehbar.
3. **Registry + Template:** `teams/registry.yaml` und Team-Template existieren; Probelauf: ein Muster-Team-Repo aus dem Template besteht board-check lokal (Trockenlauf, ohne GitHub).
4. **PM-Repo real:** `pm` läuft im Kanban-Betrieb, erscheint automatisch in Mission Control (Discovery-Nachweis), enthält erste Session-Agenda und die D027-Übernahme als erste Log-Einträge.
5. **Prozesskonformität:** Gates als Inbox-DRs mit Frist-Default, Aufwandsschätzung je Planning, etwaige Plattform-Änderungen requirements-first ab SWR-053 mit Matrix 0 Lücken, 0 € API.

## Rahmen

2 Sprints (S0: E1–E3 Governance-Fassung → G1-artige Freigabe als Inbox-DR; S1: E4/E5 Umsetzung + Probelauf + Abnahme G4). Kein G2 nötig, solange E5 keine Architektur berührt (sonst kleines ADR). Playbook, Team-Node-Gate, Baselines als Tags + Manifest, Sandbox pusht nie.
