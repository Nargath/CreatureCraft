# Modular Tag Subsystem Design
*Universal framework for creature features across multiple game systems*

---

## Design Philosophy

The tag system balances **narrative specificity** with **mechanical simplicity** to create interconnected subsystems that share a common language.

**Core Problem Solved:** Different game systems (combat, crafting, cooking, harvesting) need to reference creature features in consistent ways without each system requiring its own unique mechanics.

**Solution:** Universal tags that provide standardized data to all subsystems while preserving player choice in how they track and organize materials.

### Player Experience
- **Narrative Choice:** "Dragon Teeth [Sharp 8]", "Wyvern Scales [Defense 6]" 
- **Pragmatic Choice:** "[Sharp 8] Components", "[Defense 6] Materials"
- **System Processing:** All subsystems read the tag data ([Sharp 8], [Defense 6]) and ignore item names
- **Result:** Rich collecting experience with streamlined mechanical integration

---

## Fundamental Rules

### Rule 1: Tag Level = Creature CR
**All tags on a creature are set to the creature's Challenge Rating:**
- CR 8 Red Dragon â†’ [Fire 8], [Flight 8], [Defense 8]
- CR 15 Ancient Dragon â†’ [Fire 15], [Flight 15], [Defense 15]
- CR 3 Goblin â†’ [Mobility 3], [Vital 3]

This creates uniform scaling across all creature features and eliminates individual power level calculations.

### Rule 2: Single Tag Per Component
**Each harvested component has exactly one tag:**
- Dragon Teeth â†’ [Sharp 15] only
- Dragon Fire Glands â†’ [Fire 15] only  
- Dragon Scales â†’ [Defense 15] only

Variety comes from different components, not multiple tags per component.

### Rule 3: Universal DC Formula
**All subsystems use:** DC = 14 + Tag Level + Difficulty Modifier
- Follows PF2e standard DC structure
- Tag Level provides base difficulty
- Difficulty Modifier applied based on task/creature complexity

---

## Tag Categories

### Special Tags (Leveled)
Represent extraordinary creature abilities with mechanical power scaling:
- **[Fire X]** - Heat, combustion, thermal effects
- **[Venom X]** - Toxins, poisons, disease
- **[Sharp X]** - Cutting, piercing, penetration
- **[Flight X]** - Aerial movement, wind effects
- **[Sensory X]** - Enhanced perception, detection
- **[Magical X]** - Arcane essence, spell enhancement

**Characteristics:**
- Tag level determines effect potency and DC
- Used across multiple subsystems (Hindercraft, Crafting, Cooking)
- Provide enhanced capabilities and magical effects

### Mundane Tags (Unleveled)
Represent basic materials for survival and standard crafting:
- **[Meat]** - Protein sources, cooking ingredients
- **[Hide]** - Leather goods, basic armor
- **[Bone]** - Tools, structural materials
- **[Fat]** - Cooking oils, weatherproofing

**Characteristics:**
- No level scaling (quantity determined by creature size)
- Support survival gameplay and economic activities
- Functionality tracked by tag presence/absence

---

## Universal DC System

### Base DC Calculation
**DC = 14 + Tag Level** (following PF2e standard progression)

### Difficulty Modifiers
Applied based on task complexity or creature properties:
- **Normal:** +0 
- **Hard:** +2
- **Very Hard:** +5  
- **Incredibly Hard:** +10

### Modifier Sources
**Hindercraft & Harvesting:** Determined by creature statblock
- "Hindering this ancient dragon is Very Hard" = +5 modifier

**Crafting & Cooking:** Determined by recipe complexity  
- "Masterwork enchanted blade recipe" = Very Hard = +5 modifier

### Examples
- **Hellhound [Fire 3]:** Base DC 17, Normal hindering DC 17, Hard harvesting DC 19
- **Ancient Dragon [Fire 17]:** Base DC 31, Very Hard hindering DC 36, Normal crafting DC 31

---

## Tag Data Structure

Each tag contains standardized data that all subsystems can reference:

### Special Tag Data Categories
- **Hindercraft Data:** Conditions applied, save types, effects
- **Harvesting Data:** Yield types, special requirements, spoilage rules  
- **Crafting Data:** Material properties, applications, effect scaling
- **Cooking Data:** Consumable effects, preparation requirements, duration
- **Economic Data:** Base values, rarity progression, trade factors

### Mundane Tag Data Categories
- **Functionality:** Primary uses and applications
- **Yield Scaling:** Based on creature size, not CR
- **Condition Tracking:** Fresh/Preserved/Spoiled states
- **Spoilage Rules:** When tags are lost due to degradation

---

