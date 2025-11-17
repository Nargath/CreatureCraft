# Tag System Framework
*Universal mechanical framework for creature components across all subsystems*

---

## Purpose of This Document

This document defines the **MECHANICAL RULES** that govern how tags work across all subsystems. For design philosophy, rationales, and guiding principles, see the Design Philosophy document.

---

## Core Mechanical Rules

### Rule 1: Tag Level Equals Creature CR

**Specification:** All special tags on a creature are set to the creature's Challenge Rating.

**Examples:**
- CR 8 Red Dragon Ã¢â€ ' [Fire 8], [Flight 8], [Defense 8], [Sharp 8]
- CR 15 Ancient Dragon Ã¢â€ ' [Fire 15], [Flight 15], [Defense 15], [Sharp 15]
- CR 3 Goblin Ã¢â€ ' [Sharp 3], [Defense 3]

**Result:** Uniform scaling across all creature features. No individual power level calculations required.

---

### Rule 2: Single Tag Per Component

**Specification:** Each harvested component has exactly one special tag.

**Examples:**
- Dragon Teeth Ã¢â€ ' [Sharp 15] only
- Dragon Fire Glands Ã¢â€ ' [Fire 15] only
- Dragon Scales Ã¢â€ ' [Defense 15] only

**Result:** Variety comes from different components, not multiple tags per component. Simplifies tracking and prevents stacking issues.

---

### Rule 3: Universal DC Formula

**Specification:** All subsystems use the same difficulty class calculation.

**Formula:** DC = 14 + Tag Level + Difficulty Modifier

**Components:**
- **14:** PF2e standard DC baseline
- **Tag Level:** Creature's Challenge Rating (automatic scaling)
- **Difficulty Modifier:** Task-specific adjustment

**Difficulty Modifiers:**
- **Normal:** +0
- **Hard:** +2
- **Very Hard:** +5
- **Incredibly Hard:** +10

**Modifier Sources:**
- **HinderCraft & HarvestCraft:** Determined by creature properties (e.g., ancient dragon = Very Hard = +5)
- **CookCraft & ForgeCraft:** Determined by recipe/enhancement complexity

**Examples:**
- Hellhound [Fire 3]: Base DC 17, Normal task DC 17, Hard task DC 19
- Ancient Dragon [Fire 17]: Base DC 31, Very Hard task DC 36

---

## Tag Categories

### Special Tags (Leveled)

**Definition:** Represent extraordinary creature abilities with power scaling. Level equals creature CR.

**Characteristics:**
- Level determines DC and effect potency/duration
- Used across multiple subsystems (HinderCraft, HarvestCraft, CookCraft, ForgeCraft)
- Provide enhanced capabilities and magical effects

**Tag Format:** [TagName X] where X = Creature CR

**Examples:**
- [Fire 12] - Fire-based component from CR 12 creature
- [Venom 5] - Venom from CR 5 creature
- [Sharp 20] - Natural weapon from CR 20 creature

**Complete Special Tags List:**
See special_tags_list.md for comprehensive list of all 39 special tags.

---

### Mundane Tags (Unleveled)

**Definition:** Represent basic biological materials for survival and standard crafting. No level scaling.

**Characteristics:**
- No level value (quantity determined by creature size, not CR)
- Support survival gameplay and economic activities
- Functionality tracked by tag presence/absence

**Tag Format:** [TagName] (no level number)

**Standard Mundane Tags:**
- [Meat] - Protein sources, cooking ingredients
- [Hide] - Leather goods, basic armor materials
- [Bone] - Tools, structural materials
- [Fat] - Cooking oils, weatherproofing, lubricants
- [Organs] - Specialized internal organs
- [Blood] - Non-magical blood for various applications
- [Scale] - Non-magical scales and protective plates
- [Feather] - Flight feathers and down (mundane varieties)
- [Fur] - Pelts and fur materials
- [Sinew] - Tendons and binding materials

---

## Mundane Material Yield System

### Quantity Scaling by Creature Size

**Formula:** Base Yield Ãƒâ€” Size Multiplier

**Size Multipliers:**
- **Tiny:** 0.1Ãƒâ€”
- **Small:** 0.5Ãƒâ€”
- **Medium:** 1Ãƒâ€” (baseline)
- **Large:** 3Ãƒâ€”
- **Huge:** 5Ãƒâ€”
- **Gargantuan:** 10Ãƒâ€”

**Example - Dragon Meat:**
- Medium creature: 2 Bulk meat
- Gargantuan dragon: 20 Bulk meat (2 Ãƒâ€” 10)

**Key Principle:** Volume scales with size, not quality. A Tiny wolf and a Gargantuan wolf both provide [Meat] with identical functionality - just different quantities.

---

### Condition and Spoilage System

