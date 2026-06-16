# VPS Tutorial: How to Choose, Set Up, and Run Your First VPS — From Zero to Live Server (Complete Beginner's Walkthrough, with Plan Comparison & Cost Breakdown)

If you've ever googled "VPS tutorial" and ended up staring at a wall of jargon about kernel parameters and iptables rules — welcome. You're in the right place, and we're going to skip the scary parts first and get you oriented.

A VPS, or Virtual Private Server, is basically a slice of a real physical server that's been carved out just for you. You get your own RAM, your own CPU threads, your own storage. No sharing with the neighbor who decides to run a cryptocurrency miner at 3am. It's not a dedicated server (which would cost you hundreds a month), and it's definitely not shared hosting (where everyone's on the same machine and your site slows down when someone else gets a traffic spike). It's the middle ground — and honestly, for most independent developers, small teams, and side projects, it's exactly what you need.

This VPS tutorial walks you through everything: what a VPS actually is, when you need one, how to pick a provider, and how to actually get one running. We'll use as our example provider throughout — a Malaysia-based cloud host founded in 2020 that's made a name for itself by doing one thing unusually well: squeezing absurdly high CPU clock speeds into budget-friendly VPS plans.

---

## What Is a VPS, and Do You Actually Need One?

Let's keep this real. You probably don't need a VPS if you're running a simple WordPress blog that gets 200 visitors a month. Shared hosting handles that fine, and it's cheaper.

But you probably *do* need a VPS if:

- You're running an app that needs persistent processes (bots, APIs, background workers)
- Your shared hosting keeps throwing 503 errors when traffic spikes
- You need root access to install custom software
- You're hosting multiple small projects and shared hosting limits are getting in the way
- You're learning Linux and want a real environment to experiment in

A VPS gives you **full root access**. You install what you want, configure it how you want, restart services when you want. It's real Linux, on real hardware, that happens to be in a data center somewhere — accessible from your laptop anywhere in the world via SSH.

---

## Step 1: Understanding the Specs — What to Look For

Before picking a plan, here's what those numbers actually mean:

**CPU Cores & Clock Speed**

Most budget VPS providers compete on core count. Evoxt takes a different approach — they compete on clock speed. Their VMs run at up to 6.0 GHz. For context, most providers are shipping VMs running at 2.2–2.4 GHz. That gap is not small. For web servers, database queries, and anything single-threaded, a faster clock matters more than having 8 slow cores.

**RAM**

For a simple web app or bot, 1–2 GB is workable. For anything running a database alongside an application server, 4 GB is a comfortable baseline. Don't go below 512 MB unless you're running something very minimal — you'll spend half your time managing swap space.

**Storage**

SSD is the only reasonable choice in this era. Evoxt uses SSD across all plans, which handles most workloads well. For storage-heavy use cases (media servers, databases with lots of data), pay attention to the GB numbers.

**Bandwidth / Monthly Transfer**

This is how much data your server can send and receive each month. A typical small web app won't get close to 1 TB/month. But if you're serving video, doing heavy file transfers, or running a game server, track this carefully. Evoxt charges $3/TB overage on standard plans.

**Location (Region)**

Pick the region closest to your primary users. Latency matters for interactive applications. For users in Asia, Evoxt's Hong Kong, Japan, and Malaysia options are worth considering. For US or European audiences, they have standard regions there too.

---

## Step 2: Picking an Evoxt Plan

Evoxt organizes plans into three network tiers:

- **Standard** — US, UK, Canada, Germany, Poland, Amsterdam, Japan (Tokyo), Malaysia, Australia
- **Premium Network** — Hong Kong and Japan (Osaka), with higher-quality routing but lower included transfer
- **Premium Plus** — Malaysia only, with a premium network path and pricing to match

Here's the full Standard tier lineup:

### 🌐 Standard Network Plans

| Plan | CPU | RAM | Storage | Monthly Transfer | Price | Link |
|------|-----|-----|---------|-----------------|-------|------|
| VM-0.5 | 1 core (up to 6.0 GHz) | 512 MB | 5 GB | 500 GB | $2.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-0.75 | 1 core (up to 6.0 GHz) | 1 GB | 10 GB | 750 GB | $4.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-1 | 1 core (up to 6.0 GHz) | 2 GB | 20 GB | 1000 GB | $5.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-1.5 | 2 cores (up to 6.0 GHz) | 2 GB | 20 GB | 1500 GB | $6.95/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-2 | 2 cores (up to 6.0 GHz) | 4 GB | 30 GB | 2000 GB | $11.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-3 | 4 cores (up to 6.0 GHz) | 4 GB | 30 GB | 3000 GB | $14.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-4 | 4 cores (up to 6.0 GHz) | 8 GB | 60 GB | 4000 GB | $23.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-6 | 8 cores (up to 6.0 GHz) | 8 GB | 60 GB | 5000 GB | $29.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-8 | 8 cores (up to 6.0 GHz) | 16 GB | 80 GB | 6000 GB | $47.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-12 | 16 cores (up to 6.0 GHz) | 16 GB | 80 GB | 8000 GB | $60.95/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-16 | 16 cores (up to 6.0 GHz) | 32 GB | 100 GB | 10 TB | $95.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |

