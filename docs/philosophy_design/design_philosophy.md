# Creature Crafts Design Philosophy & Guidelines
*Core principles and lessons for subsystem development*

---

## Fundamental Design Principles

### 1. Simplicity is Paramount
**Core Rule:** Each subsystem should have ONE primary mechanic that can be explained in a single sentence.
- HinderCraft: "Target a feature, apply condition, attempt to hinder"
- HarvestCraft: "Roll Survival vs DC to extract components"
- CookCraft: "Component + Category = Effect"

**Complexity Ceiling:** If explaining the mechanic requires multiple conditional statements or extensive examples, it's too complex.

### 2. Narrative Freedom, Mechanical Consistency
**Principle:** Let players describe HOW they do things while keeping WHAT happens mechanically consistent.

**Good Example:** Food forms in CookCraft
- Players choose if they make stew, roast, or jerky (narrative)
- All provide the same mechanical effect (consistency)
- Mundane components determine available forms (light mechanical touch)

**Bad Example:** Different recipes with different DCs for marginal benefits
- Forces players to optimize rather than roleplay
- Creates unnecessary lookup requirements

### 3. Universal Language Through Tags
**The Tag System is Sacred:** All subsystems reference the same tags with consistent meaning.
- Tag level ALWAYS equals creature CR
- Same DC formula across all systems: **14 + Tag Level + Modifiers**
- Tags carry their data, not individual subsystem rules

**Tag Level Purpose by System:**
- **HinderCraft:** Determines DC only
- **HarvestCraft:** Determines DC only
- **CookCraft:** Determines duration/uses
- **Future Systems:** Should find ONE aspect to scale (not power)

---

## Mechanical Guidelines

### 4. Player Scaling is Already Solved
**Remember:** PF2e's proficiency system handles character advancement:
- Character level adds to all checks
- Proficiency ranks (Trained/Expert/Master/Legendary) add bonuses
- A level 15 Master is vastly better than a level 5 Trained character

**Don't:** Add extra scaling mechanics, level-based bonuses, or artificial progression systems.

### 5. Fixed Effects, Variable Application
**Effects should be predictable:**
- Fire Resistance 5 is always Fire Resistance 5
- +1d6 damage is always +1d6 damage

**Variation comes from:**
- Duration (tag level Ã— time unit)
- Number of uses/charges
- What conditions can be affected (up to tag level)
- How many people can benefit

**Never:** Scale power directly with tag level (Fire Resistance = tag level breaks balance)

### 6. One Component, One Effect
**No Stacking:** Adding more components doesn't enhance effects.
- Prevents "god meal" problems
- Keeps math simple
- Maintains resource value

**Multiple components can:**
- Make multiple separate items
- Feed more people (split duration/uses)
- Provide backup for failures

---

## Complexity Management

### 7. Context Determines Acceptable Complexity

**Combat/Active Systems (Simple):**
- Used under pressure
- Need instant resolution
- Example: HinderCraft's two-action attack

**Exploration Systems (Moderate):**
- Used during travel/exploration
- Can handle some choice
- Example: HarvestCraft's component selection

**Downtime Systems (Can be Complex):**
- Used during rest
- Players have time to consider
- Example: CookCraft's category selection and food forms

### 8. Categories as Effect Lenses
**Pattern:** Same component + different category = different effect

This elegant solution provides:
- Player choice without complexity
- Clear mechanical outcomes
- Reusability of components
- No need for extensive recipe lists

**Example:** [Fire] component
- Sustenance: Cold resistance
- Enhancement: Fire resistance
- Combat: Fire damage
- Curative: Remove disease

### 9. Batch Processing Philosophy

**Either dead simple or non-existent:**
- Combat effects: NO batching (individual buffs)
- Long duration effects: Simple division (duration Ã· servings)
- Complex batching with multiple components: Avoid entirely

**If batching exists:**
- One rule for all: +2 DC per extra serving
- Clear category restrictions
- No complex component pooling

---

## Resource Economy

### 10. The Offcuts Philosophy
**CookCraft's unique role:** Uses the "leftover" components that players aren't saving for other purposes.

**What are offcuts?**
- Components players have forgotten about in inventory
- Low-level components that seem "beneath" current party level
- Excess components when you have too many of one type
- Components from random encounters not worth saving
- The third [Fire 5] when you only needed two for crafting

**Not level-gated:** Other subsystems work at ALL levels:
- **ForgeCraft:** Uses components at any level to make permanent items
- **BrewCraft:** Uses components at any level for potions
- **CookCraft:** Gets the "leftovers" regardless of level