**Condition States:**
- **Fresh:** Full functionality, all tags present
- **Preserved:** Extended shelf life, maintains tags
- **Spoiled:** Non-functional, tags lost

**Mechanical Rule:** Tag presence determines functionality. Condition descriptors are narrative.

**Examples:**
- "Fresh Dragon Meat [Meat]" Ã¢â€ ' Functional for cooking
- "Preserved Dragon Meat [Meat]" Ã¢â€ ' Functional for cooking
- "Spoiled Dragon Meat" (no [Meat] tag) Ã¢â€ ' Unusable in recipes

**Spoilage Timing:**
Determined by GM based on climate, storage, and preservation methods. Standard fantasy adventuring assumption: special components last 1 week, mundane materials last 3 days without preservation.

---

## Tag Data Structure

Each tag contains standardized data that all subsystems can reference independently:

### Special Tag Data Categories

**HinderCraft Data:**
- Conditions applied by Target Area attacks
- Save type (Fortitude/Reflex/Will)
- Critical hit conditions

**HarvestCraft Data:**
- Component yield types available
- Extraction difficulty modifiers
- Special harvesting requirements
- Spoilage rules specific to tag type

**CookCraft Data:**
- Sustenance category effects
- Enhancement category effects
- Utility category effects
- Duration calculation (base time Ãƒâ€” tag level)

**ForgeCraft Data:**
- Expression path options (Destruction/Protection/Utility/Magic)
- Tier effects based on tag level ranges
- Material properties and compatibility
- Enhancement scaling rules

**Economic Data:**
- Base value calculations
- Rarity modifiers by tag level
- Trade factors and market demand

---

### Mundane Tag Data Categories

**Functionality:**
- Primary uses and applications
- Crafting compatibility
- Cooking applications

**Yield Scaling:**
- Base yield amounts
- Size multiplier application
- Bulk measurements

**Condition Tracking:**
- Fresh/Preserved/Spoiled state rules
- Preservation methods available
- Tag retention conditions

**Spoilage Rules:**
- Time until spoilage (unpreserved)
- Environmental factors affecting decay
- When tags are permanently lost

---

## Subsystem Integration Specifications

### Interface Principles

**Independent Data Access:**
Each subsystem reads tag data without requiring other subsystems:
- HinderCraft reads combat conditions and save types
- HarvestCraft reads yield quantities and extraction requirements
- CookCraft reads consumable effects and duration formulas
- ForgeCraft reads material properties and enhancement options

**No Cross-Dependencies:**
Subsystems don't call each other's mechanics. They only share the universal tag data structure.

**Example - [Fire 12] Component:**
- **HinderCraft:** Reads "Fort save, conditions: Flat-Footed/Sickened"
- **HarvestCraft:** Reads "Yield: 1-2 fire glands, DC +2 for heat danger"
- **CookCraft:** Reads "Sustenance: Fire resistance 5, Duration: 1h Ãƒâ€” 12 = 12 hours"
- **ForgeCraft:** Reads "Available paths: Destruction/Protection/Utility/Magic, Tier 3 effects"

**Result:** Each subsystem functions independently while maintaining consistency.

---

### Data Consistency Rules

**Tag Level Determines Scaling:**
- [Fire 8] provides consistent baseline power regardless of subsystem context
- Individual subsystems apply their own difficulty modifiers on top of base DC
- Effect potency, duration, and value all scale predictably with tag level

**Scaling Patterns by Subsystem:**
- **HinderCraft:** Tag level determines DC only (no power scaling)
- **HarvestCraft:** Tag level determines DC only (no yield scaling)
- **CookCraft:** Tag level determines duration/uses (fixed effect power)
- **ForgeCraft:** Tag level determines tier access (grouped power scaling)

**Universal Baseline:**
All subsystems agree that [Fire 12] is more valuable than [Fire 5], but each interprets that value differently according to its purpose.

---

## GM Implementation Guidelines

### Tag Assignment Process

**Step 1: Identify Creature Features**
Review creature's significant abilities:
- Breath weapons, special attacks
- Natural weapons (claws, teeth, stingers)
- Special movement modes
- Sensory capabilities
- Defensive features

**Step 2: Assign Tag Types**
Match features to appropriate tags:
- Elemental attacks Ã¢â€ ' Corresponding elemental tags
- Toxins/venoms Ã¢â€ ' [Venom]
- Natural weapons Ã¢â€ ' [Sharp]
- Armor/shells Ã¢â€ ' [Defense]
- Flight/burrow/swim Ã¢â€ ' Movement tags
- Enhanced senses Ã¢â€ ' [Vision], [Scent], [Sense]

**Step 3: Set All Tags to Creature CR**
All special tags = Creature's Challenge Rating (no exceptions)

**Step 4: Determine Difficulty Modifiers**
Assess task complexity based on creature properties:
- **Ancient dragons, unique creatures:** Very Hard (+5)
- **Elite monsters, dangerous features:** Hard (+2)
- **Standard creatures:** Normal (+0)

