# Noillirk: data reference table

What [noillirk.pro](https://noillirk.pro/) stores for a guest player, who can see it and how it ends. Summarised from the [privacy page](https://noillirk.pro/privacy) on 2026-11-01.

| Data | Stored where / how | Who can see it | How it ends |
|---|---|---|---|
| Player identity | Signed, HttpOnly session cookie → random player ID | Only your browser | Clear cookies (loses link) or delete profile |
| Nickname | Server, on your profile | Leaderboards, room players | Change it, or delete profile |
| Flights, answers, scores, achievements | Server | You; answers shown to room players after each round closes; challenge recipients after they answer | Delete profile |
| Device link | One-time private code | Whoever you give it to | Single use |
| Unknown answers | Sent to AI judge (currently DeepSeek) with prompt + board context | — | Accepted verdicts cached by question and judge version |
| Room chat | Live room | Room players | Normally cleared after ~30 minutes; reported messages may be kept for moderation |
| Product events | Fixed action names, mode categories, coarse outcomes | — | No answers, nicknames, room codes or tracking IDs in browser events; respects DNT / GPC |
| Daily return category | First/latest UTC visit date in your browser only | — | Clear site data |

## Export and delete

Your profile has **export** and **permanent delete**. Deleting removes sessions, flights and achievements; a completed room may keep a pseudonymous historical result.

Infrastructure: hosting, records, rooms and background processing run on Cloudflare services.

Related: [connection-help.md](connection-help.md), [hosting-a-round.md](hosting-a-round.md).

Maintained by Chaozi, developer of noillirk.pro (independent; not affiliated with Daily, the creator of the original Noillirk).
