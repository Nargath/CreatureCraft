# Creature Crafts Design Philosophy
*Core principles, rationales, and lessons for subsystem development*

---

## Purpose of This Document

This document explains **WHY** we make design decisions, provides guiding principles for future development, and captures lessons learned. For specific mechanical rules and technical specifications, see the Tag System Design document.

---

## Fundamental Design Principles

### 1. Simplicity is Paramount

**Core Principle:** Each subsystem should have ONE primary mechanic that can be explained in a single sentence.

**Rationale:** Players should internalize mechanics quickly without constant reference. Complex systems create friction and slow gameplay.

**Examples:**
- HinderCraft: "Target a feature, apply condition, attempt to hinder"
- HarvestCraft: "Roll Survival vs DC to extract components"
- CookCraft: "Component + Category = Effect"
- ForgeCraft: "Component + Item Type + Expression Path = Enhanced Equipment"

**Complexity Ceiling:** If explaining the mechanic requires multiple conditional statements or extensive examples, it's too complex.

**Why This Matters:** The best subsystem is one that players internalize after using once and never need to reference again.

---

### 2. Narrative Freedom, Mechanical Consistency

**Core Principle:** Let players describe HOW they do things while keeping WHAT happens mechanically consistent.

**Rationale:** Player creativity and roleplay should flourish without creating mechanical complexity or balance issues.

**Good Example - Food Forms in CookCraft:**
- Players choose if they make stew, roast, or jerky (narrative freedom)
- All provide the same mechanical effect (mechanical consistency)
- Mundane components determine available forms (light mechanical touch)
- **Result:** Rich roleplay without system complexity

**Bad Example - Recipe Lists:**
- Different recipes with different DCs for marginal benefits
- Forces players to optimize rather than roleplay
- Creates unnecessary lookup requirements
- **Result:** Math replaces creativity

**Application:** Whenever you're tempted to create mechanical distinctions, ask "Can this be narrative instead?"

---

### 3. Universal Language Through Tags

**Core Principle:** All subsystems reference the same tags with consistent meaning. The tag system is sacred.

**Rationale:** A universal language allows subsystems to work together seamlessly without requiring special interaction rules.

**What This Means:**
- Tags carry their data, not individual subsystem rules
- Tag interpretation is consistent across all uses
- New subsystems can be added without redefining existing tags

**Why Universal Language Matters:**
- Players learn once, apply everywhere
- Subsystems integrate naturally without special cases
- Future development builds on solid foundation
- Cross-referencing is intuitive and predictable

---

### 4. Player Scaling is Already Solved

**Core Principle:** PF2e's proficiency system handles character advancement. Don't add extra scaling mechanics.

**Rationale:** PF2e already has elegant level-based progression built in:
- Character level adds to all checks automatically
- Proficiency ranks (Trained/Expert/Master/Legendary) provide clear advancement
- A level 15 Master is vastly better than a level 5 Trained character

**Don't Add:**
- Extra scaling mechanics
- Level-based bonuses beyond PF2e standard
- Artificial progression systems
- "Unlock" mechanics tied to character level

**Why This Matters:** Adding redundant scaling creates complexity without value. Trust PF2e's existing progression.

---

### 5. Fixed Effects, Variable Application

**Core Principle:** Effect magnitude should be predictable and fixed. Variation comes from duration, uses, or scope - not power.

**Rationale:** Power scaling with tag level breaks balance and creates unpredictable outcomes. Fixed effects are easier to balance and mentally track.

**Effects Should Be Predictable:**
- Fire Resistance 5 is always Fire Resistance 5
- +1d6 damage is always +1d6 damage
- +2 circumstance bonus is always +2 circumstance bonus

**Variation Comes From:**
- Duration (tag level Ãƒâ€” time unit)
- Number of uses/charges
- What conditions can be affected (up to tag level)
- How many people can benefit

**Never:** Scale power directly with tag level (Fire Resistance = tag level breaks balance)