**Step 5: Identify Mundane Materials**
Determine which unleveled tags apply:
- Living creatures Ã¢â€ ' [Meat], [Hide], [Bone], [Blood]
- Furry creatures Ã¢â€ ' [Fur]
- Scaled creatures Ã¢â€ ' [Scale]
- Flying creatures Ã¢â€ ' [Feather]
- Special organs Ã¢â€ ' [Organs]

---

### Creature Variety Through Components

**Multiple Components, Single Tag Each:**
A single creature provides multiple tag types through different body parts, but each component has exactly one tag.

**Example - Ancient Red Dragon (CR 17):**
- Fire Breath Glands Ã¢â€ ' [Fire 17]
- Teeth and Claws Ã¢â€ ' [Sharp 17]
- Armored Scales Ã¢â€ ' [Defense 17]
- Wing Membranes Ã¢â€ ' [Flight 17]
- Enhanced Eyes Ã¢â€ ' [Vision 17] or [Sense 17]
- Arcane Heart Ã¢â€ ' [Magical 17]
- Mundane materials: [Meat], [Hide], [Bone], [Blood], [Scale]

**Result:** Rich variety without complex tag combinations.

---

## Player Usage Guidelines

### Inventory Tracking Options

Players choose how to track components:

**Option 1 - Specific Tracking:**
- "Ancient Dragon Teeth [Sharp 17]"
- "Wyvern Venom Sac [Venom 12]"
- Provides narrative satisfaction and thematic collections

**Option 2 - Generic Tracking:**
- "[Sharp 17] Components x3"
- "[Venom 12] Components x2"
- Streamlined for practical players

**Option 3 - Mixed Approach:**
- Specific names for themed collections or special projects
- Generic tracking for bulk materials
- "Ancient Dragon Teeth [Sharp 17]" for planned sword project
- "[Fire 8] Components x4" for general use

**System Result:** All three approaches work identically in mechanics. Player choice is purely organizational.

---

### Material Functionality Rules

**Identical Tag Level = Identical Function:**
All components with the same tag and level work identically in all subsystems:
- [Fire 12] dragon glands = [Fire 12] elemental core (mechanically)
- [Sharp 8] owlbear claws = [Sharp 8] razor beetle mandibles (mechanically)

**Tag Presence Determines Usability:**
- Component with tag Ã¢â€ ' Functional in all systems
- Spoiled component (no tag) Ã¢â€ ' Unusable
- Preserved component (tag retained) Ã¢â€ ' Fully functional

**Higher Tag Levels:**
- Provide access to higher effect tiers (ForgeCraft)
- Provide longer durations (CookCraft)
- Require higher skill checks (all systems)
- May have higher economic value

---

## System in Practice

### Complete Example: Ancient Red Dragon (CR 17)

**Special Components Available:**
| Component | Tag | Base DC |
|-----------|-----|---------|
| Fire Glands | [Fire 17] | 31 |
| Teeth/Claws | [Sharp 17] | 31 |
| Enhanced Eyes | [Vision 17] | 31 |
| Wing Membranes | [Flight 17] | 31 |
| Armored Scales | [Defense 17] | 31 |
| Arcane Heart | [Magical 17] | 31 |

**Mundane Materials Available:**
| Material | Tag | Yield (Gargantuan) |
|----------|-----|--------------------|
| Meat | [Meat] | 40 Bulk |
| Hide | [Hide] | 25 Bulk |
| Scales | [Scale] | 30 Bulk |
| Bones | [Bone] | 20 Bulk |
| Blood | [Blood] | 15 Bulk |

---

### Material Flow Example

**Step 1 - Collection (HarvestCraft):**
Player harvests "Ancient Dragon Teeth [Sharp 17]"
- Base DC: 31 (14 + 17)
- Creature modifier: Very Hard (+5)
- Final DC: 36
- Success: Gain 1 component

**Step 2 - Processing Decision:**
Player decides to use component for permanent crafting (ForgeCraft)
- Alternative: Could cook for temporary combat benefit (CookCraft)
- Strategic choice: Permanent value vs immediate utility

**Step 3 - Crafting Application (ForgeCraft):**
Create enhanced longsword using Destruction expression path
- Component: [Sharp 17]
- Base item: +1 Longsword (Level 4)
- Expression: Destruction path
- Tag level 17 = Tier 4 access
- Item level 4 < Tier 4 requirement (Level 13+)
- **Limited to Tier 2 effect:** +2 status bonus to damage
- Base DC: 31 (14 + 17)
- Complexity: Normal (+0)
- Final DC: 31
- Time: 17 days

**Step 4 - System Result:**
- Tag level drove base DC (31)
- Item level limitation prevented overpowered combination
- Component name provided narrative satisfaction
- Mechanical consistency maintained throughout

