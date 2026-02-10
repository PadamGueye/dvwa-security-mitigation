# DVWA – Mitigation des vulnérabilités Web

## 📌 Contexte du projet
Ce projet s’inscrit dans le cadre du cours **INF-806 / IFT-509 – Systèmes et réseaux**.  
Il consiste à mettre en place une application web volontairement vulnérable (**Damn Vulnerable Web Application – DVWA**) puis à **mitiger ses failles de sécurité sans modifier directement le code de l’application**, en utilisant des mécanismes d’infrastructure et de sécurité intermédiaires.

L’objectif pédagogique est de comprendre :
- les vulnérabilités web courantes,
- les méthodes d’attaque (Red Team),
- les techniques de défense et de mitigation (Blue Team),
- l’impact réel des mesures de sécurité mises en place.

---

## 👥 Membres du groupe
- **Anicet**
- **Modeste**
- **Abdarazack**
- **Loic**
- **Adama**

Les attributions détaillées des tâches seront précisées dans le rapport final.

---

## 🎯 Objectifs du projet
- Déployer DVWA dans un environnement virtualisé
- Identifier et documenter les vulnérabilités (Red Teaming 1)
- Mettre en place des mécanismes de mitigation :
  - WAF via reverse proxy
  - Rate limiting
  - IPS (Snort / Suricata)
  - Outils de bannissement (Fail2ban / Crowdsec)
- Tester l’efficacité des mitigations (Red Teaming 2)
- Produire un rapport détaillé conforme au cahier des charges

---

## 🧱 Architecture générale (vue logique)
Client  
→ Reverse Proxy / WAF  
→ Machine virtuelle DVWA  
→ Base de données  

L’ensemble est déployé sur un réseau virtuel dédié.

---

## 🛠️ Technologies et outils envisagés
- **DVWA** (Damn Vulnerable Web Application)
- **Machines virtuelles** (VirtualBox / VMware)
- **Outils Red Team** :
  - OWASP ZAP
  - Burp Suite
  - sqlmap
  - Wapiti
- **Outils Blue Team** :
  - Nginx (reverse proxy / WAF)
  - Snort ou Suricata
  - Fail2ban ou Crowdsec
- **Outils annexes** :
  - Wireshark
  - GitHub (gestion de projet et versioning)

---

## 📂 Structure du dépôt
```
.
├── apps
│   └── dvwa
│       ├── config
│       ├── database
│       ├── docs
│       └── src
├── infrastructure
│   ├── vm
│   ├── network
│   └── reverse-proxy
├── security
│   ├── red-teaming
│   ├── blue-teaming
│   ├── ips
│   └── waf
├── scripts
├── docs
│   ├── rapport
│   └── annexes
├── meeting-notes
└── README.md
```
---

## 🗓️ Organisation du travail
- Minimum **3 réunions par semaine**
- Suivi de l’avancement via les **Issues GitHub**
- Journal des réunions et milestones dans `meeting-notes/`
- Travail collaboratif avec validation collective des décisions techniques

---

## 📄 Livrables attendus
- Environnement DVWA fonctionnel
- Documentation des vulnérabilités identifiées
- Mise en place et configuration des mécanismes de mitigation
- Comparaison avant / après mitigations
- **Rapport final (PDF)** conforme aux consignes du cours

---

## 📚 Références
Les références utilisées (articles, documentations, outils) seront listées dans le rapport final.

---

## ⚠️ Remarque
Ce dépôt est utilisé exclusivement à des **fins pédagogiques**.  
DVWA est volontairement vulnérable et **ne doit jamais être exposée sur un réseau public**.