### 🇭🇰🇯🇵 Premium Network Plans (Hong Kong & Japan Osaka)

| Plan | CPU | RAM | Storage | Monthly Transfer | Price | Link |
|------|-----|-----|---------|-----------------|-------|------|
| VM-0.5 | 1 core (up to 6.0 GHz) | 512 MB | 5 GB | 250 GB | $2.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-0.75 | 1 core (up to 6.0 GHz) | 1 GB | 10 GB | 250 GB | $4.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-1 | 1 core (up to 6.0 GHz) | 2 GB | 20 GB | 500 GB | $5.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-1.5 | 2 cores (up to 6.0 GHz) | 2 GB | 20 GB | 500 GB | $6.95/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-2 | 2 cores (up to 6.0 GHz) | 4 GB | 30 GB | 1000 GB | $11.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-3 | 4 cores (up to 6.0 GHz) | 4 GB | 30 GB | 1000 GB | $14.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-4 | 4 cores (up to 6.0 GHz) | 8 GB | 60 GB | 2000 GB | $23.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-6 | 8 cores (up to 6.0 GHz) | 8 GB | 60 GB | 2000 GB | $29.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-8 | 8 cores (up to 6.0 GHz) | 16 GB | 80 GB | 3000 GB | $47.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-12 | 16 cores (up to 6.0 GHz) | 16 GB | 80 GB | 3000 GB | $60.95/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-16 | 16 cores (up to 6.0 GHz) | 32 GB | 100 GB | 5000 GB | $95.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |

### 🇲🇾 Premium Plus Network Plans (Malaysia Premium)