---

### Cross-Subsystem Usage Patterns

**Same Component, Different Subsystems:**

**[Fire 12] Component Usage Options:**

**HinderCraft (Combat):**
- Target: Breath gland or fire-generating organ
- DC: 26 (14 + 12 + 0 Normal)
- Save: Fortitude
- Effect: Flat-Footed or Sickened 1

**HarvestCraft (Collection):**
- Target: Fire glands, thermal organs
- DC: 28 (14 + 12 + 2 Hard extraction)
- Result: 1-2 [Fire 12] components
- Risk: 1d6 fire damage on failure

**CookCraft (Temporary Boost):**
- Sustenance: Fire resistance 5 for 12 hours
- Enhancement: +2 Reflex saves for 6 hours
- Utility: Ignite capability for 6 hours
- DC: 26 (14 + 12)

**ForgeCraft (Permanent Item):**
- Destruction: +1d6 fire damage (Tier 3)
- Protection: Fire resistance 8 (Tier 3)
- Utility: Heat/ignition abilities (Tier 3)
- Magic: Fire spell capabilities (Tier 3)
- DC: 26+ (14 + 12 + complexity modifier)
- Time: 12 days

**Result:** Same component provides value across all subsystems. Player choice determines which benefit to pursue.

---

## Technical Specifications Summary

### Quick Reference - Universal Rules

**DC Calculation:** 14 + Tag Level + Difficulty Modifier

**Tag Level:** Always equals Creature CR

**Single Tag Rule:** One tag per component

**Difficulty Modifiers:** Normal (+0), Hard (+2), Very Hard (+5), Incredibly Hard (+10)

**Mundane Yield:** Base Yield Ãƒâ€” Size Multiplier

**Size Multipliers:** Tiny (0.1Ãƒâ€”), Small (0.5Ãƒâ€”), Medium (1Ãƒâ€”), Large (3Ãƒâ€”), Huge (5Ãƒâ€”), Gargantuan (10Ãƒâ€”)

**Spoilage Rule:** Tag presence determines functionality

**Component Equivalence:** Same tag + same level = identical function

---

### Quick Reference - Tag Categories

**Special Tags:** Leveled, format [TagName X], X = Creature CR

**Mundane Tags:** Unleveled, format [TagName], quantity by size

**Special Tag Count:** 39 total (see special_tags_list.md)

**Mundane Tag Count:** 10 standard tags (expandable)

---

### Quick Reference - Subsystem Scaling

**HinderCraft:** Tag level Ã¢â€ ' DC only

**HarvestCraft:** Tag level Ã¢â€ ' DC only

**CookCraft:** Tag level Ã¢â€ ' Duration/uses (fixed power)

**ForgeCraft:** Tag level Ã¢â€ ' Tier access (grouped power)

---

## Integration with PF2e Rules

### Bonus Type Usage

**Item Bonuses:** Used by permanent enhancements (ForgeCraft weapons/armor)

**Circumstance Bonuses:** Used by situational benefits (CookCraft Enhancement, ForgeCraft Protection)

**Status Bonuses:** Used by internal buffs (CookCraft Enhancement, ForgeCraft Destruction)

**Untyped Bonuses:** Avoided (maintain PF2e stacking rules)

**Result:** All bonuses stack appropriately per PF2e rules.

---

### Time Scale Standards

**Combat Time:**
- Rounds (6 seconds)
- Used by: HinderCraft duration, some ForgeCraft combat effects

**Exploration Time:**
- Minutes (60 seconds)
- Hours (60 minutes)
- Used by: HarvestCraft extraction, CookCraft preparation

**Downtime Time:**
- Days (24 hours)
- Weeks (7 days)
- Used by: ForgeCraft crafting, preservation periods

**Result:** Consistent with PF2e time scales.

---

### Action Economy Integration

**HinderCraft:**
- Target Area: 2 actions (attack)
- Hinder Area: Free action (triggered)

**HarvestCraft:**
- Standard Harvesting: Exploration activity (10 minutes)
- Combat Harvesting: 2 actions

**CookCraft:**
- Field Cooking: 30 minutes (exploration)
- Camp Cooking: 1 hour (downtime)

**ForgeCraft:**
- Crafting: Days (downtime activity)

**Result:** Each subsystem respects appropriate action economy for its context.

---

## Conclusion

This document provides the mechanical specifications that govern tag behavior across all subsystems. For design rationale, guiding principles, and development philosophy, refer to the Design Philosophy document.

**Key Takeaway:** These rules create a universal language that allows independent subsystems to integrate seamlessly while maintaining their own mechanical identity and design goals.

---

*For philosophical guidance and development principles, see the Design Philosophy document.*
*For specific subsystem implementations, see individual subsystem documents.*
*For comprehensive tag listing, see special_tags_list.md.*