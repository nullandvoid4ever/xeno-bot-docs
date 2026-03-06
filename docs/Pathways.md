---
title: Xenomorph Pathways
description: Evolution pathways for xenomorphs in Xeno Bot
tags:
  - pathways
  - evolution
  - gameplay
keywords:
  - Xenomorph
  - Evolution
  - Pathways
  - Drone
  - Queen
author: Devvyyxyz
date: 2026-03-06
toc: true
icon: material/graph
---

# Xenomorph Pathways

This guide shows all evolution pathways for xenomorphs, from the initial egg/facehugger stage through to their final forms.

## Main Pathways

### Human Pathway (Standard) ![Facehugger](img/emojis/facehugger.png){ width="32" } ![Warrior](img/emojis/warrior.png){ width="32" } ![Queen](img/emojis/xenomorph_queen_sprite.png){ width="32" }

The classic xenomorph evolution path using human hosts.

```mermaid
graph LR
    FH[Facehugger] -->|Human Host| D[Drone]
    D -->|10 Royal Jelly| W[Warrior]
    W -->|25 Royal Jelly| PR[Praetorian]
    PR -->|50 Royal Jelly| Q[Queen]
    
    classDef start fill:#8B4513,stroke:#654321,stroke-width:2px,color:#fff
    classDef mid fill:#4A5568,stroke:#2D3748,stroke-width:2px,color:#fff
    classDef advanced fill:#2C5282,stroke:#1A365D,stroke-width:2px,color:#fff
    classDef final fill:#702459,stroke:#4A1639,stroke-width:2px,color:#fff
    
    class FH start
    class D,W mid
    class PR advanced
    class Q final
```

| Stage | Requirements |
|-------|-------------|
| Facehugger → Drone | **Host:** human |
| Drone → Warrior | **Cost:** 10 Royal Jelly |
| Warrior → Praetorian | **Cost:** 25 Royal Jelly |
| Praetorian → Queen | **Cost:** 50 Royal Jelly |

---

### Runner Pathway (Dog/Beast) ![Runner](img/emojis/runner.png){ width="32" } ![Crusher](img/emojis/crusher.png){ width="32" }

A faster, more agile pathway using animal hosts.

```mermaid
graph LR
    FH[Facehugger] -->|Beast Host| R[Runner]
    R -->|12 Royal Jelly| S[Sentry]
    S -->|30 Royal Jelly| C[Crusher]
    C -->|60 Royal Jelly| Q[Queen]
    
    classDef start fill:#8B4513,stroke:#654321,stroke-width:2px,color:#fff
    classDef mid fill:#CD853F,stroke:#8B4513,stroke-width:2px,color:#fff
    classDef advanced fill:#D2691E,stroke:#8B4513,stroke-width:2px,color:#fff
    classDef final fill:#702459,stroke:#4A1639,stroke-width:2px,color:#fff
    
    class FH start
    class R,S mid
    class C advanced
    class Q final
```

| Stage | Requirements |
|-------|-------------|
| Facehugger → Runner | **Host:** dog, ox, bat, or snake |
| Runner → Sentry | **Cost:** 12 Royal Jelly |
| Sentry → Crusher | **Cost:** 30 Royal Jelly |
| Crusher → Queen | **Cost:** 60 Royal Jelly |

---

### King Pathway (Royal) ![King](img/emojis/king.png){ width="32" } ![Royal Jelly](img/emojis/royal_jelly.png){ width="32" }

The most powerful pathway, creating royal xenomorphs.

```mermaid
graph LR
    KF[King Facehugger] -->|30 RJ + Host| KN[Knight]
    KN -->|50 Royal Jelly| GD[Grand Duke]
    GD -->|75 Royal Jelly| P[Prince]
    P -->|120 Royal Jelly| K[King]
    
    classDef start fill:#8B4513,stroke:#654321,stroke-width:2px,color:#fff
    classDef royal fill:#FFD700,stroke:#DAA520,stroke-width:3px,color:#000
    classDef elite fill:#FFA500,stroke:#FF8C00,stroke-width:3px,color:#000
    classDef king fill:#FF4500,stroke:#DC143C,stroke-width:3px,color:#fff
    
    class KF start
    class KN royal
    class GD elite
    class P,K king
```

