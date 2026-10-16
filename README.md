# MoonManners 🌙

A WoW Forever addon project combining thoughtful buff assistance, characterful thank-you messages, and optional healing suggestions.

## Planned features

- **Reciprocal buff etiquette:** track recent outbound buffs so a player's return buff triggers a single thank-you, not another buff request.
- **Spam protection:** separate per-player cooldowns for buff offers, healing prompts, and gratitude; never require wasted mana to dismiss a notification.
- **Rank-aware buffs:** choose the highest learned buff rank the recipient can receive, with validation against WoW Forever's actual restrictions.
- **Wandering healer:** optional prompts when an eligible friendly player drops below 40% health during combat. Separate toggles for strangers and party/raid members, and a configurable threshold.
- **Customisable messages:** add, edit, remove, and preview multiple lines inside the addon UI, saved per character or profile; support `{name}` and `%s` substitutions.
- **Racial flavour:** selectable and/or automatically detected race-specific thank-you message sets, with custom lines mixed in if desired.
- **Manual, safe casting:** respect WoW's protected-action restrictions; prompts may offer secure click/keybind actions where permitted, rather than claiming unattended auto-casting.

## Development status

Planning / initial repository setup. The functions above are not implemented yet. Source addons under evaluation: Manners and Forever Thanks. Compatibility needs verification against WoW Forever interface 16001 and the client's available APIs.


## Gratitude delivery modes

- **Whisper only:** send one selected racial/custom thank-you line.
- **Emote only:** perform a configurable `/thank`, `/salute`, `/bow`, `/wave`, `/cheer`, or `/applaud` (as supported by the client).
- **Whisper + emote:** send a thank-you line and perform one selected or randomly rotated emote.
- **Off:** no automatic gratitude.

Allow fixed emote selection or random rotation from an enabled-emote list, and use the same per-recipient cooldown for combined actions so one buff event never triggers repeated whispers/emotes. Validate that the recipient is a valid emote target, avoid changing the player's selected target, and gracefully fall back if targeted emotes are unsupported. Respect client chat and emote restrictions.
