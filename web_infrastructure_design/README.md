<p align="center">
  <img src="./assets/banner.jpeg" alt="web_infrastructure_design Banner">
</p>

# web_infrastructure_design

> Because knowing how websites actually work is the difference between a developer and a wizard.

---

## 📝 Description

This project is a deep dive into web infrastructure design through whiteboarding exercises. Starting from a single-server LAMP stack all the way up to a scaled, secured, and monitored multi-server architecture, I designed and explained each infrastructure step by step — without a computer or notes. Each task required me to understand not just how things work, but *why* they are built that way, what can go wrong, and how to make them better. The deliverables are diagrams, hosted screenshots, and the ability to explain every component out loud.

---

## 🎯 Learning Objectives

By completing this project, I am able to draw and explain a complete web stack from memory, covering every layer from DNS resolution to database replication. I can explain the role of each component — web server, application server, load balancer, database — and describe how they interact. I understand what system redundancy means and why it matters for availability. I can identify single points of failure (SPOF) in an architecture and propose improvements. I also know the key acronyms used in the field: LAMP (Linux, Apache, MySQL, PHP/Python/Perl), SPOF (Single Point of Failure), and QPS (Queries Per Second). Finally, I am able to whiteboard any of these architectures in front of an audience in under 30 minutes, which is honestly more stressful than it sounds.

---

## 🛠️ Technologies Used

This project is technology-agnostic in terms of code — there is no code to run. The focus is on infrastructure concepts: Nginx as the web server, an application server layer, MySQL for the database (with Primary-Replica configuration), HAproxy as the load balancer, SSL certificates for HTTPS, firewalls for security, and monitoring clients such as Sumologic. Diagrams were created using whiteboarding tools and screenshots were hosted on Imgur.

---

## ⚙️ Requirements

- OS: Ubuntu 20.04 LTS
- No code to execute — this project is diagram and explanation based
- A `README.md` file at the root of the project is mandatory
- For each task: whiteboard the diagram, take a screenshot, upload it to an image hosting service, and insert the link into the answer file
- Each task will be manually reviewed and whiteboarded in front of a mentor, staff member, or student — no computer or notes allowed
- Keep answers focused: cover exactly what is asked, avoid being overly verbose

---

## 🚀 Installation

```bash
git clone https://github.com/GwenP88/holbertonschool-system_engineering-devops.git
cd holbertonschool-system_engineering-devops/web_infrastructure_design
```

---

## ▶️ Usage / Execution

This project does not contain executable scripts. Each task answer file contains a link to a hosted screenshot of the corresponding infrastructure diagram.

To review a task:

```bash
cat 0-simple_web_stack
cat 1-distributed_web_infrastructure
cat 2-secured_and_monitored_web_infrastructure
cat 3-scale_up
```

Each file contains the URL pointing to the diagram screenshot hosted online.

---

## 📊 Project Progress

<p align="center">
<img src="assets/progress_barre_100.gif" alt="Mandatory tasks progress" width="80%">
</p>

<p align="center">
<sub>Mandatory tasks completion: 100%</sub>
</p>

---

## ✨ Features

### Task 0 - Simple Web Stack

- **Status:** Mandatory
- **Objective:** Design a single-server web infrastructure hosting `www.foobar.com` using a LAMP stack. Explain the role of each component: server, domain name, DNS record, web server, application server, and database.
- **Constraint:** Only one server allowed; must use `foobar.com` with a `www` A record pointing to IP `8.8.8.8`.
- **Expected behavior:** Be able to explain the full request flow from user to server, and identify the infrastructure's weaknesses: SPOF, downtime during deployments, and inability to scale under heavy traffic.

**Files:** `0-simple_web_stack`

---

### Task 1 - Distributed Web Infrastructure

- **Status:** Mandatory
- **Objective:** Design a three-server infrastructure for `www.foobar.com` with a load balancer (HAproxy), two servers each running Nginx, an application server, the codebase, and a MySQL database.
- **Constraint:** Must explain the purpose of every added element, the load balancer's distribution algorithm, Active-Active vs Active-Passive setup, and how a Primary-Replica database cluster works.
- **Expected behavior:** Be able to identify remaining SPOFs, security issues (no firewall, no HTTPS), and the absence of monitoring.

**Files:** `1-distributed_web_infrastructure`

---

### Task 2 - Secured and Monitored Web Infrastructure

- **Status:** Mandatory
- **Objective:** Extend the three-server infrastructure to serve `www.foobar.com` over HTTPS, with 3 firewalls and 3 monitoring clients (e.g. Sumologic).
- **Constraint:** Must explain why each element was added, how monitoring works, how to track QPS, and describe the infrastructure's remaining issues: SSL termination at the load balancer, single write-capable MySQL node, and identical component stacking on all servers.
- **Expected behavior:** A secured, encrypted, and monitored architecture with clear understanding of its trade-offs.

**Files:** `2-secured_and_monitored_web_infrastructure`

---

### Task 3 - Scale Up

- **Status:** Advanced
- **Objective:** Scale the infrastructure by adding a dedicated server, configuring HAproxy as a clustered load balancer, and splitting web server, application server, and database onto their own separate servers.
- **Constraint:** Must justify every added element.
- **Expected behavior:** A fully separated, horizontally scalable architecture where each component runs independently — because putting everything on one server is fine until it really, really isn't.

**Files:** `3-scale_up`

---

## 🤝 Contributions & Acknowledgements

Thanks to the Holberton School team for making me draw the same server diagram four times until I understood why redundancy matters. Thanks also to every Stack Overflow thread and RFC that helped clarify what DNS actually does at 2am. You are all heroes.

---

## 👤 Author

**Gwenaelle PICHOT**
- Student at Holberton School
- Track: holbertonschool-system_engineering-devops
- Project: web_infrastructure_design
- GitHub: [@GwenP88](https://github.com/GwenP88)