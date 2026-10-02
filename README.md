# bina-top-uptime

External uptime check for [bina.top](https://bina.top), run by GitHub Actions every 10 minutes.

- When the site does not answer (3 attempts, one minute apart), an issue labelled `site-down` is opened and the owner is notified.
- When it answers again, the issue is closed with a "back up" comment.
- `keepalive.yml` makes an empty commit once a month, because GitHub pauses scheduled workflows in repositories without activity for 60 days.

The forum server has its own, more detailed watchdog. This check covers the case where the whole server or its network is down.
