CE student in Athens.

## Projects

### [oasa-accuracy](https://github.com/xMik3/oasa-accuracy)

How accurate are Athens bus ETAs, and what kind of model is behind them?

I built a Node collector that polls OASA's live feed every 45 seconds and
saves everything to MySQL. It has been running since the 27th of July 2026 and has collected
744k predictions so far. A pandas pipeline then works out when each bus
actually arrived and compares that to every prediction made about it.

### [unisys](https://github.com/xMik3/unisys)

A REST API for a university management system, built around three roles.
Students browse the course catalogue, register for courses and see their
grades. Teachers see the courses they have been assigned and grade the
students registered in them. A Secretary sits above both, with full CRUD
over students, teachers and courses, assigning teachers to courses.

[Try it live in Swagger](https://unisys.250724.xyz/docs)

### homelab

The server the two projects above actually run on. Everything is
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

**Stack:** JavaScript/Node, Python, MySQL, Docker

**Reach me:** ieronymidismichael@gmail.com
