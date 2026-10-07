# Modern Bag Roddsoft

Modern Bag Roddsoft is a fork of Modern Bag focused on making the Gen1Recomp inventory faster, clearer, and more comfortable to use. The original pocket-based Bag remains the foundation; this fork builds on it with quality-of-life navigation, persistent selections, Favorites and pins, search tools, expanded TM/HM information, unlimited inventory, and Gen1 Modern UI support.

## Highlights added in this fork

- **Seven inventory pockets** including a dedicated **FAVORITES** pocket.
- **Visible pocket navigation header** showing the current pocket and its position in the pocket set.
- **Persistent cursor memory per pocket.** Reopening a pocket returns to the item you last selected when it is still available. This is especially useful in battle: after throwing a Poké Ball, reopening the BALLS pocket returns to that ball instead of starting at the first entry.
- **Wrap-around navigation.** Press **Up** on the first item to jump to the last item, or **Down** on the last item to return to the first.
- **Hold-to-scroll** with configurable OFF, NORMAL, FAST, and VERY FAST speeds.
- **Configurable opening pocket**, including a **LAST USED** option.
- **Favorites and persistent pins** for keeping important items easy to reach.
- **Automatic sorting** while preserving pinned items at the top.
- **Quick Search** across the entire Bag.
- **Advanced TM/HM tools** with move-name search, filters, sorting, and detailed move information.
- **Unlimited inventory capacity** for both distinct item types and stack sizes.
- **Gen1 Modern UI integration**, including touch-friendly search/filter controls and keyboard presentation.

## Pockets and navigation

The Bag is divided into:

- **FAVORITES** — items marked as favorites from any other pocket.
- **MEDICINE** — healing items, status cures, Revives, PP recovery, vitamins, and Rare Candy.
- **BALLS** — built-in and modded items registered as Poké Balls.
- **TM/HM** — all TMs and HMs.
- **BATTLE** — X items, Dire Hit, Guard Spec, and Poké Doll.
- **KEY ITEMS** — non-tossable and key items.
- **OTHER** — stones, Repels, Escape Rope, fossils, and items not covered above.

Press **Left/Right** to change pockets. The pocket header makes the current category and pocket position visible.

Vertical navigation wraps around the list. Pressing **Up** while the first item is selected moves directly to the last item, and pressing **Down** on the last item returns to the first.

Each pocket also remembers its last selected item between Bag openings. If that item is no longer available, the Bag safely falls back to an available entry.

## Opening pocket and fast scrolling

In **MODS → Modern Bag Roddsoft → Options** you can configure:

- **Opening Pocket** — FAVORITES, MEDICINE, BALLS, TM/HM, BATTLE, KEY ITEMS, OTHER, or LAST USED.
- **Hold Scroll Speed** — OFF, NORMAL, FAST, or VERY FAST.

The default opening pocket remains **MEDICINE**. Choosing **LAST USED** makes the Bag reopen on the pocket you most recently used.

Holding **Up** or **Down** repeats list movement automatically. **FAST** is the default repeat profile. This uses Gen1Recomp's native ListMenu key-repeat support so remapped keyboard and controller inputs continue to work.

## Favorites, pins, and item tools

Press **SELECT** while an item is highlighted to open **ITEM OPTIONS**:

- **ADD FAVORITE / REMOVE FAVORITE** — add or remove the item from FAVORITES.
- **PIN TO TOP / UNPIN ITEM** — keep the item above unpinned items in its normal category.
- **MOVE ITEM** — manually reposition an item for the current Bag session.
- **CANCEL** — close ITEM OPTIONS.

Row markers show saved status: `F` for Favorite, `P` for pinned, and `PF` for both.

Favorites and pins persist even if an item stack reaches zero. When the item is acquired again, its saved Favorite and Pin status returns.

## Automatic sorting

Items are sorted automatically by pocket and display name when the Bag opens and when item types are added or removed. TMs and HMs remain in numerical order, with HMs before TMs.

Pinned items stay above unpinned items. Manual reordering through **ITEM OPTIONS → MOVE ITEM** is available for the current Bag session.

## Quick Search

Press **START** from any pocket except TM/HM to open Quick Search.

Search works across the full Bag and matches both displayed item names and internal item identifiers. Choosing a result returns to the appropriate pocket with that item selected.

The search keyboard supports controller/keyboard navigation and, with Gen1 Modern UI enabled, large pointer/touch-friendly keys. DEL, CLR, GO, and EXIT are available directly from the keyboard.

## Advanced TM/HM tools

The **TM/HM** pocket has a dedicated START menu that can:

- search by the move contained in a TM or HM;
- filter by elemental type;
- filter by **PHYSICAL**, **SPECIAL**, or **STATUS** using Generation I damage rules;
- sort by machine number, move name, highest power, or lowest power;
- combine move-name, type, and damage-class filters.

Press **Y** on controller or **I** on keyboard while a TM/HM is highlighted to open **MOVE INFORMATION**, showing the move's type, class, power, accuracy, PP, and effect.

Pinned machines remain above unpinned machines under every sorting mode.

## Unlimited inventory

The Bag can contain an unlimited number of distinct item types, and individual stacks can exceed the vanilla 99-item limit.

Modern Bag Roddsoft wraps Gen1Recomp's normal BagMenu rather than replacing item behavior. Items continue to be used, consumed, taught, thrown, and validated through the game's normal inventory systems.

## Gen1 Modern UI support

Modern Bag Roddsoft supports the `gen1ModernUi` API v1 compatibility contract.

With **Gen1 Modern UI 0.8.2 or newer**, the pocket Bag uses its dedicated pocket-aware presentation. Quick Search and TM/HM move search expose keyboard-grid state for large individual keys, Move Information integrates with the UI, and dedicated SEARCH/FILTER touch controls are available.

Gen1 Modern UI is optional. Without it, all Modern Bag Roddsoft inventory features continue to work with the classic 160×144 interface.

## Installation and updates

Import the release ZIP through the Gen1Recomp MODS manager, enable **Modern Bag Roddsoft**, and fully restart Gen1Recomp.

**Important for upgrades from versions using the old `modern_bag` ID:** Modern Bag Roddsoft now uses the new internal ID `modern_bag_roddsoft`. Remove/disable the old installation and manually install the new release ZIP. Saved mod-specific settings from the old ID may not carry over automatically.

This fork includes GitHub release metadata for the G1R Deluxe mod updater. Once an updater-aware version is installed, future published versions can be discovered through the launcher.

## Compatibility

Custom Poké Balls and machines are categorized using their registered item fields. Conventional custom medicines are detected from their effect identifiers, while unknown items safely fall back to OTHER.

The internal mod ID is `modern_bag_roddsoft`. This intentionally separates Modern Bag Roddsoft from installations that used the older `modern_bag` ID.
