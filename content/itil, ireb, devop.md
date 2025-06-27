+++
title = "Requirements Management im IT-Betrieb – Zwischen Incident Queue und Change Advisory Board"
description = "Ein kritischer Blick auf die Rolle von Anforderungen in laufenden IT-Service-Umgebungen – jenseits von Projektlogik und Entwicklungszyklen."
slug = "requirements-management-it-betrieb"
date = 2025-06-27
updated = 2025-06-27

[extra]
comment = true
math = false
mermaid = true
page_summary_on_paginator = true
page_info = []
toc = true
section = "_index.md"

[extra.cover]
image = "/images/schnittstellenanalyse.webp"
alt = "Stilisierte Blöcke als Symbol für methodische Integration"
+++

# Requirements Management im IT-Betrieb – Zwischen Incident Queue und Change Advisory Board

## Einleitung

Requirements Engineering gilt gemeinhin als Disziplin der Projektwelt. Doch Anforderungen entstehen nicht nur vor oder während der Softwareentwicklung – sie entstehen auch im laufenden Betrieb: durch Nutzerfeedback, regulatorische Anpassungen oder Betriebsstörungen. Wer Requirements Management ausschließlich als vorgelagerte Disziplin versteht, riskiert blinde Flecken an einer entscheidenden Stelle der Wertschöpfung.

## Anforderungen im Betrieb: Quellen, Formen, Konflikte

Im produktiven Betrieb entstehen Anforderungen kontinuierlich, allerdings selten als formal strukturierte Spezifikationen. Typische Quellen sind:

- **Incidents und Problem-Tickets**
- **Change Requests**
- **Compliance- und Security-Anforderungen**
- **Beobachtungen aus Monitoring und Logging**

Diese Anforderungen stehen häufig in einem Spannungsfeld:
- zwischen Stabilität (ITIL) und Veränderung (DevOps),
- zwischen operativer Dringlichkeit und strategischer Planung,
- zwischen implizitem Erfahrungswissen und formalisierter Dokumentation.

## Praktische Muster für Requirements Management im Betrieb

### 1. Betriebssicht in das Anforderungsboard integrieren
### 2. Bidirektionales Tracing zwischen Incident- und RE-Objekten
### 3. Change Management als integrativer Anforderungskanal

## Diagramm

{% mermaid() %}
flowchart TD
    I[Incident / Problem] --> A[Analyse und Kategorisierung]
    A -->|nicht-relevant| X[Abschluss]
    A -->|potentieller Bedarf| R[Anforderung ableiten]
    R --> B[Story / Change formulieren]
    B --> C[Entwicklung / Umsetzung]
    C --> D[Deployment in Betrieb]
    D --> F[Überprüfung im Monitoring]
    F -->|Problem gelöst| X
    F -->|Problem besteht| I
{% end %}

## Tipps oder Zusammenfassung

- Requirements entstehen auch im Betrieb – RE endet nicht mit dem Go-Live.
- Nicht jede Beobachtung ist eine Anforderung – aber jede sollte geprüft werden.
- Tracing zwischen Incidents, Changes und Anforderungen ist essenziell.
- Change-Prozesse bieten wertvolle Kontexte für RE – wenn sie genutzt werden.

---

## Fazit

Requirements Management endet nicht mit dem Go-Live. Im Gegenteil: Der produktive Betrieb ist ein permanenter Resonanzraum für Anforderungen – vorausgesetzt, man richtet die richtigen Antennen aus. Wer RE als Teil des Betriebs versteht, schafft die Grundlage für kontinuierliche Verbesserung – jenseits von DevOps-Rhetorik und ITIL-Schablonen.

## Häufige Fragen (FAQ)

### Muss man im Betrieb tatsächlich vollständige Anforderungen dokumentieren?

Nein, aber man braucht strukturierte Entscheidungen über Anforderungen – auch im Betrieb. Das heißt: Klarheit über Bedarf, Wirkung und Bewertungskriterien. Das Dokument ist zweitrangig, das gemeinsame Verständnis zentral.

### Wie unterscheidet man Anforderungen von reinen Betriebsaufgaben?

Durch Wirkungsperspektive: Betriebsaufgaben zielen auf Wiederherstellung (Incident), Anforderungen auf Veränderung. Die Grenze ist nicht immer scharf – aber sie ist relevant für Budgetierung, Priorisierung und Qualitätsmanagement.

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Muss man im Betrieb tatsächlich vollständige Anforderungen dokumentieren?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nein, aber man braucht strukturierte Entscheidungen über Anforderungen – auch im Betrieb. Das heißt: Klarheit über Bedarf, Wirkung und Bewertungskriterien. Das Dokument ist zweitrangig, das gemeinsame Verständnis zentral."
      }
    },
    {
      "@type": "Question",
      "name": "Wie unterscheidet man Anforderungen von reinen Betriebsaufgaben?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Durch Wirkungsperspektive: Betriebsaufgaben zielen auf Wiederherstellung (Incident), Anforderungen auf Veränderung. Die Grenze ist nicht immer scharf – aber sie ist relevant für Budgetierung, Priorisierung und Qualitätsmanagement."
      }
    }
  ]
}
</script>