| Plan | CPU | RAM | Storage | Monthly Transfer | Price | Link |
|------|-----|-----|---------|-----------------|-------|------|
| VM-0.5 | 1 core (up to 6.0 GHz) | 512 MB | 5 GB | 150 GB | $3.49/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-0.75 | 1 core (up to 6.0 GHz) | 1 GB | 10 GB | 250 GB | $4.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-1 | 1 core (up to 6.0 GHz) | 2 GB | 20 GB | 300 GB | $5.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-1.5 | 2 cores (up to 6.0 GHz) | 2 GB | 20 GB | 300 GB | $6.95/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-2 | 2 cores (up to 6.0 GHz) | 4 GB | 30 GB | 600 GB | $11.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-3 | 4 cores (up to 6.0 GHz) | 4 GB | 30 GB | 700 GB | $14.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-4 | 4 cores (up to 6.0 GHz) | 8 GB | 60 GB | 1000 GB | $23.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-6 | 8 cores (up to 6.0 GHz) | 8 GB | 60 GB | 1250 GB | $29.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-8 | 8 cores (up to 6.0 GHz) | 16 GB | 80 GB | 2000 GB | $47.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-12 | 16 cores (up to 6.0 GHz) | 16 GB | 80 GB | 2500 GB | $60.95/mo | 👉 [Deploy](https://bit.ly/Evoxt) |
| VM-16 | 16 cores (up to 6.0 GHz) | 32 GB | 100 GB | 4000 GB | $95.99/mo | 👉 [Deploy](https://bit.ly/Evoxt) |

> **Quick guide for beginners:** Not sure which plan to start with? If it's your first VPS and you just want to learn the ropes, the VM-0.75 at $4.99/mo (1 GB RAM, 1 core) is a decent starting point. For a real app or API, go with VM-1 (2 GB RAM) at $5.99/mo. You can always scale up later — Evoxt lets you add individual resources like CPU cores, RAM, or extra IPs without switching plans.

There's also a verified promo code floating around: **AFF1129-hostspot** for a recurring 40% discount on VM-1 and above. Apply it at checkout.

---

## Step 3: Setting Up Your VPS — The Actual Tutorial Part

Alright, you've signed up, picked a plan, and you've got a VM provisioned. Your welcome email (or control panel) has your server's IP address, your root password, and your operating system — almost certainly some flavor of Linux. Let's connect.

### Connecting via SSH

SSH (Secure Shell) is how you talk to your server from your laptop. It's like a remote terminal.

**On macOS or Linux:** Open your Terminal app and run:

bash
ssh root@YOUR_SERVER_IP


Replace `YOUR_SERVER_IP` with the actual IP address from your control panel. Hit enter, type `yes` when asked about the fingerprint, then enter your root password.

**On Windows:** Use Windows Terminal with OpenSSH (built into Windows 10 and 11), or download PuTTY. In PuTTY, enter your server's IP in the Host Name field, keep port 22, and click Open.

Once you're in, you'll see a prompt like `root@hostname:~#`. You're inside your server. Welcome.

### First Things First: Update the System

Before doing anything else, update your packages. On Ubuntu or Debian:

bash
apt update && apt upgrade -y


On CentOS or AlmaLinux:

bash
dnf update -y


This installs the latest security patches. Not optional — skip it and you're leaving known vulnerabilities in place.

### Create a Non-Root User

Running everything as root is like doing your daily browsing as an administrator. If you fat-finger a command, you can delete the entire filesystem. Create a normal user with sudo access:

bash
adduser yourusername
usermod -aG sudo yourusername


Switch to that user going forward: `su - yourusername`. Run privileged commands with `sudo command` instead of just `command`.

### Set Up SSH Key Authentication

Passwords are fine to start, but SSH keys are better. On your *local machine* (not the server):

bash
ssh-keygen -t rsa -b 4096


This creates a key pair: a private key you keep (never share it) and a public key. Copy the public key to your server:

bash
ssh-copy-id yourusername@YOUR_SERVER_IP


Now you can log in without a password. After you confirm this works, you can optionally disable password login entirely by editing `/etc/ssh/sshd_config` and setting `PasswordAuthentication no`.

### Set Up a Basic Firewall

A VPS exposed to the internet will start getting port-scanning attempts within minutes of deployment. Not exaggerating. Set up UFW (Uncomplicated Firewall) on Ubuntu:

bash
sudo apt install ufw
sudo ufw allow OpenSSH
sudo ufw enable


This blocks everything except SSH. As you add services — web server, database, etc. — you'll open specific ports as needed.

---

## Step 4: Install Your First Web Server

Let's get something actually running. Install Nginx:

bash
sudo apt install nginx
sudo systemctl enable nginx
sudo systemctl start nginx


Then open port 80 in your firewall:

bash
sudo ufw allow 80
sudo ufw allow 443


Navigate to your server's IP address in a browser. You should see the default Nginx welcome page. That's your server, running, serving a page over the internet. Not bad for a few minutes of work.

From here you can deploy a static site, set up a reverse proxy to a Node.js app, host a Flask or Django application, or configure a WordPress installation with a database.

---

## Step 5: Things Worth Knowing Before You Run Into Them

**Backups:** Every Evoxt plan includes automatic weekly offsite backups. This is genuinely useful — your data survives even if their infrastructure has a catastrophic failure. That said, for important production data, consider running your own periodic backups too.

**Scaling:** If you outgrow your current plan, Evoxt lets you add resources incrementally. Extra IP address: $3/month. Extra vCore: $3/month. Extra GB of RAM: $2/month. You can also upgrade your entire plan without data loss.

**Monitoring:** Evoxt provides basic monitoring in their control panel — CPU usage, network, etc. For more serious setups, consider installing something like Netdata or Grafana to get visibility into what your server is doing.

**Billing:** Evoxt accepts credit cards, PayPal, Bitcoin, and USDT (Tron). You can prepay for up to 3 years and get credits applied automatically to future invoices — useful if you want to lock in pricing and not think about monthly renewals.

**VNC Access:** If you manage to misconfigure SSH and lock yourself out, Evoxt provides VNC access through their control panel. It's a browser-based console to your server. You'll thank them for this feature exactly once, at the worst possible moment.

---

## Who Is Evoxt Actually Good For?

Based on what we know about their infrastructure and positioning, Evoxt makes the most sense for:

- **Developers and indie hackers** who want solid CPU performance without paying cloud-provider prices
- **Users in Asia** who need good network routing to the region — their Hong Kong and Osaka nodes are premium-routed
- **People hosting CPU-intensive workloads** like web scraping, data processing, or game servers where single-core speed matters
- **Budget-conscious teams** running multiple projects who want predictable monthly pricing without overage surprises

It's probably not the first choice if you need managed database services, integrated CDN, or one-click WordPress hosting with cPanel. Evoxt is a self-managed VPS — you bring your knowledge, they bring the hardware.

---

## Summary

A VPS is one of those things that sounds intimidating until you actually use one — and then you wonder why you waited. The barrier is mostly psychological. SSH, a few Linux commands, and you're running real infrastructure for under six bucks a month.

👉 [Get started with Evoxt — plans from $2.99/month](https://bit.ly/Evoxt)

Start with the smallest plan that fits your needs. Worst case, you spend $3 and learn something. Best case, you've got a server running your project that'll scale with you as you grow.
