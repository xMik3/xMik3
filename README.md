CE student in Athens.

## Projects

### [oasa-accuracy](https://github.com/xMik3/oasa-accuracy)

How accurate are Athens bus ETAs, and what kind of model is behind them?

I built a Node collector that polls OASA's live feed every 45 seconds and
saves everything to MySQL. It ran from the start of August to the end of September 
and collected 1.92 million predictions. A pandas pipeline then works out when each bus
actually arrived and compares that to every prediction made about it.

### [unisys](https://github.com/xMik3/unisys)

University management system REST API in TypeScript, built around three roles.
Students browse the course catalogue, register for courses and see their
grades. Teachers see the courses they have been assigned and grade the
students registered in them. A Secretary sits above both, with full CRUD
over students, teachers and courses, assigning teachers to courses.

### homelab

The server the oasa-accuracy project actually ran on. Everything is
containerized behind Traefik with Let's Encrypt TLS, and internal access goes over
WireGuard. Grafana sits on top of Prometheus
and node-exporter for host metrics, Traefik access logs for who is probing
what, and CrowdSec for intrusion detection.

I built it to host my own services and it turned into the most useful thing
I have learned outside a course.

### opencart

I was setting up OpenCart on my server to test some features for someone
I know who runs a pharmacy on it. The install died on the schema step. Two
rows in the setup SQL had six values against five columns, so MySQL
rejected the whole INSERT and nothing after it got created. I
traced it, fixed it, [opened a PR](https://github.com/opencart/opencart/pull/15364)
which got merged upstream.

---

**Stack:** TypeScript/Node, Python, MySQL, Docker

**Reach me:** ieronymidismichael@gmail.com