**Exception - Permanent Crafting Systems:**
Forgecraft deliberately breaks this rule for permanent items through tier grouping (not continuous scaling). This is a conscious, justified exception because:
- Permanent items deserve different treatment than temporary consumables
- Multi-day crafting investment should yield impressive results
- Item level gating provides balance safeguards
- Tier structure maintains some predictability

**Critical Note:** This exception is ONLY for permanent item crafting. Temporary systems (CookCraft, BrewCraft) must maintain fixed effects.

---

### 6. One Component, One Effect

**Core Principle:** Adding more components doesn't enhance effects. Each component provides one distinct benefit.

**Rationale:** Prevents "god item" optimization problems and keeps resource math simple.

**What This Prevents:**
- "God meal" combining [Fire 5] + [Fire 5] + [Sharp 3] for super-effects
- Complex calculations pooling tag levels
- Analysis paralysis over optimal combinations

**Multiple Components Can:**
- Make multiple separate items/meals
- Feed more people (split duration/uses among servings)
- Provide backup for crafting failures

**Why This Matters:** Maintains resource value, prevents optimization spirals, keeps gameplay fluid.

---

## Complexity Management

### 7. Context Determines Acceptable Complexity

**Core Principle:** The amount of complexity acceptable depends on when the mechanic is used.

**Combat/Active Systems (Keep Simple):**
- Used under time pressure
- Need instant resolution
- Decision paralysis is deadly
- Example: HinderCraft's two-action attack

**Exploration Systems (Moderate Complexity Okay):**
- Used during travel/exploration
- Some deliberation time available
- Can handle meaningful choices
- Example: HarvestCraft's component selection

**Downtime Systems (Can Be Complex):**
- Used during rest/town time
- Players have full deliberation time
- Can support deeper decision trees
- Examples: CookCraft's category selection, ForgeCraft's expression paths

**Why This Matters:** Match complexity to available decision time. Don't make players do math in initiative order.

---

### 8. Categories as Effect Lenses

**Core Principle:** Same component + different category = different effect. This is an elegant solution for player choice.

**Rationale:** Provides meaningful player agency without creating extensive recipe lists or complex interactions.

**What This Provides:**
- Player choice without complexity
- Clear mechanical outcomes
- Component reusability
- No need for extensive recipe memorization

**Example - [Fire] Component:**
- Sustenance: Fire resistance (environmental protection)
- Enhancement: +2 Reflex saves (combat performance)
- Utility: Ignite capability (special ability)

**Pattern Recognition:** This works because each category asks "How do I want to USE this essence?" rather than "What CAN I make?"

**Why This Matters:** One simple decision (choose category) replaces dozens of specific recipes while maintaining player agency.

---

### 9. Batch Processing Philosophy

**Core Principle:** Batching should be either dead simple or non-existent.

**Rationale:** Complex batching rules create mid-game calculation overhead and slow play.

**Simple Batching (Acceptable):**
- Split duration among servings (total duration ÃƒÂ· people)
- +2 DC per extra serving (universal rule)
- Clear restrictions on what can/can't be batched

**Complex Batching (Avoid):**
- Pooling multiple different tag levels
- Fractional efficiency calculations
- Conditional modifiers based on combinations

**Why This Matters:** If players need to do math during prep time, they'll avoid the system entirely.

---

## Resource Economy Philosophy

### 10. The Offcuts Philosophy

**Core Principle:** CookCraft uses "leftover" components that players aren't saving for other purposes. All other crafting systems work at ALL levels.

**What Are Offcuts:**
- Components players have forgotten about in inventory
- Low-level components that seem "beneath" current party level
- Excess components when you have too many of one type
- Random encounter materials not worth saving for projects
- The third [Fire 5] when you only needed two for weapon crafting

**The Resource Hierarchy:**
- **ForgeCraft:** Works at any level to make permanent items (Level 1 party makes +1 weapons with [Sharp 3])
- **BrewCraft:** Works at any level for potions and alchemical items
- **CookCraft:** Gets the "leftovers" - still valuable, but chosen last