| Stage | Requirements |
|-------|-------------|
| King Facehugger → Knight | **Cost:** 30 Royal Jelly<br>**Host:** human, predator, or engineer |
| Knight → Grand Duke | **Cost:** 50 Royal Jelly |
| Grand Duke → Prince | **Cost:** 75 Royal Jelly |
| Prince → King | **Cost:** 120 Royal Jelly |

---

### Deacon Pathway (Engineer) ![Hammerpede](img/emojis/Hammerpede.webp){ width="32" } ![Deacon](img/emojis/deacon.png){ width="32" } ![Engineer](img/emojis/engenieer.png){ width="32" }

A unique pathway creating the powerful Deacon xenomorph.

```mermaid
graph LR
    H[Hammerpede] -->|15 Royal Jelly| T[Trilobite]
    T -->|40 RJ + Engineer| D[Deacon]
    
    classDef proto fill:#4B0082,stroke:#2F0052,stroke-width:2px,color:#fff
    classDef mid fill:#6A0DAD,stroke:#4B0082,stroke-width:2px,color:#fff
    classDef final fill:#8B008B,stroke:#68006B,stroke-width:2px,color:#fff
    
    class H proto
    class T mid
    class D final
```

| Stage | Requirements |
|-------|-------------|
| Hammerpede → Trilobite | **Cost:** 15 Royal Jelly |
| Trilobite → Deacon | **Cost:** 40 Royal Jelly<br>**Host:** engineer |

---

### Neomorph Pathway ![Neomorph](img/emojis/neomorph.png){ width="32" } ![Chestburster](img/emojis/chestburster.png){ width="32" }

A separate evolution line starting from Neomorph eggs.

```mermaid
graph LR
    E[Neomorph Egg] -->|Hatch| BB[Bloodburster]
    BB -->|35 RJ + Human| N[Neomorph]
    
    classDef egg fill:#DC143C,stroke:#8B0000,stroke-width:2px,color:#fff
    classDef burst fill:#FF6347,stroke:#DC143C,stroke-width:2px,color:#fff
    classDef final fill:#B22222,stroke:#8B0000,stroke-width:2px,color:#fff
    
    class E egg
    class BB burst
    class N final
```

| Stage | Requirements |
|-------|-------------|
| Neomorph Egg → Bloodburster | Hatch the egg |
| Bloodburster → Neomorph | **Cost:** 35 Royal Jelly<br>**Host:** human |

---

## Special Pathways

### Predalien Pathway ![Predalien](img/emojis/predalien.png){ width="32" } ![Predator](img/emojis/predator.png){ width="32" }

The hybrid xenomorph-predator evolution path, combining traits from both species.

```mermaid
graph LR
    PE[Predalien Egg] -->|Predator Host| PF[Predalien Facehugger]
    PF -->|Emerge| HB[Hybrid Chestburster]
    HB -->|35 Royal Jelly| PD[Predalien Drone]
    PD -->|45 Royal Jelly| PW[Predalien Warrior]
    PW -->|60 Royal Jelly| PB[Predalien Brute]
    
    classDef start fill:#8B4513,stroke:#654321,stroke-width:2px,color:#fff
    classDef hybrid fill:#5C4033,stroke:#3E2723,stroke-width:2px,color:#fff
    classDef advanced fill:#7D4E24,stroke:#5C3317,stroke-width:2px,color:#fff
    classDef elite fill:#9C5E31,stroke:#7D4E24,stroke-width:2px,color:#fff
    
    class PE start
    class PF,HB hybrid
    class PD,PW advanced
    class PB elite
```

| Stage | Requirements |
|-------|-------------|
| Predalien Egg → Predalien Facehugger | **Host:** predator (obtained through hunts) |
| Predalien Facehugger → Hybrid Chestburster | Automatic emergence |
| Hybrid Chestburster → Predalien Drone | **Cost:** 35 Royal Jelly |
| Predalien Drone → Predalien Warrior | **Cost:** 45 Royal Jelly |
| Predalien Warrior → Predalien Brute | **Cost:** 60 Royal Jelly |

---

### Spitter Pathway (Toxic) ![Black Goo](img/emojis/black_goo.png){ width="32" } ![Warrior](img/emojis/warrior.png){ width="32" }

Xenomorphs with potent acid-spitting abilities from toxic-exposed hosts.

