# Week 3 – Student Exercise: Networking Basics (Internal vs External Access)

Complete this lab on your own VM.

---

## Task summary

Your Week 3 exercise is to prove to yourself that:

- the app can be reachable internally and externally
- external access depends on port rules

---

## Step-by-step (on your VM via SSH)

### 1) Check your private IP
Run:
```bash
hostname -I
````

Note the private IP that looks like `10.x.x.x` or `192.168.x.x`.

---

### 2) Confirm Velo-learn is running in PM2

Run:

```bash
pm2 list
```

If the app is not running, start it:

```bash
cd /home/azureuser/Velo-learn
pm2 start npm --name velo-learn -- start
pm2 save
```

---

### 3) Test local access from the VM

Run:

```bash
curl http://localhost:3000
```

You should see HTML output.

Write down: **Local curl works.**

---

## Step-by-step (from your laptop)

### 4) Find your VM public IP

In the portal, locate the VM **Public IP address**.

---

### 5) Test external access in your browser

From your laptop browser, open:

```text
http://<YOUR_PUBLIC_IP>:3000
```

If the app loads, the port rule already exists.
If it fails, you will add the rule in the next step.

---

## Step-by-step (portal networking rule)

### 6) Add an inbound NSG rule for port 3000 (if needed)

In the portal:

* VM → Networking (or the VM’s NSG) → Inbound rules
* Add an inbound rule:

  * **Protocol:** TCP
  * **Port:** 3000
  * **Source:** Any (for training) or your own IP (preferred)
  * **Action:** Allow
  * **Priority:** choose a valid priority that does not conflict
  * **Name:** `allow-tcp-3000`

Then test again from your laptop:

```text
http://<YOUR_PUBLIC_IP>:3000
```

---

## Break it and fix it (required)

### 7) Break external access

Disable or delete the inbound rule for port 3000.

Then confirm:

* On VM (should still work):

```bash
curl http://localhost:3000
```

* On laptop (should fail):

```text
http://<YOUR_PUBLIC_IP>:3000
```

### 8) Fix external access

Recreate or re-enable the inbound rule for port 3000.

Then confirm again:

* On laptop (should work):

```text
http://<YOUR_PUBLIC_IP>:3000
```

---

## What to submit

Submit your Week 3 work in `cloud-devops-submissions` under:

`week-03/`

Include:

* `notes.md`
* `screenshots/`

---

## Notes to include in `notes.md`

1. Your private IP (from `hostname -I`)
2. Your public IP (from the portal)
3. A short results summary in this format:

**When port 3000 was allowed in the NSG**

* `curl http://localhost:3000` from VM: <result>
* Browser to `http://PUBLIC_IP:3000` from laptop: <result>

**When port 3000 was blocked in the NSG**

* `curl http://localhost:3000` from VM: <result>
* Browser to `http://PUBLIC_IP:3000` from laptop: <result>

---

## Screenshots required

Add these screenshots to `week-03/screenshots/`:

1. `pm2 list` output
2. NSG inbound rule showing the allow rule for TCP 3000 (rule name and port visible)

This lab links app health (PM2 + local curl) to network access (NSG rules + external browser access).
