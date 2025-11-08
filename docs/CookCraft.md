---
title: CookCraft SubSystem
date: "{{ git_revision_date_localized }}"
---

# CookCraft Subsystem
*Creature Component Cuisine*

---

## What Is CookCraft?

CookCraft transforms harvested creature components into temporary consumables. Unlike permanent crafting or complex alchemy, CookCraft provides short-term benefits that support adventure activities through simple cooking mechanics.

**Key Benefits:**
- Convert creature materials into beneficial consumables
- Recipe categories determine how tag powers manifest
- Support party with tactical and survival benefits
- Create economic value from harvested materials

**No Recipe Requirements:**
Anyone can cook creature components - there are no recipes to learn or discover. The knowledge is simply choosing which category effect you want from your component. A [Fire] component can provide warmth (Sustenance), protection (Enhancement), offense (Combat), or healing (Curative) based on how you prepare it.

---

## Core Mechanics

### Basic Process
1. **Choose Recipe:** Select category and food form
2. **Gather Components:** One special + appropriate mundane components
3. **Make Check:** Roll Survival or Crafting vs DC
4. **Cook Time:** 30 minutes (field) or 1 hour (camp)
5. **Results:** Create consumables based on success

### Difficulty Class
**DC = 14 + Tag Level**
- **Tag Level:** From the special component used (0 for mundane-only)
- **Batch Cooking:** +2 DC per additional serving beyond the first

### Skills
**Choose based on approach:**
- **Survival:** Traditional cooking, field preparation, natural methods
- **Crafting:** Technical precision, equipment usage, refined techniques

### Degrees of Success
**Critical Success:** Create 2 servings
**Success:** Create 1 serving
**Failure:** Components consumed, no result
**Critical Failure:** Components destroyed + Sickened 1 for 1 hour

---

## Duration and Effect Scaling

### Core Principle
**Effect magnitude is fixed by recipe category.** Higher tag levels provide longer duration, not stronger effects.

### Duration by Category
**Base duration multiplied by tag level:**
- **Sustenance:** 1 hour Ã— tag level (max 24 hours)
- **Enhancement:** 10 minutes Ã— tag level (max 3 hours)
- **Combat:** 1 round Ã— tag level (max 5 rounds)
- **Curative:** Instant (tag level determines what it can affect)

### Examples
**[Fire 5] Enhancement:** Fire Resistance 5 for 50 minutes
**[Fire 12] Enhancement:** Fire Resistance 5 for 120 minutes
**[Venom 8] Curative:** Can remove poisons up to level 8

---

## How CookCraft Works

### The Simple Truth
**[Special Component] + [Mundane Components] + [Category] = Effect**

There are no complex recipes to learn. If you have a [Fire] component and some meat, you can cook it. The category you choose (Combat, Enhancement, Sustenance, Curative) determines what benefit you get from that [Fire] essence.

### Core Rules

**One Component, One Effect:**
- Each recipe uses ONE special component
- Adding more special components doesn't enhance the effect
- Save extra components for additional meals

### Batch Cooking by Category

**Combat Recipes:** 
- Always single-serving
- Quick consumption, brief effect (max 5 rounds)
- Perfect for using low-level components

**Enhancement/Sustenance Recipes:**
- Can split duration among multiple servings
- Example: [Fire 12] Enhancement = 120 min solo OR 40 min for 3 people
- DC increases by +2 per additional serving

**Curative Recipes:**
- Instant effect, typically single-serving
- Tag level determines what it can cure/remove

### What Doesn't Work
- [Fire 5] + [Fire 5] â‰  [Fire 10] effect
- [Fire 5] + [Sharp 3] â‰  both effects at once
- Multiple components don't stack or enhance

---

## Recipe Categories

Recipe categories are simply different ways to prepare components. The same [Fire] component can be cooked four different ways, each extracting a different benefit from its essence:

### Sustenance
*Slow-cooked for lasting nourishment*

**Tag Interpretations (Fixed Effects):**
- **[Fire]** â†’ Cold resistance 5
- **[Venom]** â†’ Disease resistance 5
- **[Sharp]** â†’ Reduce ration consumption by half
- **[Sensory]** â†’ +2 item bonus to Perception during rest/watch
- **[Mundane]** â†’ Basic nutrition and fatigue removal

**Duration:** 1 hour Ã— tag level (max 24 hours)
**Example:** [Fire 5] Sustenance = Cold resistance 5 for 5 hours

### Enhancement  
*Prepared to boost abilities*