```mermaid
graph LR
    CE[Classic Egg] -->|Toxic Host| FH[Facehugger]
    FH -->|Emerge| TC[Toxic Chestburster]
    TC -->|15 Royal Jelly| SD[Spitter Drone]
    SD -->|35 Royal Jelly| SW[Spitter Warrior]
    
    classDef start fill:#8B4513,stroke:#654321,stroke-width:2px,color:#fff
    classDef toxic fill:#228B22,stroke:#006400,stroke-width:2px,color:#fff
    classDef advanced fill:#32CD32,stroke:#228B22,stroke-width:2px,color:#000
    
    class CE start
    class FH,TC toxic
    class SD,SW advanced
```

| Stage | Requirements |
|-------|-------------|
| Classic Egg → Facehugger | **Host:** toxic-exposed human |
| Facehugger → Toxic Chestburster | Automatic emergence |
| Toxic Chestburster → Spitter Drone | **Cost:** 15 Royal Jelly |
| Spitter Drone → Spitter Warrior | **Cost:** 35 Royal Jelly |

---

### Prowler Pathway (Agile) ![Runner](img/emojis/runner.png){ width="32" }

Highly agile xenomorphs from feline or avian hosts, specialized for stealth.

```mermaid
graph LR
    CE[Classic Egg] -->|Agile Host| FH[Facehugger]
    FH -->|Emerge| MC[Micro Chestburster]
    MC -->|12 Royal Jelly| PD[Prowler Drone]
    PD -->|28 Royal Jelly| PA[Prowling Assassin]
    
    classDef start fill:#8B4513,stroke:#654321,stroke-width:2px,color:#fff
    classDef agile fill:#483D8B,stroke:#2F2F6F,stroke-width:2px,color:#fff
    classDef stealth fill:#6A5ACD,stroke:#483D8B,stroke-width:2px,color:#fff
    
    class CE start
    class FH,MC agile
    class PD,PA stealth
```

| Stage | Requirements |
|-------|-------------|
| Classic Egg → Facehugger | **Host:** feline or birdlike |
| Facehugger → Micro Chestburster | Automatic emergence |
| Micro Chestburster → Prowler Drone | **Cost:** 12 Royal Jelly |
| Prowler Drone → Prowling Assassin | **Cost:** 28 Royal Jelly |

---

### Protomorph Pathway (Self-Evolving) ![Xenomorph](img/emojis/xenomorph_sprite.png){ width="32" }

Ancient xenomorph variant that evolves without a host - self-contained evolution.

```mermaid
graph LR
    PE[Proto Egg] -->|Self-Evolve| PW[Protomorph Warrior]
    PW -->|40 Royal Jelly| EP[Elder Protomorph]
    
    classDef proto fill:#1A1A2E,stroke:#0F0F1E,stroke-width:2px,color:#fff
    classDef ancient fill:#16213E,stroke:#0F3460,stroke-width:2px,color:#fff
    
    class PE proto
    class PW,EP ancient
```

| Stage | Requirements |
|-------|-------------|
| Proto Egg → Protomorph Warrior | **No host required** - self-evolves |
| Protomorph Warrior → Elder Protomorph | **Cost:** 40 Royal Jelly |

**Special Note:** This pathway is unique - the Proto Egg does not need a host and evolves independently.

---

### Jockey Pathway (Engineer) ![Engineer](img/emojis/engenieer.png){ width="32" } ![USSM](img/emojis/USSM.png){ width="32" }

Elite xenomorphs from the rare Space Jockey eggs and engineer hosts.

```mermaid
graph LR
    SJ[Space Jockey Egg] -->|Engineer Host| FH[Facehugger]
    FH -->|Emerge| CB[Chestburster]
    CB -->|40 Royal Jelly| JD[Jockey Drone]
    JD -->|65 Royal Jelly| JS[Jockey Sentinel]
    
    classDef jockey fill:#2C3E50,stroke:#1A252F,stroke-width:2px,color:#fff
    classDef elite fill:#34495E,stroke:#2C3E50,stroke-width:2px,color:#fff
    classDef sentinel fill:#5D6D7E,stroke:#34495E,stroke-width:2px,color:#fff
    
    class SJ jockey
    class FH,CB elite
    class JD,JS sentinel
```