## Subsystem Integration

### Interface Principles
**Each subsystem accesses tag data independently:**
- Hindercraft reads combat conditions and save types
- Harvesting reads yield quantities and extraction requirements
- Crafting reads material properties and enhancement scaling
- Cooking reads consumable effects and preparation methods

**Cross-subsystem interactions handled at implementation level:**
- Framework provides data, subsystems determine interactions
- Example: Hindered creatures may be easier to harvest (subsystem design choice)

### Data Consistency
**Tag level determines scaling across all subsystems:**
- [Fire 8] provides consistent baseline power regardless of context
- Individual subsystems apply their own difficulty modifiers
- Effect potency, duration, and value all scale with tag level

---

## Implementation Guidelines

### For Game Masters

**Tag Assignment Process:**
1. Identify creature's significant features (breath weapons, natural weapons, etc.)
2. Assign appropriate tag type based on feature function
3. Set tag level to creature's Challenge Rating
4. Determine task difficulty modifiers based on creature properties

**Creature Variety Through Different Components:**
- Single creature provides multiple tag types through different body parts
- Each component has exactly one tag for simplicity
- Higher CR creatures provide higher tag levels across all components

### For Players

**Inventory Tracking Choices:**
- **Specific tracking:** "Ancient Dragon Teeth [Sharp 15]"
- **Generic tracking:** "[Sharp 15] Components x3"
- **Mixed approach:** Specific items for themed collections, generic for bulk materials

**Material Functionality:**
- All components with same tag level work identically in recipes
- Tag presence determines usability (spoiled items lose tags)
- Higher tag levels provide more powerful effects but require higher skill checks

---

## System in Practice

### Example: Ancient Red Dragon (CR 17)

**Special Components Available:**
- Dragon Fire Glands [Fire 17] â†’ Base DC 31
- Dragon Teeth [Sharp 17] â†’ Base DC 31  
- Dragon Eyes [Sensory 17] â†’ Base DC 31
- Dragon Wings [Flight 17] â†’ Base DC 31

**Mundane Materials Available:**
- Dragon Meat [Meat] (40 Bulk from Gargantuan size)
- Dragon Hide [Hide] (25 Bulk)
- Dragon Scales [Scale] (30 Bulk)
- Dragon Bones [Bone] (20 Bulk)

**Usage Examples:**
- **Hindercraft:** Target dragon eyes (Very Hard) = DC 36 Reflex save vs Dazzled
- **Harvesting:** Extract fire glands (Very Hard) = DC 36 skill check
- **Crafting:** Make fire sword with [Fire 17] (Normal recipe) = DC 31 crafting check
- **Cooking:** Prepare strength stew with [Meat] (Normal recipe) = Standard cooking DC

### Material Flow Example

**Player Collection:**
- Harvests "Ancient Dragon Teeth [Sharp 17]" 
- Chooses to track specifically for thematic sword project

**Crafting Application:**
- Recipe requires "[Sharp 12+] material x2"
- Dragon Teeth [Sharp 17] meets requirement âœ“
- Base DC: 14 + 17 = 31
- Recipe modifier: Masterwork (+5) = Final DC 36
- Effect: Sword gains cutting power scaled to [Sharp 17] potency

**System Result:**
- Tag level drives mechanics (DC calculation, effect power)
- Item name provides narrative satisfaction
- Recipe complexity modifies difficulty appropriately

---

## Mundane Materials System

### Design Principle: Volume Over Power
Mundane materials use unleveled tags for categorization, with creature size determining yield quantity rather than quality scaling.

### Quantity Scaling by Creature Size
- **Tiny:** 0.1Ã— base yield
- **Small:** 0.5Ã— base yield
- **Medium:** 1Ã— base yield  
- **Large:** 3Ã— base yield
- **Huge:** 5Ã— base yield
- **Gargantuan:** 10Ã— base yield

### Condition and Spoilage Management
**Tag presence determines functionality:**
- "Fresh Dragon Meat [Meat]" â†’ Functional for cooking
- "Spoiled Dragon Meat" (no tag) â†’ Unusable in recipes
- "Preserved Dragon Meat [Meat]" â†’ Extended shelf life but same function

**Condition information appears in item names for player reference but doesn't affect mechanical interactions** - only tag presence matters for rules.

### Economic and Survival Integration
- Enables systematic cooking ingredient collection
- Supports monster hunting/trading economy gameplay  
- Provides mechanical framework for bounty hunting and resource management
- Fills gaps in PF2e's survival and economic systems

---

This framework provides the universal language and scaling principles that allow independent subsystems to integrate seamlessly while maintaining their own mechanical complexity and design goals.