**Tag Interpretations (Fixed Effects):**
- **[Fire]** â†’ Fire resistance 5
- **[Venom]** â†’ Poison resistance 5
- **[Sharp]** â†’ +1 item bonus to attack rolls
- **[Sensory]** â†’ +2 item bonus to Perception
- **[Flight]** â†’ +10 foot movement speed
- **[Magical]** â†’ +1 item bonus to spell DCs

**Duration:** 10 minutes Ã— tag level (max 3 hours)
**Example:** [Sharp 8] Enhancement = +1 to attacks for 80 minutes

### Combat
*Quick-fired for immediate offense*

**Tag Interpretations (Fixed Effects):**
- **[Fire]** â†’ +1d6 fire damage to strikes
- **[Venom]** â†’ Strikes inflict Sickened 1 on critical hit
- **[Sharp]** â†’ Strikes inflict Bleed 1
- **[Sensory]** â†’ Gain See Invisibility effect
- **[Flight]** â†’ Ignore difficult terrain
- **[Magical]** â†’ Strikes count as magical

**Duration:** 1 round Ã— tag level (max 5 rounds)
**Example:** [Fire 5] Combat = +1d6 fire damage for 5 rounds

### Curative
*Distilled for healing properties*

**Tag Interpretations (Fixed Effects):**
- **[Fire]** â†’ Remove disease (up to tag level)
- **[Venom]** â†’ Remove poison (up to tag level)
- **[Sharp]** â†’ Remove bleed and heal 2d8 HP
- **[Sensory]** â†’ Remove confusion, stupefied, or dazzled
- **[Magical]** â†’ Remove curse (up to tag level)
- **[Mundane]** â†’ Restore 1d4 HP, remove fatigued

**Duration:** Instant (tag level determines maximum condition level affected)
**Example:** [Venom 7] Curative = Remove poison effects up to level 7

---

## Component Requirements

### The Basic Formula
**Every recipe = [Special Component] + [Mundane Components] + [Category Choice]**
- Special component provides the tagged power
- Mundane components make it edible food
- Category choice determines how the power manifests

### Special Components
- **One per recipe:** Each recipe uses exactly ONE special component
- **No stacking:** Additional components don't enhance effects
- **Batch cooking:** Enhancement/Sustenance can split duration among servings
- **Combat restriction:** Combat recipes are always single-serving
- **Tag mixing:** Cannot mix different special tag types in one recipe

### Mundane Components & Food Forms
The mundane components you use determine what type of food you make. All forms provide the same mechanical effect but create different narrative experiences:

**Stew/Soup:** [Meat] + [Fat] + [Bone] or [Organs]
- Natural choice for batch cooking
- Camp cooking only (needs pot and time)

**Roast/Grilled:** [Meat] + [Fat]
- Simple and reliable
- Can be field-cooked

**Jerky/Preserved:** [Meat] only
- Takes longer to prepare
- Travels well, good for Sustenance

**Broth/Tonic:** [Bone] + [Organs] or [Blood]
- Light and quick to consume
- Natural fit for Curative category

**Pie/Pastry:** [Meat] + [Fat] + trade goods (flour, etc.)
- Requires civilization supplies
- Impressive for social situations

### Batch Cooking Requirements
- Add 1 mundane component per extra serving
- Example: Stew for 3 people needs 3Ã— the mundane components

---

## Time and Equipment

### Cooking Time
**Field Cooking:** 30 minutes
- Quick preparations over open flame
- Limited to simpler food forms (roasts, jerky)
- Requires portable cooking kit

**Camp Cooking:** 1 hour
- Full meal preparation with proper setup
- Enables all food forms (stews, soups, pies)
- Better for batch cooking

### Equipment
**Portable Cooking Kit** (5 gp, 3 Bulk)
- Basic pots, utensils, portable heat source
- No penalty to checks
- Enables field cooking

**Professional Cooking Tools** (25 gp, 5 Bulk)
- Quality cookware, precision utensils, spices
- +1 item bonus to CookCraft checks
- Makes field cooking more versatile

### Food Form Limitations
Some food forms require specific conditions:
- **Stews/Soups:** Need camp setup and proper pots
- **Pies/Pastries:** Require trade goods (flour, etc.)
- **Jerky:** Takes longer but can be done while traveling
- **Roasts:** Can be field-cooked with basic equipment

---

## Effect Guidelines

### Fixed Effect Magnitudes
Effects are determined by recipe category, NOT tag level:
- All [Fire] Enhancement recipes give Fire Resistance 5
- All [Sharp] Combat recipes give +1d6 damage
- Higher tag levels provide longer duration, not stronger effects