| Stage | Requirements |
|-------|-------------|
| Space Jockey Egg → Facehugger | **Host:** engineer (rare event capture) |
| Facehugger → Chestburster | Automatic emergence |
| Chestburster → Jockey Drone | **Cost:** 40 Royal Jelly |
| Jockey Drone → Jockey Sentinel | **Cost:** 65 Royal Jelly |

**Special Note:** Engineer hosts are extremely rare and obtained through special capture events.

---

### Irradiated Pathway ![Atom](img/emojis/atom.png){ width="32" } ![Xenomorph](img/emojis/Xenomorph.png){ width="32" }

Radioactive xenomorphs from radiation-exposed hosts with unique glowing properties.

```mermaid
graph LR
    IE[Irradiated Egg] -->|Rad-Exposed Host| FH[Facehugger]
    FH -->|Emerge| GB[Glowing Burster]
    GB -->|20 Royal Jelly| ID[Irradiated Drone]
    ID -->|40 Royal Jelly| IW[Irradiated Warrior]
    
    classDef rad fill:#39FF14,stroke:#32CD32,stroke-width:2px,color:#000
    classDef glow fill:#00FF00,stroke:#39FF14,stroke-width:2px,color:#000
    classDef radioactive fill:#7FFF00,stroke:#00FF00,stroke-width:2px,color:#000
    
    class IE rad
    class FH,GB glow
    class ID,IW radioactive
```

| Stage | Requirements |
|-------|-------------|
| Irradiated Egg → Facehugger | **Host:** radiation-exposed human |
| Facehugger → Glowing Burster | Automatic emergence |
| Glowing Burster → Irradiated Drone | **Cost:** 20 Royal Jelly |
| Irradiated Drone → Irradiated Warrior | **Cost:** 40 Royal Jelly |

---

### Berserker Pathway ![Warrior](img/emojis/warrior.png){ width="32" } ![Crusher](img/emojis/crusher.png){ width="32" }

Powerful brute-force xenomorphs from large bear-like hosts.

```mermaid
graph LR
    BE[Berserker Egg] -->|Large Host| FH[Facehugger]
    FH -->|Emerge| BB[Burster]
    BB -->|25 Royal Jelly| BD[Berserker Drone]
    BD -->|45 Royal Jelly| BW[Berserker Warrior]
    
    classDef start fill:#8B4513,stroke:#654321,stroke-width:2px,color:#fff
    classDef brute fill:#8B0000,stroke:#5C0000,stroke-width:2px,color:#fff
    classDef berserker fill:#DC143C,stroke:#8B0000,stroke-width:2px,color:#fff
    
    class BE start
    class FH,BB brute
    class BD,BW berserker
```

| Stage | Requirements |
|-------|-------------|
| Berserker Egg → Facehugger | **Host:** bear-like (large creature) |
| Facehugger → Burster | Automatic emergence |
| Burster → Berserker Drone | **Cost:** 25 Royal Jelly |
| Berserker Drone → Berserker Warrior | **Cost:** 45 Royal Jelly |

---

## Host Types

Different hosts produce different xenomorph variants:

| Host Type | Produces | Used In |
|-----------|----------|---------|
| **Human** | Drone, Neomorph | Standard, King, Neomorph pathways |
| **Dog/Ox/Bat/Snake** | Runner | Runner pathway |
| **Predator** | Predalien | King pathway, Predalien pathway |
| **Engineer** | Deacon, Jockey | King, Deacon, Jockey pathways |
| **Toxic** | Spitter | Spitter pathway |
| **Feline/Bird** | Prowler | Prowler pathway |
| **Radiation-Exposed** | Irradiated | Irradiated pathway |
| **Bear-like (Large)** | Berserker | Berserker pathway |

---

## Tips

!!! tip "Resource Management"
    Royal Jelly is essential for evolution. Plan your evolution path carefully based on available resources.

!!! info "Host Rarity"
    Some hosts like Engineers and Predators are rare. Save special eggs until you have the appropriate host available.

!!! warning "Special Requirements"
    Some pathways have unique requirements - the Protomorph pathway doesn't need a host, while the Jockey pathway requires rare event captures.

!!! tip "More Information"
    For specific stat changes and abilities at each stage, see the [Encyclopedia command](Commands/Collection.md#encyclopedia).
