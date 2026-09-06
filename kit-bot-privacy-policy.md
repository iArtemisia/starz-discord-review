# STARZ Kit Bot Privacy Policy

Last updated: September 6, 2026.

STARZ Kit Bot is operated by the STARZ bot owner for the STARZ Discord and Rust Console Edition community. This policy explains how the bot processes and stores information while linking Discord members to Rust players, controlling role-based kit access, delivering kits and purchases, and providing authorized server-management features.

## Discord data used

The bot may use the following Discord information when a feature requires it:

- Discord server, channel, message, role, user, and application identifiers.
- Usernames, global and server display names, nicknames, role memberships, and permissions.
- Slash-command inputs, button and modal interactions, and the identity of the user performing an action.
- Administrator-configured channels, roles, kit mappings, shop settings, event and task settings, and related audit information.
- Discord-to-Rust account links, including the Discord user ID, Rust gamertag or player identifier, server, verification state, timestamps, and linking method.
- Kit ownership, purchased or assigned access, claim and cooldown state, delivery results, virtual-currency balances, shop purchases, and game or reward records associated with a Discord user.

STARZ Kit Bot currently uses Discord's Guild Members privileged intent. It needs current member roles and names to verify role-gated Elite, VIP, custom, special, and Spawn Kit access; match an in-game Rust gamertag to a linked or uniquely matching Discord member; inspect members of configured roles for role-holder tracking and role-based access verification; and react when a role or nickname change affects access. If the required member information is unavailable or ambiguous, protected actions are intended to fail closed.

The bot does not use the Guild Presences privileged intent and does not collect Discord online status, activities, or presence history. Rust server online status is obtained from the game server's own RCON or log data, not Discord presence.

## Message content

The Message Content privileged intent and weekly purchase listener are currently disabled in the production Kit Bot configuration. The bot therefore does not currently operate passive message-content auto-responses or purchase-log listening.

The code supports optional administrator-enabled message features. If those features are enabled in the future, the bot may inspect non-bot messages in accessible community channels in memory to match administrator-configured exact or contains auto-response triggers. It may also parse messages and embeds in a specifically configured purchase-log channel to identify a Discord user or role and a weekly virtual-currency amount.

The bot does not maintain a general archive of ordinary server conversations. Administrator-authored sticky and auto-response trigger or response text can be stored as configuration. For configured purchase-log processing, the bot can store derived information such as Discord message, user, and role identifiers, the target server, amount, processing result, deduplication state, and subscription state; it does not store the original ordinary message body as a general chat record.

Message content is not used to train artificial-intelligence or machine-learning models. The bot's supported parsing and matching behavior is deterministic and does not call an AI or language-model service.

## Rust server and operational data

To provide its game-server features, the bot may process and store:

- Rust server identifiers and configuration, Rust gamertags and immutable player identifiers, and account-link records.
- RCON and game-log events needed for approved features, including kit requests, login or respawn evidence, qualifying kills and deaths, team information, and delivery acknowledgements.
- In-game coordinates used for heat maps, event or teleport features, and saved TP Home locations. These are virtual Rust world coordinates, not real-world device location.
- Kit definitions, item shortnames and quantities, role eligibility, entitlements, cooldowns, player preferences, claim attempts, delivery receipts, and duplicate-suppression records.
- Virtual-currency balances, ledger entries, shop categories and purchases, queued or banked deliveries, minigame results, reward history, and associated actor and timestamp information.
- Scheduled tasks, event configuration and recovery state, server-health samples, staff actions, and diagnostic or audit records.
- When separately configured, website fulfillment or TikTok integration identifiers, request or order state, entitlement results, and replay-protection records.

Optional schemas or integrations listed above are not necessarily enabled on every server. The bot processes them only when the corresponding feature is configured and used.

## Purpose and access

Information is used to authenticate and authorize Discord and Rust users, deliver configured kits and purchases, enforce cooldowns and role requirements, maintain player-facing statistics and rewards, prevent duplicate or unauthorized grants, recover safely after restarts, operate configured server features, and diagnose failures.

Discord results are visible according to the permissions of their destination channels, private responses, or direct messages. Ordinary Discord members do not receive direct access to the hosted database files. Authorized STARZ staff can use role- and permission-gated bot functions, and direct access to hosted files is controlled through the operator's Railway project access.

## Storage and security

Operational records are stored outside Discord in SQLite databases and JSON files on the Kit Bot's Railway-hosted persistent volume. Railway states in its [Data Processing Addendum](https://railway.com/legal/dpa) that databases are encrypted at rest and protected with access controls and monitoring. STARZ Kit Bot does not separately encrypt every SQLite or JSON record in its own application code.

The bot uses server-side Discord permission checks for protected actions, redacts RCON credentials from supported diagnostic output, uses bounded and duplicate-safe receipts for sensitive delivery workflows, protects supported website requests with signatures, timestamps, and replay checks, and encrypts supported gift-card secrets at the application layer. No internet-connected service can guarantee absolute security.

Discord and Railway process information as the communication and hosting providers used to operate the bot. Separately enabled STARZ services may receive the minimum signed fulfillment or status information required for their configured integration.

## Retention

There is no single automatic expiration period for all STARZ Kit Bot data.

Under the current code defaults, pending account-link codes expire after about five minutes, heat-map event rows are retained for about two days, several kill-streak, non-player-event, and diagnostic or duplicate-suppression records are retained for about seven days, and owner-health samples are retained for about fourteen days. Some successfully posted shop-log and scheduled-task history rows are configured for prompt deletion. Feature settings can affect these periods.

Account links, kit definitions and assignments, entitlements, cooldown state, balances and ledgers, aggregate player statistics, purchase or fulfillment receipts, scheduled-task and event configuration, administrative audit records, and some delivery receipts can remain while operationally needed or until an authorized deletion, replacement, reset, or retention process removes them. Migration or recovery backups can temporarily retain copies. Removing the bot from a server or ceasing use does not automatically erase every stored record.

Messages, embeds, logs, or files posted back to Discord remain subject to Discord's and the relevant server's retention and deletion controls.

## Deletion requests and choices

To request deletion or ask a privacy question, open a support ticket in the STARZ Discord server and ask to contact the bot owner. Identify **STARZ Kit Bot** and describe the Discord account, Rust account, server, purchase, kit, statistic, or other records you want reviewed.

Requests are handled manually. The owner may need to verify that the requester controls the relevant Discord or Rust account or is authorized for the relevant server or record. No fixed response or deletion deadline is currently promised.

Deleting information required by a feature can prevent account linking, role verification, kit access, purchases, statistics, or other dependent features from working until the required information is supplied again. Deletion does not create a permanent exclusion from the bot, and later use can create new records.

The bot does not provide one universal per-user switch that opts an account out of all Guild Members processing while continuing to use role-gated features. Leaving the Discord server stops future live member updates but does not automatically remove all historical operational records. A user can ask staff to remove an account link or other eligible data through the support process above.

Because Message Content processing is currently disabled, the production bot does not currently inspect ordinary message text for the optional message features described above. If those features are enabled later, there is no universal individual opt-out while continuing to use the affected channel feature; server administrators can disable the applicable auto-response or purchase listener, and users can avoid optional submissions or configured purchase-log channels.

## Policy updates

This policy will be updated when STARZ Kit Bot's data practices materially change. Questions and deletion requests should be directed to the bot owner through a STARZ support ticket.
