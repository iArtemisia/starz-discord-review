# STARZ Ticket Bot Privacy Policy

Last updated: September 6, 2026.

STARZ Ticket Bot is operated by the STARZ bot owner for the STARZ Discord and Rust Console Edition community. This policy explains how the bot processes and stores information while providing support tickets, staff tools, help responses, transcripts, and bounty workflows.

## Discord data used

The bot may use the following information when a feature requires it:

- Discord server, channel, thread, message, role, user, and application identifiers.
- Discord usernames, display names, mentions, roles, and permissions supplied with messages, interactions, or specific member lookups.
- Ticket form submissions and guided-intake answers, including subjects, questions, server details, player or team names, staff-supplied closing reasons, and other text entered for support.
- Messages and attachments posted in ticket channels and private staff-notes threads.
- Staff activity connected to tickets, including claim, unclaim, escalation, close, message-count, and clock-in records with relevant identifiers and timestamps.
- Administrator-configured help-directory entries, exact-match keywords, automatic reply text, ticket-panel settings, sticky-message text, and associated media.
- Bounty submission and workflow data, which can include submitter and target identifiers or names, server details, amounts, notes, uploaded evidence, and funding, payout, Forum-post, and completion state.

The bot does not subscribe to Discord's privileged Guild Members or Guild Presences gateway intents. It does not collect Discord online status, activities, or presence history. It can receive member and role information included with a message or interaction and can request a specific member from Discord when needed for a ticket action.

## Message Content Intent

The bot uses the Message Content Intent. In Discord channels the bot can access, it checks incoming text to recognize its configured prefix commands, the explicit `directory` trigger, configured exact-match help topics, guided ticket-intake replies, and staff sticky-message setup.

This does not mean every accessible server conversation is archived. Ordinary messages that do not activate a stored feature are evaluated transiently and are not saved as a general chat history. However, messages inside a ticket or staff-notes thread can later be read and retained in a transcript when the ticket is closed. Text deliberately saved as a sticky, help entry, or guided-intake answer is also retained as operational data.

Message content is not used to train artificial-intelligence or machine-learning models. The bot's help matching and intake behavior are deterministic bot features, not AI model training or inference.

## Why the data is used

The bot uses this information to:

- create private support channels and route normal, Management+, streamer, architect, and bounty tickets;
- verify access and apply Discord role and channel permissions;
- guide users through ticket intake and provide configured help responses;
- let authorized staff claim, escalate, annotate, rename, and close tickets;
- create staff and player transcript copies and maintain support and audit records;
- operate configured sticky messages, panels, staff statistics, and reward calculations;
- prevent duplicate or unauthorized bounty actions and maintain bounty funding and Forum-post state; and
- diagnose failures and preserve operational continuity across bot restarts.

## Where information is stored and who can access it

Live tickets, private staff-notes threads, ticket log messages, and transcript attachments are stored through Discord and are visible according to the permissions of their destination channels, threads, or direct messages.

The bot also stores operational data outside Discord on its Railway-hosted service and attached storage. This can include configuration JSON, ticket statistics and intake records, bounty records, plaintext ticket and staff-note transcript files, and uploaded ticket-panel or proof media.

Railway provides protection at the hosting and storage-provider layer, including storage-layer encryption. STARZ Ticket Bot does not separately encrypt each JSON, transcript, or media file in its own application code. The bot uses private-channel permissions, role-gated staff actions, upload type and size checks, filename and path validation, and signed service-to-service requests for supported bounty operations. Authorized STARZ staff and the bot owner may access records needed to operate, support, or troubleshoot these features. Discord and Railway process data as platform and hosting providers, and supported bounty data may be exchanged with the connected STARZ Minigames service.

## Transcripts and media

When a ticket is closed, the bot can read the ticket history and linked staff-notes history. A staff transcript can contain author names and Discord IDs, timestamps, message text, attachment filenames and Discord URLs, embed summaries, ticket metadata, close information, and staff notes. A separate player-safe transcript excludes the staff-notes section.

The full staff transcript is saved on the bot's hosted storage and is also sent to the configured Discord log channel when possible. A player-safe copy can be sent to the ticket opener by Discord direct message. Copies posted through Discord remain subject to Discord and server-channel retention and deletion controls.

Uploaded ticket evidence and panel media can be copied to hosted storage so the bot is not dependent on a temporary Discord attachment URL. Supported uploads are limited by configured file type and size checks.

## Retention

There is no single automatic expiration period for all STARZ Ticket Bot data.

Configuration, ticket statistics, intake answers, bounty records, successful proof uploads, panel media, and saved transcript files can remain until they are manually removed or a feature-specific clear or replacement action removes them. Removing the bot from a server or no longer using it does not automatically erase all stored records. Some temporary runtime values disappear when the bot restarts. Anti-replay receipt nonces used by the signed bounty-funding bridge are automatically pruned after 24 hours, but that limit does not apply to the underlying bounty record.

## Deletion requests and choices

To request deletion or ask a privacy question, open a support ticket in the [STARZ Discord server](https://discord.gg/STARZ) and ask to contact the bot owner. Identify **STARZ Ticket Bot** and describe the account, server, ticket, transcript, media, or other data you want reviewed for deletion.

Requests are handled manually. The bot owner may need to verify that the requester controls the relevant Discord account or is authorized for the relevant server or record. No fixed response or deletion deadline is currently promised.

Deleting information required by a configured feature may prevent that feature from working until the required information is supplied again. Deletion does not create a permanent exclusion from the bot, and later use can create new records.

The bot does not provide one universal per-user switch that opts an account out of all message-content processing while continuing to use message-dependent ticket features. Server administrators can restrict the channels the bot can access and can disable or avoid supported features. Users can avoid optional uploads and bounty submissions, but messages submitted inside an active ticket may be included in that ticket's operational records and transcript.

## Policy updates

This policy will be updated when STARZ Ticket Bot's data practices materially change. Questions and deletion requests should be directed to the bot owner through a STARZ support ticket.
