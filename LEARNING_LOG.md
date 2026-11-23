# Learning Log
 
A running record of what I've actually worked through, in order. I'm
logging this the way I'd want to read someone else's: specific enough to
verify, honest about what's still in progress, no padding.
 
---
 
## Access control, start to finish
 
I just closed out PortSwigger's Web Security Academy **Access Control**
track — all 13 labs, apprentice through expert. That topic ended up being
a better crash course in *why* authorization bugs exist than any single
writeup could have given me, because it forces you through every shape of
the same root failure instead of just reading about one example:
 
- **Unprotected admin functionality** — found through a leaked `robots.txt`
  entry in one lab and through a JS source reference in another. Same bug,
  two different ways an app accidentally tells you where the door is.
- **Role controlled by something the client can edit** — a role flag
  sitting in a cookie, and separately one sitting in a JSON body the
  frontend wasn't supposed to let you touch. The lesson that stuck: if the
  *server* isn't the one deciding your role on every request, the client
  will eventually be asked to decide it for you.
- **URL-based and method-based control that only checks one path or one
  verb** — the same resource, reachable through a route or an HTTP method
  nobody thought to gate the same way as the "front door" route.
- **Multi-step processes missing a check on one step** — this is the one
  I keep coming back to, because it's the least "scanner-findable" of the
  set. Nothing about any single request looks wrong; the bug only exists
  in the gap between steps.
- **Referer-based access control** — a header the client fully controls,
  used as if it were a trust signal. Trivial to bypass, and a good
  reminder to distrust anything sent *by* the party whose access you're
  trying to restrict.
None of these are exotic. That's the point — this is what the inside of
most real broken-access-control reports looks like, not a novel parser
bug. It's exactly the category OWASP has ranked #1 on the Web Top Ten
since 2021, and exactly why it's where I'm starting.
 
**What this connects to:** I'd already been writing up my own notes on
IDOR/BOLA and broken access control before this (a field-manual document
I've been building out), and going through PortSwigger's labs in parallel
sharpened that document more than writing it in isolation did — seeing
the same failure mode implemented four different ways makes the pattern
stick in a way a single definition doesn't.
 
**What's next, honestly labeled as not done yet:**
- Working through HackingHub's *Hacking APIs* course — currently in the
  authorization section (IDOR & BOLA, Nested Resource Authorization,
  Response Property Authorization, Mass Assignment, Function-Level
  Authorization) that this PortSwigger track maps onto almost one-to-one,
  just at the API layer instead of the web-app layer.
- Reading *Hacking APIs* (Corey Ball) and *Black Hat GraphQL* alongside
  the course, not after it.
- Running the same authorization-testing instinct against my homelab
  stack — crAPI, vAPI, VAmPI, DVGA, OWASP Juice Shop — once I'm further
  into the API-specific material, so the technique transfers from "I can
  do this in a browser lab" to "I can do this against a raw API with no
  UI holding my hand."
I'll log the next milestone when there's an actual one to report, not on
a schedule.
 
