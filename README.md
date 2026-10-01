<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="remind.me.at landing page" width="880">
  </picture>
</p>

# remind.me.at

Reminders for the things that quietly expire.

Remind tracks warranties, renewals, registrations and filings. Set the rule once and it fires at your local time, even across daylight saving, with delivery to a channel you already read. It is strict on purpose: if it cannot follow a rule exactly, it names the unsupported part and saves nothing, instead of quietly scheduling a reminder that goes wrong on a date nobody is watching.

## Features

- **Real recurrence rules**: a closed RRULE subset (`FREQ`, `INTERVAL`, `BYDAY`, `UNTIL`, `COUNT`), with unsupported parts rejected by name.
- **Time-zone aware**: every reminder stores an IANA time zone and a wall-clock time, so "09:00 every Monday" stays at nine across daylight saving.
- **Phrase entry and a rule builder**: write a reminder in a small, closed grammar or build the rule visually; both produce the same RRULE subset.
- **Verified delivery**: email or webhook targets that receive nothing until they are confirmed.
- **Quiet hours, snooze and redeliver**: a reminder due at 3am can wait until you are awake.
- **Calendar export**: ICS export and a calendar feed, so reminders show up in the calendar you already use.
- **Fire history**: each reminder keeps a record of when it fired.
- **Heartbeat monitoring**: the scheduler checks in with a monitor outside the network, so a stalled scheduler gets noticed.

## Built with

- Next.js 16 (App Router) and React 19
- TypeScript
- Tailwind CSS 4
- iCalendar (ICS) export
- Better Auth (shared me.at account)

## Part of the me.at family

remind.me.at is one of the [`*.me.at`](https://me.at) apps by Trevor McDougald. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

See [LICENSE](LICENSE).
