# Sprint-1-Report P5 — PM-Gründung + Probelauf + Abnahmevorbereitung

*2026-08-15, PL. Tickets T-0007–T-0010 done, Abnahme-DR T-0011 in der Inbox.*

## Ergebnis

Das PM-Team existiert real: Repo `pm` als erster Vollzug des neuen Gründungs-Prozesses (intake.md v2) — Charter v1.0 nach der Auftraggeber-Beschreibung, team.yaml mit 4 SLAs, drei Kanban-Takt-Tickets (Session-Agenda, Intake-Queue, LeLe Q4), Session-Agenda v1 und Klasse-B-Decision-Log mit den ersten Einträgen B000/B001. Registry: `pm` auf `aktiv`. Discovery zeigt pm automatisch neben p0–p5 — ohne eine Zeile Plattform-Code.

## E5-Befund (Verträglichkeit sprintloser Betrieb)

| Prüfung | Lauf | Ergebnis |
|---|---|---|
| board.py Validierung + BOARD.md | `board.py pm` / `--check` | OK, 3 Tickets |
| Discovery/Cockpit-Aggregation | `cockpit_alle('.')` | pm erscheint: p0…p5, **pm** |
| Cockpit-Kennzahlen | `cockpit('.', 'pm')` | status_zahlen {open: 3}, briefe_offen 0 |
| Inbox/Briefkasten | repo-agnostisch (ADR-004) | keine Sonderfälle |

**Keine Code-Änderung nötig → keine neuen SWRs** (K5-Klausel greift nicht). Matrix bleibt 52/0.

## K3-Probelauf (Template)

Template → `/tmp/team-muster` (bewusst außerhalb des Arbeitsordners), Platzhalter gefüllt (Profil `dienstleistung`), `git init`: board.py **0 Tickets validiert**, BOARD.md generiert, `--check` grün, 0 Platzhalter-Reste.

## Abnahmebilanz K1–K5

| K | Kriterium | Bewertung | Evidenz |
|---|---|---|---|
| 1 | Playbook: 3 Profile mit Gates/Artefakten/DoD | **erfüllt** | Kap. 15 (v0.7), Stichprobe G1/D001 |
| 2 | Klassen A/B/C + F17-Guardrails + Klasse-B-Log | **erfüllt** | Kap. 16; `pm/management/decisions/` B000/B001, via Mission Control einsehbar |
| 3 | Registry + Template + Probelauf | **erfüllt** | registry.yaml (3 Einträge), Template, /tmp-Trockenlauf grün |
| 4 | PM-Repo real, Discovery, Agenda, D027-Übernahme | **erfüllt** | pm-Repo, cockpit_alle-Nachweis, session-agenda.md, B000 |
| 5 | Prozesskonformität (Gates, Schätzung, req-first, 0 €) | **erfüllt** | D000/D001 via Inbox; E5-Schätzspalten; keine Code-Änderung → keine SWRs nötig; 0 € |

## Aufwand (E5)

Sprint 0: geschätzt 85 min · Sprint 1: geschätzt 75 min · Ist gesamt: ≈ 138 min (−14 %, konsistent mit P2–P4-Kalibrierung).

## Retro (Kurzform)

**Gut:** Gründungs-Prozess funktionierte beim ersten echten Durchlauf (pm) und im Trockenlauf (Muster) ohne Korrektur; „generalisieren statt neu erfinden" hat sich ausgezahlt — 0 Zeilen Plattform-Code für ein neues Team. **Beobachtung:** dauerhaft offene Takt-Tickets sind im Board-Ampelbild ungewohnt (immer „open") — Beobachtungsauftrag an LeLe Q4 (pm/T-0003), ob eine Takt-Kennzeichnung im HMI gewünscht wird (wäre ein kleiner CR, kein Muss). **Risiko benannt:** Session-Takt heißt: kein Digest ohne Session — bewusste F14-Entscheidung, Autopilot-CR bleibt im Backlog.
