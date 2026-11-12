# Extension-Idle

Adds "idle prompting" after the user has been idle for some time to organically continue the conversation.

Idea and implementation by [city-unit](https://github.com/city-unit).

## Changes in this fork

This fork fixes idle prompting in group chats.

- Fixed a typo in `resetIdleTimer`: `context.groupID` is now `context.groupId`, so the timer starts in group chats.
- In group chats, the idle prompt now runs SillyTavern's `/trigger` command, which makes a group member reply. Before, it called a function that needs a single selected character and crashed in groups with "Cannot read properties of undefined (reading 'name')".
- In group chats, the idle prompt text isn't sent; the character just continues naturally. One-on-one chats work as before.
- Tip: leave "Use Continuation" turned off, or the idle message may not fire.

Original extension by city-unit and the SillyTavern team, licensed under AGPL-3.0.