### Stacking Rules
- Same recipe type doesn't stack (higher bonus applies)
- Different categories stack normally (Enhancement + Combat + Sustenance)
- Cannot consume same recipe until duration expires
- All effects provide item bonuses (following PF2e item bonus rules)

---

## Example Recipes

*Note: Recipe names are purely narrative. "Drake Fire Roast" is mechanically identical to "Goblin Fire Stew" if both use [Fire] components of the same level.*

### Wolf Pack Jerky
**Category:** Sustenance
**Food Form:** Jerky ([Meat] only)
**Components:** [Meat] x1
**DC:** 14 (no special component)
**Effect:** Removes fatigued, provides 8 hours satiation
**Note:** Simple trail food using only mundane ingredients

### Drake Fire Roast
**Category:** Enhancement  
**Food Form:** Roast ([Meat] + [Fat])
**Components:** [Fire 7] + drake [Meat] + drake [Fat]
**DC:** 21 (14 + 7)
**Effect:** Fire resistance 5 for 70 minutes

### Owlbear Battle Stew
**Category:** Combat
**Food Form:** Quick stew ([Meat] + [Organs])
**Components:** [Sharp 5] + owlbear [Meat] + owlbear [Organs]
**DC:** 19 (14 + 5)
**Effect:** +1d6 damage and Bleed 1 on strikes for 5 rounds
**Note:** Single serving only (Combat recipes don't batch)

### Basilisk Curative Broth
**Category:** Curative
**Food Form:** Broth ([Organs] + [Blood])
**Components:** [Venom 8] + basilisk [Organs] + basilisk [Blood]
**DC:** 22 (14 + 8)
**Effect:** Remove poison effects up to level 8 (instant)

### Party Protection Soup (Batch)
**Category:** Enhancement
**Food Form:** Soup ([Meat] + [Fat] + [Bone])
**Components:** [Fire 18] + [Meat] Ã—3 + [Fat] Ã—3 + [Bone] Ã—3
**DC:** 36 (14 + 18 + 4 for 2 extra servings)
**Effect:** 3 servings, each person gets Fire Resistance 5 for 60 minutes
**Note:** Single component split among 3 people (180 min Ã· 3 = 60 min each)

---

## Dangerous Components

Some tags require careful handling:

**[Fire/Lightning]:** Failure = 1d6 energy damage
**[Venom]:** Failure = Sickened 1 (blocks further cooking)
**[Magical]:** Failure = Stupefied 1 for 10 minutes

Professional tools reduce failure consequences by one step.

---

## Integration

### With HarvestCraft
- All harvested components work in recipes
- Mundane materials provide base requirements
- Special tags enable enhanced effects
- Combat-harvested components work normally

### With HinderCraft  
- Recently hindered features may be easier to harvest
- Hindered components could provide fresher materials
- No special mechanical interaction required

### Economic Value
- Mundane recipes: 1-5 gp value
- Enhancement recipes: 10-50 gp value  
- Combat recipes: 25-100 gp value
- Curative recipes: 50-200 gp value

---

## Quick Reference

### Recipe Planning
1. **Choose category** (determines effect type)
2. **Select special component** (determines tag and duration)
3. **Choose food form** (based on available mundane components)
4. **Decide portions** (single or batch for Enhancement/Sustenance)
5. **Calculate DC** (14 + tag level + batch modifier if applicable)
6. **Cook** (30 min field, 1 hour camp)

### Duration Formula
- **Sustenance:** 1 hour Ã— tag level (max 24 hours)
- **Enhancement:** 10 minutes Ã— tag level (max 3 hours)
- **Combat:** 1 round Ã— tag level (max 5 rounds)
- **Curative:** Instant (affects conditions up to tag level)

### Batch Cooking
- **Combat:** No batching - always single serving
- **Enhancement/Sustenance:** Can split duration among servings
- **DC Calculation:** Base DC + 2 per extra serving
- **Duration Split:** Total duration Ã· servings = time per person
- **Important:** Cannot combine multiple special components for enhanced effects

---

**Remember:** CookCraft is simple - one component, one effect. Choose your category to determine how the component's power manifests. Combat recipes are personal quick buffs (no batching), while Enhancement and Sustenance can be shared meals (split duration). The mundane components you use determine the food form (stew, roast, jerky) but not the mechanical effect. This system turns leftover creature parts into meaningful tactical choices without complex rules.