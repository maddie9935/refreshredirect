# Automatic refresh and redirect demo

Demo pages for recording the user experience of automatic page refreshes and redirects, before and after the fix. The site is a made-up university registrar.

| Page | What it does |
| --- | --- |
| `index.html` | Links to all demo pages |
| `waitlist.html` | Error: reloads every 30 seconds, erasing form input and sending screen readers back to the top |
| `waitlist-fixed.html` | Fixed: a "Check for open seats" button updates seat counts and screen readers announce the result |
| `waiting-room.html` | Error: redirects to `register.html` 20 seconds after loading, without warning |
| `waiting-room-fixed.html` | Fixed: after 20 seconds, announces "It's your turn" with a link to continue |
| `register.html` | The registration form both waiting rooms lead to |
| `styles.css` | Shared styles |

## Changing the timing

- Refresh: in `waitlist.html`, change the `30` in `<meta http-equiv="refresh" content="30">`.
- Redirect: in `waiting-room.html`, change the `20` in `content="20;url=register.html"`.
- Fixed waiting room: in `waiting-room-fixed.html`, change `20000` (milliseconds) in the script.

To host it, push these files to a repo and turn on GitHub Pages (Settings > Pages > Deploy from branch > `main` / root).