**Natural Resource Decisions Created:**
- "Should I save this [Fire 8] for a permanent sword?"
- "Or just cook it for tomorrow's dungeon?"
- "I have six [Fire 3] components... might as well cook some"

**Why This Matters:** Creates natural strategic decisions without artificial level gating. CookCraft gives value to components that would otherwise rot in inventory, while other crafting systems remain viable and important at all levels.

---

### 11. Meaningful Choices, Not Math Problems

**Core Principle:** Design for strategic decisions, not optimization calculations.

**Good Choice Examples:**
- "Do I use [Fire 5] for immediate combat benefit or save it for permanent crafting?"
- "Do I prepare Sustenance (all-day protection) or Enhancement (better combat performance)?"
- "Do I harvest rare components or get moving before reinforcements arrive?"

**Bad Choice Examples:**
- "If I use 3Ãƒâ€”[Fire 5] with 2Ãƒâ€”[Meat] and 1Ãƒâ€”[Fat], what's my DC modifier?"
- "Should I split this across 4.3 servings for optimal efficiency?"
- "Let me calculate the exact value-per-tag-level optimization curve..."

**Eliminate Mid-Game Calculations:**
- No pooling different tag levels
- No fractional multipliers
- No conditional modifiers based on combinations
- No lookup tables during play

**Why This Matters:** Math problems during play kill momentum and fun. Strategic decisions create engagement and player investment.

---

## Integration Philosophy

### 12. Subsystems are Modular but Connected

**Core Principle:** Each subsystem must function independently while enhancing others when combined.

**What "Modular" Means:**
- Works without requiring other subsystems
- Has complete internal logic
- Can be added or removed from campaigns
- Teaches its own mechanics clearly

**What "Connected" Means:**
- Shares universal tag language
- Creates synergies when combined
- Respects resource economy across systems
- Provides value to other subsystem outputs

**Example Flow:**
- HinderCraft makes harvesting easier (optional synergy)
- HarvestCraft provides components (required input for crafting)
- CookCraft uses components (independent choice)
- All three work alone, all three work better together

**Why This Matters:** GMs can adopt subsystems gradually. Players can engage with what interests them. The system scales to table preferences.

---

### 13. Respect PF2e Foundations

**Core Principle:** Build on PF2e's existing systems rather than replacing them.

**What This Means:**
- Use existing bonus types correctly (item, circumstance, status)
- Respect action economy and time scales
- Use standard time intervals (1 minute, 10 minutes, 1 hour)
- Follow condition and trait rules
- Maintain bounded accuracy

**Don't Invent:**
- New bonus types when existing ones work
- New conditions when PF2e has equivalents
- Non-standard durations (73 minutes)
- Alternative action economy

**Why This Matters:** Players already know PF2e. Building on familiar foundations reduces learning curve and prevents conflicts with existing rules.

---

## Development Guidelines

### The Golden Rule

**When in doubt, choose the simpler option.**

**Rationale:** Complexity must be justified by creating meaningful player choice that couldn't exist otherwise. Every additional rule, modifier, or decision point needs to earn its place by significantly improving the play experience.

**Test for Complexity:**
- Can this be narrative instead of mechanical?
- Does this create meaningful choice or just more math?
- Will players remember this after using it once?
- Could we achieve 80% of this with 20% of the rules?

---

### Red Flags to Avoid

**Complexity Creep:**
- Multiple components with different calculations
- Conditional modifiers based on combinations
- Scaling that requires lookup tables
- More than one primary resource type per subsystem

**Mathematical Gymnastics:**
- Division during play (except simple halving)
- Multiplication beyond Ãƒâ€”2
- Adding multiple different tag levels together
- Percentage calculations
- Fractional multipliers

**Artificial Restrictions:**
- "Must learn recipe first" (gates player agency)
- "Only works with matched tag levels" (creates frustration)
- "Requires specific component combinations" (forces optimization)
- "Limited uses per day" (adds tracking burden)

