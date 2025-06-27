+++
title = "IREB, ITIL und DevOps – Theorie und Praxis"
description = "Ein reflektierter Blick auf die Kombination verbreiteter Frameworks für Requirements Engineering, IT-Service-Management und agile IT-Betriebsmodelle."
slug = "ireb-itil-devops"
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
image = "/images/default-cover.webp"
alt = "Coverbild"
+++

# IREB, ITIL und DevOps – Komplementär oder widersprüchlich?

## Einleitung

IREB, ITIL und DevOps stehen für unterschiedliche disziplinäre Perspektiven: strukturierte Anforderungserhebung, regelbasiertes Service-Management und kontinuierliche, automatisierte Auslieferung. In der Projektpraxis begegnen sie sich dennoch regelmäßig – oft unfreiwillig. Dieser Beitrag beleuchtet, wie diese Ansätze zusammenspielen (können), wo sie sich reiben und was dies für die Gestaltung hybrider Betriebs- und Entwicklungsmodelle bedeutet.

## Spannungsfelder und Schnittstellen

**IREB** fokussiert sich auf die disziplinierte Erhebung, Dokumentation und Validierung von Anforderungen – häufig im Kontext klassischer Projektorganisation. **ITIL** versteht IT als Dienstleistung, mit Fokus auf Stabilität, Rollenklärung und Lifecycle-Prozesse. **DevOps** hingegen priorisiert Geschwindigkeit, Automatisierung und cross-funktionale Zusammenarbeit.

Diese Paradigmen bringen unterschiedliche implizite Annahmen mit:

- IREB erwartet ein zumindest temporär stabiles Zielsystem.
- ITIL setzt auf klare Verantwortlichkeiten und etablierte Prozesse.
- DevOps hinterfragt beides: Ziele und Prozesse sollen kontinuierlich weiterentwickelt werden.

An ihren Rändern treffen diese Modelle aufeinander: Das Anforderungsmanagement (IREB) definiert, was geliefert werden soll. DevOps sorgt für die Umsetzung und das Deployment. ITIL regelt den Betrieb und die Störungsbehebung. Friktionen entstehen dort, wo diese Übergänge nicht synchronisiert sind.

## Kombinationsszenarien: Praktische Muster statt Framework-Dogmen

In der Praxis zeigt sich: Die Integration dieser Modelle erfordert bewusste Übersetzungsarbeit. Einige erprobte Ansätze:

- **Serviceorientiertes Requirements Engineering**: Anforderungen werden nicht nur aus Sicht der Nutzer:innen, sondern auch aus Sicht der Serviceverantwortlichen (ITIL) formuliert – inklusive nicht-funktionaler Anforderungen wie Availability oder Maintainability.
  
- **DevOps-kompatible Spezifikationen**: IREB-Artefakte wie Use Cases oder User Stories werden so gestaltet, dass sie CI/CD-fähig sind – etwa durch präzise, testbare Akzeptanzkriterien oder standardisierte Schnittstellenbeschreibungen.

- **Shift-Left im Change Management**: ITIL-Prozesse für Changes werden durch DevOps-Prinzipien angereichert, etwa durch automatisierte Impact-Analysen auf Basis von Requirements-Tracing oder durch Feature-Flags statt klassischer Rollouts.

Das heißt konkret:

Weg vom Ticket-basierten Change-Prozess, bei dem jede Änderung manuell genehmigt wird.
Hin zu integrierten, automatisierten, überprüfbaren Freigaben – z. B. im Rahmen von Continuous Delivery.

Diese Muster setzen allerdings voraus, dass die Teams nicht in Frameworks denken, sondern in Aufgaben und Verantwortungsübergängen.

###Beispiele
- **Automatisierte Impact-Analysen** auf Basis von Requirements-Tracing
→ Anforderungen (z. B. aus IREB) sind systematisch mit Architekturkomponenten, Testfällen und Services verknüpft.
→ Bei Änderungen kann automatisiert ermittelt werden: „Welche Services sind betroffen? Welche Tests müssen angepasst werden?“

- **Feature-Flags** statt klassischer Rollouts
→ Neue Funktionen werden in der Produktivumgebung ausgeliefert, aber erst nach Freigabe (z. B. durch Konfiguration) aktiviert.
→ So wird der Rollout-Teil vom Deploy getrennt – das reduziert Risiko und erhöht Flexibilität.
→ Der klassische ITIL-Change („Bitte Rollout am Freitag um 20 Uhr“) wird überflüssig oder zumindest stark entlastet.

## Diagramm (optional)

{% mermaid() %}
flowchart TD
    A[IREB: Anforderungen erheben] --> B[DevOps: Umsetzen und deployen]
    B --> C[ITIL: Betrieb und Support]
    C --> D[Feedback an Requirements]
    D --> A
{% end %}

## Empfehlungen für die Praxis

- Kombinationsfähigkeit hängt weniger von Methoden, mehr von Kultur und Übersetzungsarbeit ab.
- Frameworks dürfen nicht zum Selbstzweck werden – sie müssen konkrete Probleme adressieren.
- Rollen wie Business Analyst:innen oder Service Owner sind prädestiniert, Brücken zwischen den Modellen zu schlagen.
- Werkzeuge wie Requirement-Tools, CMDBs oder CI/CD-Pipelines müssen aufeinander abgestimmt sein.

---

## Fazit

IREB, ITIL und DevOps lassen sich kombinieren – wenn sie als Baukästen verstanden werden, nicht als Religionen. Ihre Integration erfordert kritisches Denken, Rollenklärung und die Bereitschaft, etablierte Silos zu hinterfragen. Eine „One-Size-Fits-All“-Lösung gibt es nicht, wohl aber robuste Muster für ein kooperatives Zusammenspiel.

## Häufige Fragen (FAQ)

### Ist es überhaupt sinnvoll, klassische Modelle wie ITIL mit agilen Ansätzen wie DevOps zu kombinieren?

Ja, sofern die jeweiligen Stärken genutzt und Zielkonflikte offen adressiert werden. ITIL bietet Struktur und Stabilität, DevOps Geschwindigkeit und Flexibilität. Der Mehrwert liegt in der bewussten Kombination.

### Welche Rolle spielt Requirements Engineering in einem DevOps-Umfeld?

Auch in DevOps bleibt sauberes Requirements Engineering wichtig – nicht als Wasserfall-Vorarbeit, sondern als kontinuierlicher Prozess. Anforderungen müssen testbar, versionierbar und automationsfähig sein.

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Ist es überhaupt sinnvoll, klassische Modelle wie ITIL mit agilen Ansätzen wie DevOps zu kombinieren?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ja, sofern die jeweiligen Stärken genutzt und Zielkonflikte offen adressiert werden. ITIL bietet Struktur und Stabilität, DevOps Geschwindigkeit und Flexibilität. Der Mehrwert liegt in der bewussten Kombination."
      }
    },
    {
      "@type": "Question",
      "name": "Welche Rolle spielt Requirements Engineering in einem DevOps-Umfeld?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Auch in DevOps bleibt sauberes Requirements Engineering wichtig – nicht als Wasserfall-Vorarbeit, sondern als kontinuierlicher Prozess. Anforderungen müssen testbar, versionierbar und automationsfähig sein."
      }
    }
  ]
}
</script>