**This creates natural resource decisions:**
- "Should I save this [Fire 8] for a permanent sword?"
- "Or just cook it for tomorrow's dungeon?"
- "I have six [Fire 3] components... might as well cook some"

**The beauty:** CookCraft gives value to components that would otherwise rot in inventory, while other crafting systems remain viable and important at all levels.

### 11. Meaningful Choices, Not Math Problems
**Good Choice:** "Do I use this [Fire 5] for combat now or save it for enhancement later?"
**Bad Choice:** "If I use 3Ã—[Fire 5] with 2Ã—[Meat] and 1Ã—[Fat], what's my DC modifier?"

**Eliminate mid-game calculations:**
- No pooling different tag levels
- No fractional multipliers
- No conditional modifiers based on combinations

---

## Integration Principles

### 12. Subsystems are Modular but Connected
**Each subsystem must:**
- Function independently
- Share the universal tag language
- Not require other subsystems to work
- Enhance other subsystems when combined

**Example Flow:**
- HinderCraft makes harvesting easier (optional)
- HarvestCraft provides components (required for crafting)
- CookCraft uses components (independent choice)

### 13. Maintain PF2e Compatibility
**Follow PF2e conventions:**
- Use existing bonus types correctly (item, circumstance, status)
- Respect action economy
- Use standard time intervals (1 minute, 10 minutes, 1 hour)
- Follow condition and trait rules

**Avoid:**
- Creating new bonus types
- Inventing new conditions when existing ones work
- Using non-standard durations (73 minutes)

---

## Development Checklist

When creating or modifying a subsystem, verify:

### Simplicity Check
- [ ] Can the core mechanic be explained in one sentence?
- [ ] Is the DC formula just 14 + Tag Level + simple modifier?
- [ ] Are there 3 or fewer decision points?
- [ ] Can a player use it correctly after one example?

### Balance Check
- [ ] Do effects use fixed values, not scaled by tag level?
- [ ] Is component power consistent across subsystems?
- [ ] Are time requirements appropriate to the activity?
- [ ] Do failure consequences block activity without spiraling?

### Integration Check
- [ ] Uses universal tag system correctly?
- [ ] Respects PF2e rules and conventions?
- [ ] Works alone but enhances other subsystems?
- [ ] Clear role in resource economy?

### Narrative Check
- [ ] Players have creative freedom in description?
- [ ] Mechanical outcomes remain consistent?
- [ ] Food forms/methods are narrative, not mechanical?
- [ ] No artificial recipe or knowledge gates?

---

## Red Flags to Avoid

**Complexity Creep:**
- Multiple components with different calculations
- Conditional modifiers based on combinations
- Scaling that requires lookup tables
- More than one primary resource type

**Mathematical Gymnastics:**
- Division during play (except simple halving)
- Multiplication beyond Ã—2
- Adding multiple different tag levels
- Percentage calculations

**Artificial Restrictions:**
- "Must learn recipe first"
- "Only works with matched tag levels"
- "Requires specific component combinations"
- "Limited uses per day"

**Power Scaling Traps:**
- Effects that scale with tag level
- Stacking same-type components
- Multiplicative power increases
- Breaking bounded accuracy

---

## The Golden Rule

**When in doubt, choose the simpler option.**

If you're adding complexity, it must be justified by creating meaningful player choice that couldn't exist otherwise. Every additional rule, modifier, or decision point needs to earn its place by significantly improving the play experience.

The best subsystem is one that players internalize after using once and never need to reference again.

---

## Future Subsystem Spaces

Based on these principles, future subsystems should each have a distinct identity:

### ForgeCraft (Permanent Items)
- Creates lasting equipment at ANY level
- Level 1 party makes +1 weapons with [Sharp 3] components
- Level 15 party makes legendary items with [Sharp 15] components
- Longer time investment than cooking
- Can be more complex (downtime activity)

### BrewCraft (Alchemy/Potions)
- Bottled effects that can be stored
- Works at all levels like other systems
- Medium duration effects
- Possibly uses multiple components meaningfully
- Bridge between temporary cooking and permanent forging

### RuneCraft (Enchantment)
- Adds properties to existing equipment
- Works at any level (minor runes from [Tag 3], major from [Tag 15])
- Requires existing items + components
- Most complex acceptable (pure downtime)

Each should maintain its own identity while respecting these core principles. All work at every level of play, but players make strategic decisions about which system gets which components based on current needs.

---

*Remember: These guidelines are meant to maintain consistency and quality, not stifle creativity. When you have a genuinely innovative idea that breaks these rules, test it - but be ready to simplify ruthlessly if it doesn't enhance play.*