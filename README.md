<div align="center"> <img src="./assets/banner.svg" alt="0xLum1s — API Security Researcher, Access Control & Logic Flaws" width="100%"/> <br/> <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2800&pause=900&color=00E5FF&center=true&vCenter=true&width=700&lines=Authorization+is+a+claim.+I+test+the+claim.;BOLA+%2F+IDOR+%2F+BFLA+%2F+Mass+Assignment;JWT+%26+OAuth+logic+%2F+GraphQL+%2F+Race+Conditions;Every+403+is+a+hypothesis%2C+not+an+answer." alt="typing banner" />

X Medium

</div>
whoami

I'm Lum1s — a pseudonymous security researcher specializing in API security, broken access control, and application logic flaws. I don't chase CVEs in libraries; I chase the gap between what an API's documentation promises and what its authorization code actually checks. Most of what I find isn't a parser bug — it's a server that trusted a request it should have re-verified.

$ cat ./philosophy.txt
A 403 tells you a rule exists.
It doesn't tell you the rule is enforced everywhere that object is reachable.
Find every door. Then check who's actually guarding each one.
./specialties.sh
<table> <tr> <td width="50%" valign="top">

Authorization & Object-Level

IDOR / BOLA — horizontal & vertical
Broken Function-Level Authorization (BFLA)
Mass assignment / hidden-parameter injection
HTTP Parameter Pollution for auth bypass
</td> <td width="50%" valign="top">

Auth & Session Logic

JWT: alg confusion, key-trust failures, claim validation
OAuth / SSO: redirect validation, flow integrity, scope abuse
Session lifecycle & token-reuse flaws
</td> </tr> <tr> <td width="50%" valign="top">

Business Logic

Multi-step workflow abuse (checkout, onboarding, recovery)
Race conditions on limited/one-time resources
Rate-limit & idempotency-key abuse
</td> <td width="50%" valign="top">

API-Specific Surfaces

GraphQL: introspection, batching/aliasing, operation cost
Webhook signature & replay validation
SSRF via server-side fetch features
</td> </tr> </table>
./currently.sh
🔭 Working through the Hacking APIs course (HackingHub) — 64 lessons end to end, from HTTP fundamentals through JWT/OAuth, IDOR & BOLA, GraphQL, and full cross-API chaining
📘 Reading Hacking APIs (Corey Ball) and Black Hat GraphQL in parallel with the above
✅ PortSwigger Web Security Academy — Access Control track: labs complete
🧪 Homelab rotation: crAPI, vAPI, VAmPI, OWASP Juice Shop, DVGA — every new technique gets tried against a deliberately-vulnerable target before it touches anything in scope
🌱 Currently formalizing my own recon → authorization-matrix → chaining methodology into reusable, publishable notes (see pinned repos)
./arsenal.sh
<div align="center">

Show Image Show Image Show Image Show Image Show Image Show Image Show Image Show Image

</div>

Recon-to-report stack: subfinder · httpx · katana · Arjun / x8 · Schemathesis · RESTler for schema-driven and sequence-aware fuzzing, interactsh / Burp Collaborator for out-of-band confirmation, and a phone-first field kit (CatSuite on Android, paired to a desktop bridge when I need heavier tooling) so a hunt doesn't stop when I'm away from a laptop.

./stats.sh
<div align="center"> <img height="165" src="https://github-readme-stats.vercel.app/api?username=0xLum1s&show_icons=true&theme=dark&hide_border=true&bg_color=0a0e14&title_color=00e5ff&icon_color=00e5ff&text_color=7fa8b8"/> <img height="165" src="https://github-readme-streak-stats.herokuapp.com/?user=0xLum1s&theme=dark&hide_border=true&background=0a0e14&ring=00e5ff&fire=00e5ff&currStreakLabel=00e5ff"/> </div>
<div align="center">

<sub>Every finding here started as a question: <b>"who checked that this user is allowed to do this?"</b> — and then went and checked.</sub>

</div>

<!--
**0xLum1s/0xLum1s** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
