# P5-Abschlussbericht — „Genesis 2.0: Organisationsrahmen" (PL)

*2026-08-15. An: Auftraggeber. Zeitraum: ein Tag (Konzept bis Abnahme), Sprints 0–1, Baseline **p5-v1.0** (p5 + platform). Abnahme: G4a/D002 via Inbox.*

## Was gebaut wurde

Aus dem Ein-Team-Betrieb wurde eine Organisation mit Regelwerk: **Playbook Kap. 15** — drei Prozessprofile (`entwicklung`, `dienstleistung`, `wiederkehrend`), damit jedes künftige Team genau so viel Prozess bekommt, wie es braucht. **Kap. 16** — Entscheidungsklassen A/B/C plus die zwei F17-Guardrails in voller Härte (keine KI-Handlung mit Außenwirkung; sensible Daten nie in Repos mit GitHub-Remote, mit Datenklassen-Systematik). **Team-Registry + Gründungs-Template + intake.md v2** — Team-Gründung ist jetzt eine Checkliste (Klasse A) statt Handarbeit. Und als erster Vollzug: das **PM-Team** (Repo `pm`) — Charter nach deiner Beschreibung, 4 SLAs, Kanban-Takt-Tickets, Session-Agenda, Klasse-B-Decision-Log (B000/B001). Grundlage überall: Orgkonzept v1.0 + deine Entscheidungen F14–F17 (p0/D027).

## Abnahmekriterien — Ergebnis

| K | Kriterium | Bewertung | Evidenz |
|---|---|---|---|
| 1 | Drei Profile im Playbook | **erfüllt** | Kap. 15 (v0.7), Stichprobe G1/D001 |
| 2 | Klassen + Guardrails + Klasse-B-Log | **erfüllt** | Kap. 16; pm-Log B000/B001, via Mission Control einsehbar |
| 3 | Registry + Template + Probelauf | **erfüllt** | registry.yaml; Trockenlauf `/tmp/team-muster`: board-check grün, 0 Platzhalter |
| 4 | PM-Repo real im Kanban-Betrieb | **erfüllt** | pm per Discovery in Mission Control (Cockpit-Stichprobe D002), Agenda v1 |
| 5 | Prozesskonformität, 0 € | **erfüllt** | D000–D002 via Inbox; Schätzung je Planning (Ist −14 %); **0 Zeilen Plattform-Code** → keine neuen SWRs; Matrix bleibt 52/0 |

## KPIs

Tests 156 + 42 grün · Matrix 52/0 · Projektlaufzeit: 1 Tag · 3 Entscheidungen via Inbox · 0,00 € API · Plattform-Änderungen: 1 CI-Checkout-Zeile (pm), sonst nichts.

## Übergabe an den Betrieb

Die Organisation läuft ab jetzt über die **PM-Session-Agenda** (Briefkasten zuerst → Takt-Tickets → aktive Projekte → Betriebs-Backlog). Nächster Klasse-A-Entscheid liegt bereits in der Inbox: **Gründung des Pilot-Teams team-mail** (pm/T-0004) — mit der wichtigen Weiche: Datenklasse `sensibel` → lokales Repo ohne GitHub-Remote (Guardrail 2). Vorgehens-Hinweis (B002): Die Gründung läuft als Routine nach intake.md v2 unter PM-Aufsicht mit 2-Wochen-Pilotreview statt als eigenes Projekt-Repo „P6" — dein Einspruch dazu jederzeit möglich. Betrieb offen: BB-5 (PAT ab 2026-09-05).