**Power Scaling Traps:**
- Effects that scale continuously with tag level (breaks balance)
- Stacking same-type components (god item problem)
- Multiplicative power increases (exponential problems)
- Breaking bounded accuracy (PF2e core principle)

---

### Development Checklist

When creating or modifying a subsystem, verify:

**Simplicity Check:**
- [ ] Can the core mechanic be explained in one sentence?
- [ ] Are there 3 or fewer primary decision points?
- [ ] Can a player use it correctly after one example?
- [ ] Does it avoid mid-game calculations?

**Balance Check:**
- [ ] Do effects use fixed values (not scaled by tag level)?
- [ ] Is component power consistent across subsystems?
- [ ] Are time requirements appropriate to the activity?
- [ ] Do failure consequences block activity without spiraling?

**Integration Check:**
- [ ] Uses universal tag system correctly?
- [ ] Respects PF2e rules and conventions?
- [ ] Works alone but enhances other subsystems?
- [ ] Clear role in resource economy?

**Narrative Check:**
- [ ] Players have creative freedom in description?
- [ ] Mechanical outcomes remain consistent?
- [ ] Forms/methods are narrative, not mechanical?
- [ ] No artificial recipe or knowledge gates?

---

## Future Subsystem Vision

### Subsystem Identity Spaces

Each future subsystem should occupy a distinct niche in the resource economy:

**ForgeCraft (Permanent Items):**
- Creates lasting equipment at ANY level
- Longer time investment (days of downtime)
- Can support more complexity (downtime activity)
- Conscious exception to power scaling rule (tiered, not continuous)

**BrewCraft (Alchemy/Potions):**
- Bottled effects that can be stored
- Works at all levels like other systems
- Medium duration effects
- Bridge between temporary cooking and permanent forging

**RuneCraft/EnchantCraft (Enchantment):**
- Adds properties to existing equipment
- Works at any level (minor runes from low tags, major from high tags)
- Requires existing items + components
- Most complex acceptable (pure downtime)

**LoorCraft (Research/Knowledge):**
- Study components to unlock creature knowledge
- Provides tactical advantages and discovery
- Knowledge generation rather than item creation

**Key Principle:** Each should maintain distinct identity while respecting core philosophy. All work at every level of play, but players make strategic decisions about which system gets which components based on current needs.

---

## Philosophy in Practice

### When Philosophy Conflicts with Cool

**Question:** "I have this really cool idea, but it breaks one of the principles. What do I do?"

**Answer:** Test it, but be ruthlessly honest about results.

**Evaluation Process:**
1. **Identify the conflict** - Which principle does it break? Why?
2. **Justify the exception** - What does this idea provide that can't exist within the principle?
3. **Test thoroughly** - Does it actually create meaningful choice or just complexity?
4. **Be ready to simplify** - If testing shows problems, simplify ruthlessly
5. **Document the exception** - If kept, explain WHY this specific exception exists

**Example - ForgeCraft Power Scaling:**
- **Conflict:** Breaks Principle 5 (Fixed Effects, Variable Application)
- **Justification:** Permanent items deserve power progression, multi-day investment should feel impactful
- **Safeguards:** Item level gating, tier grouping (not continuous), bounded accuracy respected
- **Result:** Conscious, documented exception that enhances rather than undermines system

---

## Closing Thoughts

These principles exist to maintain consistency and quality, not to stifle creativity. When you have a genuinely innovative idea that challenges these guidelines, test it thoroughly. But remember:

**The best subsystem is one that players internalize after using once and never need to reference again.**

If your design requires players to constantly check rules, it needs simplification. If it creates meaningful choice with minimal overhead, you're on the right track.

Trust the philosophy. Test thoroughly. Simplify ruthlessly.

---

*For specific mechanical rules, DC calculations, tag structures, and technical specifications, see the Tag System Design document.*