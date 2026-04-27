# SRE + AI Learning Journey — Master Document

> **The single source of truth for the next 9 months.**
> Save this to your repo as `MASTER_SYLLABUS.md`. Open it every session.

---

## Quick reference dashboard

| What | Value |
|------|-------|
| **Start date** | Wednesday |
| **Duration** | 200 days · 9 months · 8 phases · 40 weeks |
| **Daily commitment** | ~60–70 min weekday, 90 min Saturday (parallel track) |
| **Total weekly commitment** | ~7 hours |
| **Projects to build** | 9 production-grade projects |
| **Certifications** | CCA (Claude Certified Architect) + NCP-AIO (NVIDIA) |
| **Repo** | `sre-learning-journal` on your GitHub |
| **Tools** | Mac · VS Code · Terminal · Claude.ai · GitHub |

## How to use this document

This document has 3 main parts:

1. **Master Syllabus** — every day from Day 1 to Day 200. Tables. Reference material.
2. **Parallel Track** — classic SRE system design via Alex Xu book, Saturday mornings
3. **Week 1 Full Detail** — the format every future week will follow when expanded

**Daily session protocol:**
1. Open VS Code with `linux/weekX/dayXX.md` and integrated terminal
2. Find today's row in the Master Syllabus
3. Read theory · Type all examples · Complete all challenges
4. Write in `dayXX.md`: outputs, surprises, confusion, answers
5. Commit and push: `git commit -m "feat(<phase>): Week X Day Y — <topic>"`

**Session opener for every new chat with Claude:**
> "I am on Week X Day Y — [topic]. Yesterday I covered [X]. Continue."

**Sunday check-in every week without fail:**
> "Week X done. Completed: [list]. Skipped: [honest]. Hardest: [topic]. Capstone: done/not. Please assess readiness for Week X+1."

---

# PART 1 — Master Syllabus (Day 1 to Day 200)

> **200 Days · 8 Phases · 9 Projects · 2 Certifications**
> Linux → Git → Python → DSA → SRE Automation → GenAI → AI Design → CCA + NCP-AIO
> Started: April 2026 | Machine: Mac | Tools: VS Code + Terminal + Claude.ai

---

## How to use this syllabus

Every session: open `dayXX.md` in VS Code, work through theory, type all examples in terminal, complete all challenges, commit to GitHub. Only then move to the next day.

**Session opener for every new chat with Claude:**
> "I am on Week X Day Y — [topic]. Yesterday I covered [X]. Continue."

**Sunday check-in every week:**
> "Week X done. Completed: [list]. Skipped: [honest]. Hardest: [topic]. Capstone: done/not. Please assess readiness for Week X+1."

---

## The 9 Projects

| Month | Phase | Project |
|-------|-------|---------|
| M1 | Linux | `log-parser-toolkit.sh` — 5 bash one-liners for real log analysis |
| M2 | Bash | SRE Bash Toolkit — health report, watchdog, log alerter, disk cleaner, network checker |
| M3a | Git | `sre-learning-journal` — 200 commits, your complete learning portfolio |
| M3b | Python | `log-analyzer.py` — CLI tool, argparse, regex parsing, level filtering |
| M4 | Python | `api-health-checker.py` — concurrent endpoint checker, JSON reports, pytest + CI |
| M5 | DSA | 10 LeetCode Easy solved with Big O analysis and pattern documentation |
| M6 | SRE Python | `k8s-health-dashboard.py` — K8s + Prometheus + rich terminal UI |
| M7 | GenAI | `sre-ai-assistant/` — MCP + RAG + LangGraph + LangSmith + human-in-the-loop |
| M8 | AI Design | `ai-system-design-doc.md` — production RAG system, cost model, runbooks |
| M9 | Certs | CCA + NCP-AIO certifications earned |

---

## Parallel Track — Classic SRE System Design

**Runs alongside Month 5 onwards. Do not skip this.**

The 200-day syllabus covers **AI system design** deeply (Phase 7: latency, GPU ops, RAG at scale, LLM observability). But SRE interviews at Apple, Google, Meta, Netflix all ask **classic system design** — "Design TinyURL", "Design WhatsApp", "Design a rate limiter". That's a gap we fill in parallel, not inline, because system design is best learned through drawing + explaining, not from syllabus cells.

### The method — 1 design per weekend, Saturday morning, 90 minutes

1. Read one chapter of *System Design Interview Vol 1* (Alex Xu) during the week — 20 min/day
2. Saturday morning: **close the book**. Open Excalidraw or pick up a notebook. Solve the same design problem from scratch, drawing the architecture, estimating numbers, stating tradeoffs out loud
3. Compare your solution to the book's solution. Note the gaps in a `system-design/` folder in your repo
4. Commit your Excalidraw export or notebook photo to `system-design/weekXX-design.md`
5. Next weekend, pick the next chapter

### Books — buy these before Month 5

| Book | Why | When |
|------|-----|------|
| **System Design Interview Vol 1** — Alex Xu | The 15 most-asked SRE/backend design questions | Primary reading Weeks 19–34 |
| **Designing Data-Intensive Applications** — Martin Kleppmann | The depth reference on distributed systems, consistency, replication | Read alongside, look up specific chapters as needed |

### 15-week reading plan (Week 19 = Month 5 start)

| Study Week | Syllabus Week | Xu Ch | Design problem to whiteboard |
|------------|---------------|-------|------------------------------|
| 1 | W19 | 1 | Scale from zero to millions of users |
| 2 | W20 | 2 | Back-of-envelope estimation practice |
| 3 | W21 | 3 | Framework for system design interviews |
| 4 | W22 | 4 | Design a rate limiter |
| 5 | W23 | 5 | Design consistent hashing |
| 6 | W24 | 6 | Design a key-value store |
| 7 | W25 | 7 | Design a unique ID generator in distributed systems |
| 8 | W26 | 8 | Design a URL shortener (TinyURL) |
| 9 | W27 | 9 | Design a web crawler |
| 10 | W28 | 10 | Design a notification system |
| 11 | W29 | 11 | Design a news feed system |
| 12 | W30 | 12 | Design a chat system (WhatsApp) |
| 13 | W31 | 13 | Design a search autocomplete system |
| 14 | W32 | 14 | Design YouTube |
| 15 | W33 | 15 | Design Google Drive |

By Month 8 (Week 33), you will have whiteboarded 15 production-grade classic designs. Combined with your Phase 7 AI system design work, you'll be able to handle either flavor of design interview Apple throws at you.

### The weekend rhythm

- **Saturday 9:00–10:30am** — system design whiteboard session (90 min, offline, no AI help)
- **Saturday evening** — commit your drawing + notes to `system-design/` folder
- **Sunday check-in** includes the design you completed that week

This track adds **1.5 hours/week** to your commitment. It's the difference between passing SRE interviews and getting stuck on "Design Twitter" after mastering Linux and Python.

### Topics you'll learn through these 15 designs

- Load balancing (L4 vs L7, sticky sessions)
- Caching (CDN, Redis, write-through vs write-back)
- Database scaling (sharding, replication, leader election)
- Message queues (Kafka, RabbitMQ, SQS)
- CAP theorem, consistency models, PACELC
- Microservices: API gateway, service mesh, saga pattern
- Back-of-envelope math (QPS, storage, bandwidth)
- Distributed IDs (Snowflake, UUID)
- Consistent hashing
- Rate limiting algorithms (token bucket, leaky bucket)

None of these are in the 200-day plan. All of them will come up in your job interviews. This parallel track closes that gap.

---

## Rules (locked, non-negotiable)

- **Never copy-paste code** — type every command, every line
- **Struggle first** — minimum 10 minutes before asking for help
- **Commit every day** — every session ends with a git commit
- **No skipping capstones** — every capstone completed before advancing
- **No calendar advancing** — advance when YOU can write it from scratch
- **Sunday check-in** — every week without exception
- **Exit note** — 3 sentences in dayXX.md after every session

---

## Repo structure

```
sre-learning-journal/
  linux/week1/ through week8/
  git/week9-10/
  python/week11-18/
  dsa/week19-22/
  sre-python/week23-26/
  genai/week27-32/
  ai-design/week33-36/
  certs/week37-40/
  projects/
  interview-qa/
  README.md
```

---

# PHASE 1 — Linux, OS Internals & Bash Scripting
**Months 1–2 · Weeks 1–8 · 40 days**
**Goal:** Navigate, debug, and automate any Linux system under pressure. Ace Apple SRE OS interviews.

---

### Week 1 — Filesystem & Directory Structure

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 1 | Linux filesystem hierarchy | Everything is a file · One tree from / · Mounting · Absolute vs relative paths | `pwd` `cd /` `ls` · navigate /etc /var/log /proc · `cat /proc/cpuinfo` · `file /bin/ls` | Explore 6 dirs, note contents · Draw / tree from memory · Which dir is largest? (`du -sh /*`) · **Apple Q:** Walk me through the Linux directory structure |
| 2 | Essential directories deep dive | /etc = config · /var/log = ALL logs · /proc = virtual FS live kernel data · /dev = devices as files | `ls -lh /var/log` · `cat /etc/hostname` · `ls /dev \| head -20` · `echo test > /dev/null` | Find 3 biggest files in /var/log · What is /dev/zero? /dev/random? · Explain /proc in your own words · **Apple Q:** What lives in /etc vs /var vs /proc? |
| 3 | Navigation & file operations | cd pwd ls flags · touch mkdir -p · cp -r mv · rm -rf rmdir | `mkdir -p ~/test/a/b/c` · `touch file{1..5}.txt` · `cp -r /etc/hosts ~/test/` · `ls -la ~/test` | Create folder structure 3 levels deep · Copy move rename 5 files · What does rm -rf / do? Why NEVER run it? |
| 4 | Viewing & searching files | cat less more head tail · tail -f for live watching · grep basic · find by name | `tail -f /var/log/system.log` · `grep 'error' /var/log/system.log` · `find /etc -name '*.conf'` · `head -20 /etc/hosts` | Watch a log file live 2 min · Find all .conf in /etc · Search /var/log for 'fail' · **Apple Q:** Production server throwing errors. First 3 commands? |
| 5 | **CAPSTONE** — SRE first response | Combining navigation + file ops · Real incident: unknown server · Structured approach | `hostname` `uptime` `df -h` · Find 5 largest log files · Check last reboot | **Project:** Document 'first 10 commands on unknown server' as runbook in GitHub · Reproduce from memory · **Apple Q:** You SSH into an unknown production server. First 10 commands and why? |

### Week 2 — File Permissions & Ownership

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 6 | Permission bits — rwx | r=4 w=2 x=1 · Three groups: owner/group/others · ls -l decoded · Why permissions matter | `ls -l /etc/passwd` · `ls -l /usr/bin/ls` · `stat myfile.txt` · `chmod 755 myscript.sh` | Decode: 644 755 777 600 400 · Create file, set 600, try to read as other · What permissions should a bash script have? · **Apple Q:** Explain -rwxr-xr-- bit by bit |
| 7 | chmod, chown, chgrp | chmod symbolic: u+x g-w o=r · chmod octal: 755 · chown user:group · sudo | `chmod u+x myscript.sh` · `chmod 644 config.txt` · `sudo chown root:wheel /etc/hosts` · `find . -perm 777` | Make script executable only by owner · Change ownership recursively · Find all SUID files · **Apple Q:** What does chmod 777 mean and why is it dangerous? |
| 8 | umask, special bits, sudo | umask = default mask · setuid (s) · setgid (s) · sticky bit (t) | `umask` · `umask 022` · `ls -l /usr/bin/passwd` — SUID · `ls -l /tmp` — sticky | Calculate: umask 022 applied to 666 · Why does /usr/bin/passwd have SUID? · What does sticky bit on /tmp prevent? · **Apple Q:** What is setuid and give a real example? |
| 9 | /etc/passwd, /etc/shadow, groups | User database format · Password hashes in shadow · Groups in /etc/group · id whoami groups | `cat /etc/passwd \| head -5` · `id $(whoami)` · `groups` · `sudo cat /etc/shadow \| head -3` | Decode one line of /etc/passwd · Why is /etc/shadow root-only? · What does UID=0 mean? · **Apple Q:** What is /etc/shadow and why does it exist? |
| 10 | **CAPSTONE** — permissions audit script | Combining all permissions knowledge · Audit dangerous perms | `find / -perm -4000 2>/dev/null` · `find /tmp -perm -o+w` · `find /etc -perm -002 2>/dev/null` | **Project:** `permissions-audit.sh` — finds SUID files, world-writable dirs, root-owned files. Commit. · Run and document findings · **Apple Q:** How would you audit a system for dangerous file permissions? |

### Week 3 — Inodes, Links & File Descriptors

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 11 | What is an inode? | Inode = metadata container · Stores perms/owner/size/timestamps/block pointers · Does NOT store filename · Inode number = real file identity | `ls -i` · `stat file.txt` · `df -i` · `find . -inum 12345` | Create file, find inode, delete it. What happened? · Check inode usage with df -i · Why can disk be "full" with space remaining? · **Apple Q:** What is an inode? What does it store and not store? |
| 12 | Hard links vs soft links | Hard link = same inode, another name · Symlink = pointer to path · Hard link survives original deletion · Symlink breaks if original deleted | `ln file.txt hardlink.txt` · `ln -s file.txt softlink.txt` · `ls -li` — same inode · `rm file.txt` — see symlink break | Create both types. Delete original. What happens? · Can you hard-link a directory? Why not? · Find all symlinks in /etc · **Apple Q:** Hard link vs soft link. When use each? |
| 13 | File descriptors — stdin stdout stderr | FD 0=stdin 1=stdout 2=stderr · Redirects: > 2> &> · Pipes connect stdout to stdin | `echo hello > out.txt` · `ls /nonexistent 2> err.txt` · `ls /nonexistent 2>&1 \| grep 'No such'` · `cat < input.txt > output.txt` | Redirect stdout and stderr to different files · Explain 2>&1 step by step · One-liner: run command, save output to file, errors to another · **Apple Q:** Explain file descriptors. What is 2>&1? |
| 14 | lsof — list open files | lsof: every socket/pipe/file = an fd · lsof -p PID · lsof -i for network | `lsof \| head -20` · `lsof -p $$` · `lsof -i :80` · `lsof /var/log/system.log` | Find which process has a log file open · List all network connections · How many files does your shell have open? · **Apple Q:** How do you find which process has a specific file open? |
| 15 | **CAPSTONE** — inode & fd deep dive | Connecting inodes + links + fds · Deleted files consuming space · Recovering disk | `lsof \| grep deleted` · How to reclaim space from deleted-but-open files · `watch -n1 'df -h'` | **Project:** Script that detects deleted files still held open (`lsof \| grep deleted`). Commit. · Full lifecycle of a file: creation to deletion · **Apple Q:** Disk shows 90% full but you've deleted all big files. Why? |

### Week 4 — Text Processing (grep/awk/sed)

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 16 | grep — search and filter | grep pattern file · -i -n -r -v flags · Regex basics: . * ^ $ [] | `grep 'ERROR' /var/log/system.log` · `grep -i 'fail'` · `grep -n 'timeout' server.log` · `grep -v '^#' /etc/hosts` | Extract all ERROR lines · Count 'error' occurrences · Find all lines NOT containing 'INFO' · **Apple Q:** Given a 10GB log file, how do you efficiently find all error lines? |
| 17 | awk — field processing | awk line-by-line, splits into fields · $1 $2 $NF · patterns and actions · NR NF built-ins | `ps aux \| awk '{print $1, $11}'` · `awk -F: '{print $1}' /etc/passwd` · `awk '{sum+=$1} END {print sum}'` · `awk 'NR>5 && NR<10'` | Print username column from /etc/passwd · Sum 5th column of CSV · Print lines where 3rd field > 100 · **Apple Q:** How do you print only the CPU column from ps aux? |
| 18 | sed — stream editing | `sed s/old/new/g` · `sed -i` in-place · `/pattern/d` delete · `-n '5,10p'` print range | `sed 's/ERROR/ALERT/g' server.log` · `sed -i 's/localhost/127.0.0.1/g' config` · `sed '/^#/d' /etc/hosts` · `sed -n '1,5p' bigfile.txt` | Replace hostname in config file · Delete all comment lines · Extract lines 100-200 from large log · **Apple Q:** How do you do in-place find and replace in a config file? |
| 19 | Pipes, sort, uniq, wc | `\|` pipe · sort alphabetical/numerical · `uniq -c` count · `wc -l -w` | `cat log \| sort \| uniq -c \| sort -rn \| head -10` · `ps aux \| sort -k3 -rn \| head -5` · `grep 'ERROR' \| awk '{print $5}' \| sort \| uniq -c \| sort -rn` | Top 10 most frequent log messages · Count unique IPs in access log · Most common HTTP status code · **Apple Q:** Given nginx access log, find top 10 most requested URLs |
| 20 | **CAPSTONE** — log parser toolkit | All grep+awk+sed+pipe combined · Production log analysis | Full pipeline: filter → extract → count → sort · Parse nginx for 5xx · Extract slow queries | **Project:** `log-parser-toolkit.sh` — 5 one-liners analysing real logs. Error counts, top IPs, slow requests. Commit. · **Apple Q:** 5GB nginx log. Find top 5 IPs causing 503 errors in last hour. |

### Week 5 — Processes & Signals

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 21 | Process lifecycle — fork exec wait | fork() clone · exec() replace · wait() parent waits · PID PPID relationships | `ps aux` · `ps -ef --forest` · `pstree` · `echo $$` | Draw process tree of your shell · What is PID 1? What if it dies? · Fork in bash: run command & · **Apple Q:** Walk me through what happens when you type a command in bash and press Enter |
| 22 | Process states — R S D Z T | R=Running · S=Sleeping · D=Uninterruptible(I/O) · Z=Zombie · T=Stopped | `ps aux \| awk '{print $8}' \| sort \| uniq -c` · `ps aux \| grep 'Z'` · `top` · `kill -STOP PID` then `kill -CONT PID` | Create a zombie process deliberately. Explain how. · What causes D state? · How do you clean up zombies? · **Apple Q:** What is a zombie process? How created? How removed? |
| 23 | Signals — SIGTERM SIGKILL SIGHUP | SIGTERM(15) graceful · SIGKILL(9) forced · SIGHUP(1) reload · Cannot catch SIGKILL | `kill -15 PID` · `kill -9 PID` · `kill -HUP $(cat nginx.pid)` · `killall -15 python3` | Kill process with SIGTERM then SIGKILL · Send SIGHUP to running process · What signals can't be caught? · **Apple Q:** Difference between kill -9 and kill -15? When use each? |
| 24 | nice, renice, job control | nice: start with priority (-20 to 19) · renice: change running · & background · fg bg jobs | `nice -n 10 ./heavy.sh` · `renice -n 5 -p PID` · `./script.sh &` · `jobs; fg %1; bg %1` | Start process at low priority · Bring background process to foreground · What does negative nice value mean? Who can set it? |
| 25 | **CAPSTONE** — process watchdog | Monitor process continuously · Auto-restart on crash · Logging events | while loop + ps check · trap for clean shutdown · Logging with timestamps | **Project:** `watchdog.sh` — monitors process by name, restarts if dies, logs all events with timestamps. Test by killing manually. Commit. · **Apple Q:** How would you write a script to monitor and auto-restart a crashed process? |

### Week 6 — Memory, Performance Tools & Networking

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 26 | Memory — virtual physical swap | Virtual: process sees full address space · Physical: actual RAM · Page fault · OOM killer | `free -h` · `cat /proc/meminfo` · `vmstat 1 5` · `top` look at %MEM | What is RSS vs VSZ in ps? · Simulate memory pressure · What does high swap usage mean? · **Apple Q:** Explain virtual memory. What happens when a process accesses unmapped memory? |
| 27 | top, htop, load average | top: live process/system view · Load avg: 1m/5m/15m · Load 1.0 on 1 CPU = 100% · CPU steal time | `top` (press 1 for per-CPU) · `uptime` · `cat /proc/loadavg` · `ps aux --sort=-%cpu \| head -10` | Identify top CPU consumer · Load average 4.0 on 2-core system means? · Explain CPU steal time in VM context · **Apple Q:** Load average 8.0 on 4 CPUs. What does that mean and what do you do? |
| 28 | iostat, vmstat, disk I/O | iostat: disk read/write/sec · vmstat: memory+I/O+CPU · %iowait: CPU waiting for disk | `iostat -x 1 5` · `vmstat 1 10` · `iostat -d -x 1` · `df -h` | What does high %iowait indicate? · Which process is causing most disk I/O? · Difference between throughput and IOPS? · **Apple Q:** Server is slow. top shows low CPU. What do you check next? |
| 29 | Networking — ss, netstat, lsof -i | TCP states: ESTABLISHED LISTEN TIME_WAIT · ss replaces netstat · lsof -i for connections · Ports: well-known <1024 | `ss -tlnp` · `lsof -i :8080` · `netstat -an \| grep ESTABLISHED \| wc -l` · `ss -s` | Find which process listening on port 80 · Count active TCP connections · What is TIME_WAIT and is it a problem? · **Apple Q:** How do you find which process is using port 443 on production? |
| 30 | **CAPSTONE** — system health report | Combining all performance tools · Color-coded output | CPU + memory + disk + load in one script · ANSI color codes · Exit code based on thresholds | **Project:** `health-report.sh` — checks CPU% memory% disk% load avg, top 3 CPU procs. Color output green/yellow/red. Commit. · **Apple Q:** Walk me through diagnosing a slow production server from scratch |

### Week 7 — Bash Scripting Core

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 31 | Variables, arrays, arithmetic | `VAR=value` no spaces · `$VAR` or `${VAR}` · Arrays: `arr=(a b c)` · `$((2+2))` | `NAME='Siddharth'; echo $NAME` · `arr=(web-01 web-02 db-01)` · `echo ${arr[@]}` · `echo $((100 / 4))` | Store 5 server names in array. Loop and print. · Calculate total disk usage from df · Difference between single and double quotes? · **Apple Q:** Difference between $VAR and ${VAR}? |
| 32 | Conditionals and test expressions | `if [ condition ]; then` · Numeric: -eq -ne -gt -lt · String: == != -z -n · File: -f -d -x -e | `if [ -f /etc/hosts ]; then echo 'exists'; fi` · `if [ $cpu -gt 80 ]; then echo 'HIGH'; fi` · `[ -x /usr/bin/python3 ] && echo 'ok'` · `[[ $str == *error* ]]` | CPU > 80 → WARNING, > 90 → CRITICAL · Check file exists AND is readable · Test if string contains substring · **Apple Q:** Difference between `[ ]` and `[[ ]]`? |
| 33 | Loops — for, while, until | `for item in list; do` · `for ((i=0; i<10; i++))` · `while [ condition ]; do` · break continue | `for server in web-01 web-02; do echo $server; done` · `for f in *.log; do wc -l $f; done` · `while true; do sleep 5; check; done` · `for i in {1..10}` | Loop all .log files, print line count · Infinite loop checking service every 10s · Use break when condition is met · **Apple Q:** How do you iterate over files in a directory? |
| 34 | Functions, exit codes, trap | `function name() { }` · `$?` last exit code · 0=success non-zero=failure · `trap 'cleanup' EXIT INT TERM` | `function check_disk() { df -h $1; }` · `grep pattern file; echo $?` · `trap 'rm -f /tmp/lockfile' EXIT` | Function returns 0 if service up, 1 if not · trap to clean up temp files on exit · Chain commands with && and || · **Apple Q:** What is an exit code? What does 1 vs 127 mean? |
| 35 | **CAPSTONE** — bash functions library | Reusable bash functions · source / . · Strict mode | `source ./lib/logging.sh` · `set -euo pipefail` · Logging library with log_info log_warn log_error | **Project:** `bash-lib/` — `logging.sh` (log_info/warn/error with timestamps), `utils.sh` (check_command, is_root, get_cpu_percent). Source in health-report.sh. Commit. · **Apple Q:** What does `set -euo pipefail` do and why start every script with it? |

### Week 8 — Bash Advanced + Phase 1 Capstone

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 36 | Advanced text processing | sed multi-line · awk BEGIN/END blocks · cut columns · tr translate | `awk 'BEGIN{print "Start"} /error/{count++} END{print count}'` · `sed -n '/START/,/END/p'` · `cut -d: -f1,3 /etc/passwd` · `tr '[:lower:]' '[:upper:]'` | Count errors per hour from timestamped log · Extract specific CSV columns · Convert log dates from US to ISO format · **Apple Q:** Extract all unique HTTP status codes from nginx log |
| 37 | xargs, parallel execution, find advanced | `xargs` build commands from stdin · `find -exec` · `&` background + `wait` | `find . -name '*.log' \| xargs wc -l` · `find /tmp -mtime +7 -exec rm {} \;` · `for f in *.sh; do bash $f & done; wait` | Delete all .tmp files older than 7 days · Run 5 health checks in parallel and wait · What is the danger of xargs with rm? · **Apple Q:** Find and delete all files > 100MB older than 30 days |
| 38 | cron, systemd basics, journalctl | cron schedule format: min hr dom mon dow · `crontab -e` · systemd init · journalctl | `crontab -e` · `0 */6 * * * /opt/scripts/backup.sh` · `journalctl -u nginx -n 50` · `journalctl --since '1 hour ago'` | Schedule health-report.sh every 5 minutes · Check status of a systemd service · Find all cron jobs on the system · **Apple Q:** Write a crontab entry to run a script every day at 3am |
| 39 | Script debugging, getopts, here-docs | `bash -x` trace · `bash -n` syntax check · getopts parse flags · `<<EOF` here-doc | `bash -x myscript.sh 2>&1 \| head -30` · `while getopts 'hvf:' opt; do case...` · `cat <<EOF multi line EOF` | Debug a broken script with bash -x · Add -v verbose and -h help flags to health-report.sh · Use here-doc to write a config file · **Apple Q:** How do you debug a bash script that isn't working? |
| 40 | **MEGA CAPSTONE** — SRE Bash Toolkit | All 8 weeks combined · 5 production-grade scripts · GitHub portfolio | All 5 scripts working together · README with usage · Demo run with sample output | **Project:** Complete SRE Bash Toolkit — (1) health-report.sh (2) watchdog.sh (3) log-parser-toolkit.sh (4) disk-cleanup.sh (5) network-checker.sh. All use bash-lib/. Full README. Committed and pushed. · Record yourself running all 5. · Write Phase 1 reflection in README.md |

---

# PHASE 2 — Git & GitHub
**Month 3 · Weeks 9–10 · 10 days**
**Goal:** Use Git like a professional engineer. Every future project is version controlled.

### Week 9 — Git Fundamentals

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 41 | Git mental model — snapshots | Snapshots not diffs · Working tree → staging → repo · SHA hash · .git/ directory | `git init` `git status` · `git add file.txt` `git add .` · `git commit -m 'message'` · `git log --oneline --graph` | Init repo. Make 3 commits. View log. · What is in .git/ directory? · Delete a file. Use git to restore it. · **Apple Q:** Explain the 3 areas in Git |
| 42 | Branches — the killer feature | Branch = lightweight pointer · HEAD = current position · checkout vs switch · Branches are free | `git branch feature-x` · `git switch feature-x` · `git switch -c new-branch` · `git branch -a` | Create branch, 2 commits, switch back to main · Draw branch diagram in notebook · Why are branches "cheap" in Git? · **Apple Q:** What is a Git branch and how does it work under the hood? |
| 43 | Merging and resolving conflicts | Fast-forward merge · 3-way merge commit · Conflict markers: `<<<< ==== >>>>` · `git merge --abort` | `git merge feature-x` · Create deliberate conflict · Resolve in editor · `git merge --abort` | Deliberately create and resolve a conflict · What is a fast-forward merge? · When should you NOT use git merge? · **Apple Q:** Walk me through resolving a merge conflict |
| 44 | git diff, reset, revert, stash | diff: what changed · reset soft/mixed/hard · revert: safe undo (new commit) · stash: shelve work | `git diff HEAD~1` · `git reset --soft HEAD~1` · `git stash; git stash pop` · `git revert abc123` | Undo last commit but keep changes · Stash, switch branches, come back · Difference between reset and revert? · **Apple Q:** Difference between git reset and git revert? |
| 45 | **CAPSTONE** — Git workflow drill | Full professional workflow · Feature branch flow · Conventional Commits | `feat:` `fix:` `docs:` format · Full feature branch → merge cycle | **Project:** Reorganise sre-learning-journal with proper structure. 10 well-named Conventional Commits. Push to GitHub. · Review commit history · Write git-workflow.md · **Apple Q:** What makes a good commit message? |

### Week 10 — GitHub & Team Workflow

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 46 | GitHub — remotes, push, pull, fetch | origin = default remote · `git push` · fetch vs pull (fetch+merge) · SSH keys | `git remote -v` · `git push origin feature-branch` · `git fetch --all` · `git pull --rebase origin main` | Push branch to GitHub without merging · Set up SSH key auth · Difference between fetch and pull? · **Apple Q:** git fetch vs git pull. When use each? |
| 47 | Pull requests & code review | PR = request to merge · Code review: comment, request changes · Branch protection · PR description | Create PR on GitHub · Add reviewers + description · Respond to review comments · Merge strategies: merge commit, squash, rebase | Open a real PR in your repo · Write a PR description template · Difference between squash and merge? · **Apple Q:** What is a pull request and why do teams use them? |
| 48 | git rebase, cherry-pick, reflog | rebase: replay on new base · interactive: squash reword drop · cherry-pick: copy a commit · reflog: the safety net | `git rebase main` · `git rebase -i HEAD~3` · `git cherry-pick abc123` · `git reflog` | Squash 3 commits into 1 · Cherry-pick a specific bug fix · Recover deleted branch with reflog · **Apple Q:** What is git rebase and when use instead of merge? |
| 49 | GitHub Actions — CI/CD basics | Actions: automate on git events · Workflow YAML: on, jobs, steps · Run tests on push/PR · Actions marketplace | `.github/workflows/test.yml` · `on: push: branches: [main]` · `jobs: test: runs-on: ubuntu-latest` · `steps: checkout, run tests` | Create workflow that runs on every push · Add shellcheck step for bash scripts · What is a GitHub Actions runner? · **Apple Q:** What is CI/CD and how does GitHub Actions implement it? |
| 50 | **CAPSTONE** — GitHub portfolio polish | Repo IS your resume · README structure · Tags and releases · .gitignore | README with badges · `git tag v1.0.0` · .gitignore for Python, Node, bash · GitHub profile README | **Project:** Polish sre-learning-journal: proper README, .gitignore, tag v1.0.0 of bash toolkit, create GitHub profile README. Push everything. · **Apple Q:** An interviewer asks to see your GitHub. What should they find? |

---

# PHASE 3 — Python Core & Intermediate
**Months 3–4 · Weeks 11–18 · 40 days**
**Goal:** Write real Python programs from scratch. Build tools you'd actually use as an SRE.

### Week 11 — Python Basics

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 51 | Variables, types, print, f-strings | Dynamically typed · int float str bool · f-string: `f'Hello {name}'` · `type()` | `name = 'Siddharth'; age = 40` · `print(f'I am {age}')` · `print(type(3.14))` | All 4 types + print with type · Personal info printout with f-strings · What happens when you add int + str? |
| 52 | Arithmetic, comparison, boolean | + - * / // % ** · == != > < >= <= · and or not · Short-circuit | `print(10 // 3)` · `print(10 % 3)` · `print(2 ** 8)` | FizzBuzz for 1-20 · CPU alert: > 90 CRITICAL, > 70 WARNING, else OK · What does `not not True` evaluate to? |
| 53 | if/elif/else, while loops | Indentation defines blocks · elif: first match wins · while: condition True · break continue | Grade logic with if/elif/else · Countdown with while · `while True` with break | Number guessing game with while · Rewrite bash CPU alert in Python · What is an infinite loop? |
| 54 | for loops, range, lists intro | `for item in collection` · `range(start, stop, step)` · Lists: ordered mutable · append pop len sorted | `for i in range(1, 11): print(i*7)` · `servers = ['web-01','web-02']` · `servers.append('cache-01')` | Multiplication table for 7 · Sum 1-100 without sum() · Loop server list and print 'Checking {server}' |
| 55 | **CAPSTONE** — CPU monitor | All Week 11 concepts · def return | `def get_status(cpu)` · `def summarize(readings)` · `readings = [55,82,93,67]` | **Project:** `cpu-monitor.py` — 6 readings, get_status() function, summarize() prints each with status, average + CRITICAL count. Commit. |

### Week 12 — Strings, Lists & Tuples

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 56 | String methods mastery | `.upper() .lower() .strip()` · `.split()` · `' '.join(list)` · `.replace() .startswith() .find()` | `log.split()` · `parts = log.split(' ', 2)` · `'ERROR' in log` | Parse log line into date/time/level/message · Extract all words from sentence · Count 'error' case-insensitively |
| 57 | List operations & slicing | `list[start:stop:step]` · `list[-1]` · `.insert() .remove() .pop()` · `list * 3` | `servers[1:3]` · `servers[::-1]` · `servers.pop(0)` | Reverse list without .reverse() · Rotate list left by 2 · Find second largest number |
| 58 | enumerate, zip, comprehensions | `enumerate`: (index, value) · `zip`: combine two lists · `[expr for item in list]` · filtered comprehension | `for i, srv in enumerate(servers)` · `for srv, status in zip(servers, statuses)` · `errors = [l for l in logs if 'ERROR' in l]` | Rewrite for loop as comprehension · Zip two lists into dict · Find all ERROR lines in one comprehension |
| 59 | Tuples and immutability | Tuple: immutable list · `(x, y)` unpacking · Tuples as dict keys · When tuple vs list | `point = (40.7128, -74.0060)` · `lat, lon = point` · `config = ('localhost', 5432, 'mydb')` | Unpack server config tuple to named vars · Why can't you use a list as dict key? · Store 5 server configs as tuples in a list |
| 60 | **CAPSTONE** — log line parser | All string + list tools · Real SRE utility | Parse nginx combined log · Extract IP/method/URL/status/bytes · Aggregate by status code | **Project:** `log-line-parser.py` — parse 20 sample nginx log lines, count by status, find top 3 IPs. Commit. |

### Week 13 — Dictionaries, Sets & JSON

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 61 | Dictionaries — CRUD | `dict = {key: value}` · `dict[key]` `.get(key, default)` · `.keys() .values() .items()` | `server = {'host':'web-01','cpu':85}` · `server.get('disk', 'unknown')` · `for k, v in server.items()` | Model server config as dict · Get value safely with .get() · Merge two dicts (3 ways) |
| 62 | Dict comprehensions, nested dicts | `{ k: v for k, v in ... if cond }` · Nested: `servers['web-01']['cpu']` · Counting with dicts | `{s: 'ok' for s in servers}` · `fleet = {'web-01': {'cpu':85}}` · `freq[word] = freq.get(word,0)+1` | Count word frequency in paragraph · Build nested dict of 5 servers · Sort servers by CPU descending |
| 63 | Sets and membership testing | Unordered unique · `\| & - ^` operations · O(1) membership: `x in my_set` · frozenset immutable | `errors = {'disk_full','timeout','oom'}` · `errors & critical` · `'timeout' in errors` | Servers in alert list but NOT in maintenance · Remove duplicates with set · Union two sets of IPs |
| 64 | JSON — read, write, parse | `json.loads()` string→dict · `json.dumps()` dict→string · `json.load(f) / json.dump(d, f)` · `indent=2` | `config = json.loads(json_string)` · `print(json.dumps(config, indent=2))` · `with open('config.json') as f: d = json.load(f)` | Read JSON config and extract nested value · Convert dict to pretty JSON and save · Parse mock API response JSON |
| 65 | **CAPSTONE** — config manager | All M3 Python concepts · JSON config management | Read servers.json · Validate required keys · Update value and write back | **Project:** `config-manager.py` — reads servers.json, validates fields, prints summary, updates + saves. With sample servers.json. Commit. |

### Week 14 — File I/O, Error Handling & Regex

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 66 | File I/O — read write append | `open(path, mode)` modes: r w a rb · with statement auto-closes · `readlines()` vs `read()` vs iteration | `with open('log.txt') as f: for line in f:` · `with open('out.txt', 'w') as f: f.write(...)` | Read log, count ERROR lines, write summary · Append timestamped entry to log · Difference between r and rb modes? |
| 67 | try/except/finally/raise | try risky code · except SpecificError as e · finally always runs · raise ValueError('msg') | `try: int('abc') except ValueError as e: print(e)` · `try: open('x') except FileNotFoundError:` · `raise ValueError('CPU must be 0-100')` | Wrap file open, handle FileNotFoundError AND PermissionError differently · Function raises ValueError for invalid input · What happens if you don't catch an exception? |
| 68 | Custom exceptions, logging module | `class MyError(Exception): pass` · logging: INFO WARNING ERROR CRITICAL · `basicConfig(level=logging.INFO)` · FileHandler | `class DiskFullError(Exception): pass` · `logging.warning('disk 90%')` · `logging.basicConfig(filename='app.log')` | Create ServerUnreachableError exception · Replace all print() in cpu-monitor with logging · Configure logging to file AND console |
| 69 | Regex — re module | `re.search() .match() .findall()` · Groups: `(pattern)` · `\d+ \w+ .* \s` | `re.search(r'ERROR: (.+)', log_line)` · `re.findall(r'\d{1,3}\.\d{1,3}...\d{1,3}', text)` · `re.sub(r'password=\S+', 'password=***', line)` | Extract all IPs from log file · Parse timestamp from log line · Redact all password= values |
| 70 | **CAPSTONE** — Python log analyzer | All M3 Python combined · CLI tool | `argparse: --file --level --top-n` · Parse real /var/log · Output counts + top errors | **Project:** `log-analyzer.py` — CLI (argparse), reads log file, filters by --level, shows top --top-n errors, outputs summary. README with usage. Commit. |

### Week 15 — Functions Advanced & Comprehensions

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 71 | *args, **kwargs, defaults | `def f(*args)` variable positional · `def f(**kwargs)` variable keyword · `def f(x, default=10)` | `def log(*msgs): for m in msgs: print(m)` · `def connect(host, port=5432, timeout=30):` | Function accepts any number of server names · Flexible HTTP request function with **kwargs · What happens with f(1,2, x=3, y=4)? |
| 72 | Lambda, map, filter, sorted key | `lambda x: x*2` anonymous · `map(func, iterable)` · `filter(func, iterable)` · `sorted(list, key=lambda x: x['cpu'])` | `list(map(lambda x: x**2, [1,2,3]))` · `list(filter(lambda x: x > 80, cpus))` · `sorted(servers, key=lambda s: s['cpu'], reverse=True)` | Sort list of dicts by nested value · Filter servers CPU > 80 in one line · Map log lines to severity levels |
| 73 | Dict/set comprehensions, generators | `{ k:v for k,v in items if cond }` · `{x for x in list}` · `(x for x in list)` lazy generator | `{s['name']: s['cpu'] for s in servers}` · `gen = (line for line in open('big.log'))` · `sum(1 for line in open('log') if 'ERROR' in line)` | Count ERROR lines in huge log using generator (memory efficient) · Build {server: status} dict in one line · Difference between list comprehension and generator? |
| 74 | Closures, decorators intro | Closure: function remembers its scope · `def outer(): def inner():` · `@func` wraps another function · `@functools.wraps` | `def make_multiplier(n): return lambda x: x*n` · `def timer(func): ... return wrapper` · `@timer def slow_function():` | Write closure that makes a counter · @timer decorator printing execution time · @retry(n) decorator that retries on exception |
| 75 | **CAPSTONE** — functional toolkit | Functional patterns for SRE · Composable utilities | `@retry(3)` `@log_call` `@timer` | **Project:** `decorators.py` — @timer, @retry(n), @log_call. Apply to health check functions. Commit. |

### Week 16 — OOP Basics

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 76 | Classes, __init__, self, methods | `class ClassName:` · `__init__(self, ...)` constructor · self = reference to instance | `class Server: def __init__(self, name, ip):` · `server = Server('web-01', '10.0.0.1')` · `def status(self): return 'ok' if self.cpu < 80 else 'warn'` | Server class with name/ip/cpu/memory + status() · Create 3 Server objects in a list · Class vs instance? |
| 77 | Inheritance, __str__, @property | `class Child(Parent):` · `super().__init__()` · `__str__` print representation · `@property` getter | `class WebServer(Server):` · `def __str__(self): return f'Server({self.name})'` · `@property def is_healthy(self):` | WebServer and DatabaseServer inheriting from Server · Override __str__ to print nicely · @property returning load category |
| 78 | Dataclasses, class methods, static | `@dataclass` auto init repr eq · `@classmethod` cls arg · `@staticmethod` no self/cls · When use each | `@dataclass class Server: name: str; cpu: float = 0.0` · `@classmethod def from_dict(cls, d):` · `@staticmethod def validate_ip(ip):` | Rewrite Server as @dataclass · Add from_json() classmethod · Add validate_hostname() staticmethod |
| 79 | Exception classes, context managers | Custom exception hierarchy · `__enter__ __exit__` · with works with context managers | `class SREError(Exception): pass` · `class ServerUnreachable(SREError): pass` · Context manager timing a block | Build SRE exception hierarchy (3 levels) · Context manager that times a block · Context manager creating/cleaning temp directory |
| 80 | **CAPSTONE** — server fleet model | Full OOP model of SRE fleet · JSON serialization | Fleet class with Server objects · `fleet.add_server() .get_critical()` · `fleet.to_json() Fleet.from_json()` | **Project:** `fleet-model.py` — Server @dataclass, Fleet class with add/remove/status/report, load/save from JSON. Commit with sample fleet.json. |

### Week 17 — Modules, Stdlib & Virtual Envs

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 81 | Modules, packages, import | `import module` `from module import x` · `__name__ == '__main__'` guard · Package = dir with __init__.py | `import os, sys, pathlib` · `if __name__ == '__main__': main()` | Create package 'sretools' with health.py and logging.py · Import your own module · What does __name__ guard prevent? |
| 82 | os, sys, pathlib — filesystem | os.path vs `pathlib.Path` · `Path('/var/log') / 'nginx'` · `os.walk()` · `sys.argv` | `p = Path('/var/log'); list(p.glob('*.log'))` · `for root, dirs, files in os.walk('/etc'):` · `print(sys.argv)` | List all .log files under /var/log recursively · Get size of all Python files in dir · Use sys.argv to accept a directory path |
| 83 | datetime, collections, itertools | `datetime.now()` timedelta · `Counter` · `defaultdict` · `itertools.chain groupby islice` | `Counter(['a','b','a','c'])` · `defaultdict(list)` · `list(itertools.islice(range(1000), 10))` | Parse log timestamps and find busiest minute · Count error types using Counter · Group log entries by hour with defaultdict |
| 84 | venv, pip, requirements.txt | venv: isolated environment · `python -m venv .venv` · pip install · `pip freeze > requirements.txt` | `python3 -m venv .venv` · `source .venv/bin/activate` · `pip install requests pytest` | Create venv. Install requests and pytest. Freeze requirements. · Why always use a venv? · Difference between `pip install` and `pip install -r`? |
| 85 | **CAPSTONE** — sretools package | Building proper Python package · Reusable SRE utility library | `sretools/__init__.py` · `sretools/health.py sretools/logs.py` · `from sretools.health import check_cpu` | **Project:** Create `sretools/` package — health.py (check_cpu/disk/memory), logs.py (parse_log_line, count_by_level). requirements.txt + README. Commit. |

### Week 18 — HTTP, APIs & Testing

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 86 | requests — HTTP in Python | `requests.get(url)` `.post(url, json=data)` · `response.status_code .json() .text` · Timeout + error handling | `r = requests.get('https://httpbin.org/get')` · `print(r.status_code, r.json())` · `r = requests.get(url, timeout=5)` | Check if list of URLs are reachable · POST JSON data and print response · Handle timeout and connection errors |
| 87 | REST API patterns, JSON handling | REST: GET POST PUT DELETE · Status codes: 200 201 400 401 403 404 500 · Pagination · Auth: Bearer token | `headers = {'Authorization': f'Bearer {token}'}` · `r.raise_for_status()` · Pagination loop | Function that handles pagination automatically · Reusable API client class · What does r.raise_for_status() do? |
| 88 | argparse — professional CLI tools | `add_argument` positional vs --optional · type= required= default= help= · Subcommands | `parser.add_argument('--file', required=True)` · `parser.add_argument('--level', default='ERROR')` · `args = parser.parse_args()` | Add argparse to log-analyzer.py with --file --level --top-n --output · Add --json flag · Add --version argument |
| 89 | pytest — testing your code | Run test_*.py files · `assert x == y` · `@pytest.fixture` · `@pytest.mark.parametrize` | `def test_get_status(): assert get_status(95) == 'CRITICAL'` · `@pytest.mark.parametrize('cpu,expected', [(95,'CRITICAL')])` · `pytest -v` | Write 5 tests for get_status() · Test that reads a sample log file · Run pytest and get all green |
| 90 | **CAPSTONE** — API health checker | All Python concepts combined · Production-grade CLI + tests + CI | `health-checker --config servers.json --output report.json` · Concurrent checks · GitHub Actions CI | **Project:** `api-health-checker.py` — reads JSON config of endpoints, checks each with timeout, outputs JSON/text report, --alert-threshold flag. Full pytest suite. GitHub Actions CI. Tag v1.0.0. |

---

# PHASE 4 — Data Structures & Algorithms
**Month 5 · Weeks 19–22 · 20 days**
**Goal:** Pass coding screens. Think in Big O. Write efficient solutions.

### Week 19 — Big O & Arrays & Linked Lists

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 91 | Big O notation | O(1) O(log n) O(n) O(n log n) O(n²) · Space complexity · Drop constants: O(2n)=O(n) | O(1): dict lookup · O(n): linear search · O(n²): nested loop | Classify 5 code snippets by Big O · Is O(n + m) same as O(n)? · Big O of .append() on Python list? · **Apple Q:** What is Big O? Compare O(n) vs O(n²) with example |
| 92 | Arrays — two pointer technique | Two pointers: left + right converge · O(n) instead of O(n²) · Sliding window variant | Find pair summing to target · Palindrome check · Remove duplicates in-place | Two Sum (sorted) · Valid Palindrome (#125) · Remove Duplicates from Sorted Array (#26) |
| 93 | Linked lists from scratch | Node: value + next pointer · Singly vs doubly · O(1) insert at head O(n) access | `class Node: def __init__(self, val, next=None):` · `class LinkedList: insert delete traverse` | Build LinkedList class with insert/delete/print · Reverse a linked list iteratively · Detect cycle in linked list |
| 94 | Two pointer & sliding window problems | Sliding window: expand/contract · Fast + slow pointer: cycle detection · In-place: O(1) space | Longest substring without repeating · Max sum subarray of size k · Floyd's cycle detection | Best Time to Buy and Sell Stock (#121) · Maximum Average Subarray (#643) · Linked List Cycle (#141) |
| 95 | **CAPSTONE** — array & linked list sprint | Pattern recognition · Clean solution code | Problem → brute force → optimize · Walk through time/space complexity · Edge cases | **Project:** Solve LeetCode #1, #121, #125. Commit each with Big O analysis in comments. Explain solutions out loud. |

### Week 20 — Stacks, Queues & Hash Maps

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 96 | Stacks — LIFO | Stack: push (top) pop (top) · Python list as stack · Applications: undo, call stack, balanced parens | `stack = []; stack.append(1); stack.pop()` · Valid parentheses | Valid Parentheses (#20) · Min Stack (#155) · Daily Temperatures (#739) |
| 97 | Queues & deque | Queue: enqueue(back) dequeue(front) · `collections.deque` O(1) both ends · BFS uses queues · heapq | `from collections import deque` · `q.append(1); q.popleft()` · BFS level traversal | Implement queue using two stacks · Number of Recent Calls (#933) · First Unique Character (#387) |
| 98 | Hash maps — internals & patterns | Hash function → index · Collision: chaining or open addressing · O(1) avg · Counting pattern | `freq[word] = freq.get(word,0)+1` · `Counter` · Two Sum hash map O(n) | Two Sum (#1) hash map version · Group Anagrams (#49) · Top K Frequent Elements (#347) |
| 99 | String problems with hash maps | Anagram detection · Substring problems · Character frequency · Sliding window + hash map | `Counter` comparison · Find all anagrams · First non-repeating character | Valid Anagram (#242) · Contains Duplicate (#217) · Longest Consecutive Sequence (#128) |
| 100 | **CAPSTONE** — hash map sprint | Hash map as go-to structure · Pattern recognition | seen set · count map · index map | **Project:** Solve #347, #49, #217. Commit with full explanations and Big O. |

### Week 21 — Recursion, Sorting & Searching

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 101 | Recursion — thinking recursively | Base case: when to stop · Recursive case: smaller subproblem · Stack overflow risk · Memoization | `def factorial(n): if n<=1: return 1; return n*factorial(n-1)` · Fibonacci memoized | Recursive: sum of list, reverse string, power(base,exp) · Fibonacci with @lru_cache · What causes stack overflow in recursion? |
| 102 | Binary search | Requires sorted input · Divide + check middle: O(log n) · `while l <= r` template | `def binary_search(arr, target):` · Search Insert Position · Find First and Last Position | Binary Search (#704) · Search Insert Position (#35) · Find Minimum in Rotated Sorted Array (#153) |
| 103 | Sorting algorithms | Bubble: O(n²) · Merge sort: O(n log n) divide and conquer · Quick sort: O(n log n) avg · Timsort in Python | Implement merge sort from scratch · `sorted()` and `list.sort()` · `sorted(servers, key=lambda s: s['cpu'])` | Implement merge sort · Sort Colors (#75) · Sort list of dicts by multiple keys |
| 104 | Trees — binary trees & BST | TreeNode: value left right · BST: left<root<right · DFS: inorder preorder postorder · Height depth balance | `class TreeNode: def __init__(self, val):` · `def inorder(root):` · BST search O(log n) | Max Depth of Binary Tree (#104) · Invert Binary Tree (#226) · Validate BST (#98) |
| 105 | **CAPSTONE** — recursion & sorting sprint | Recursive thinking · Sort-then-search pattern | Solve, optimize, explain Big O | **Project:** Solve #104, Climbing Stairs (#70) with memoization, Merge Intervals (#56). Commit with explanations. |

### Week 22 — Graphs & Problem Solving Framework

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 106 | Graphs — representation & BFS | Adjacency list: dict of lists · BFS: level-by-level, uses queue · BFS for shortest path | `graph = {'A': ['B','C'], 'B': ['D']}` · BFS template with visited set | Number of Islands (#200) · Flood Fill (#733) · BFS shortest path in maze |
| 107 | DFS on graphs and trees | DFS: go deep first, stack/recursion · Cycle detection · Connected components · Backtracking | DFS recursive and iterative · Course Schedule: cycle detection | Course Schedule (#207) · Clone Graph (#133) · Number of Connected Components (#323) |
| 108 | Dynamic programming intro | DP = recursion + memoization OR bottom-up table · Overlapping subproblems · 1D DP: Fibonacci, Climbing Stairs | `dp[i] = dp[i-1] + dp[i-2]` · House Robber · Unique Paths | House Robber (#198) · Unique Paths (#62) · Coin Change (#322) |
| 109 | Problem solving framework | 5 steps: understand, examples, approach, code, review · Pattern recognition from constraints · Interview communication | n ≤ 10⁴ → O(n²) ok · 'shortest path' → BFS · 'all combinations' → backtracking | Classify 10 problems by pattern before solving · Time yourself: 20 min per LeetCode Easy · Record voice explanation of solution |
| 110 | **CAPSTONE** — LeetCode sprint | 10 Easy problems solved + explained · Clean code with Big O | One problem per 20-30 min · Document patterns | **Project:** Solve 10 LeetCode Easy total (#1 #20 #21 #70 #104 #121 #125 #141 #226 #242). Each committed with Big O and pattern name. Write dsa-patterns.md cheat sheet. |

---

# PHASE 5 — SRE Python Automation
**Month 6 · Weeks 23–26 · 20 days**
**Goal:** Build real SRE tools that work in production. Linux + Python finally combine.

### Week 23 — subprocess, OS Automation & CLI Tools

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 111 | subprocess — run shell from Python | `subprocess.run()` wait · `Popen()` non-blocking · `capture_output=True` · `check=True` raise on error | `result = subprocess.run(['df','-h'], capture_output=True, text=True)` · `print(result.stdout)` | Run df -h from Python, parse output · Run ps aux, find top 3 CPU processes · What is the security risk of `shell=True`? |
| 112 | os, pathlib for system tasks | `os.walk()` recursive · `pathlib.Path` modern · `os.environ` · `os.getpid() os.getuid()` | `for root, dirs, files in os.walk('/var/log'):` · `Path('/var/log').glob('**/*.log')` · `os.environ.get('HOME', '/tmp')` | Find all files over 100MB in /var recursively · Read config from env var with fallback · Disk usage of each subdir in /var/log |
| 113 | logging module — production logging | Levels: DEBUG INFO WARNING ERROR CRITICAL · Formatters · Handlers: console + file · RotatingFileHandler | `logging.basicConfig(level=logging.INFO, format='%(asctime)s %(levelname)s %(message)s')` · `RotatingFileHandler('app.log', maxBytes=10_000_000, backupCount=5)` | Log to both console and rotating file · Filter: WARNING+ to file, all to console · Difference between logger.error() and logging.error()? |
| 114 | Building professional CLI tools | argparse subcommands · click (alternative) · Config file + CLI precedence · Exit codes: 0=ok 1=error 2=usage | `subparsers = parser.add_subparsers(dest='command')` · `sys.exit(1)` on error · `print('error', file=sys.stderr)` | Add --config flag to load JSON config · Add subcommands: health check report alert · Package CLI with proper help text |
| 115 | **CAPSTONE** — disk space monitor | subprocess + pathlib + logging + argparse combined | Check all mount points · Alert if > threshold · Write to log file | **Project:** `disk-monitor.py` — checks all mount points, alerts if > threshold (default 80%), logs to rotating file, --threshold --logfile --json flags. README. Commit. |

### Week 24 — Prometheus Metrics & REST APIs

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 116 | Prometheus concepts & client | Prometheus scrapes /metrics · Types: Counter Gauge Histogram Summary · Labels add dimensions | `from prometheus_client import Counter, Gauge, start_http_server` · `cpu_usage = Gauge('cpu_usage_percent', 'CPU usage')` | Start Prometheus HTTP server on port 8000 · Create Gauge for CPU + Counter for disk checks · Visit localhost:8000/metrics |
| 117 | Custom Prometheus exporter | Exporter: collect metrics + expose /metrics · Collect loop · Labels for multi-dimensional data · Histogram for latency | `class SREExporter: def collect(self):` · `REGISTRY.register(SREExporter())` · `request_latency = Histogram('latency', 'Latency', buckets=[0.1,0.5,1,5])` | Build exporter exposing CPU/memory/disk as Gauges · Add per-service CPU tracking with labels · Write 3 PromQL alert expressions |
| 118 | Calling REST APIs — SRE use cases | Query Prometheus HTTP API · Call Kubernetes API · Retry with exponential backoff | `requests.get('http://prometheus:9090/api/v1/query?query=up')` · Exponential backoff: `time.sleep(2**attempt)` · `r.raise_for_status()` in retry loop | Query Prometheus API, find metrics above threshold · Implement `retry_request(url, retries=3)` with backoff · Parse a Kubernetes-style API response |
| 119 | Async HTTP with asyncio | asyncio: single-threaded concurrency · `async def + await` · aiohttp · `asyncio.gather()` concurrent | `async def check_url(session, url):` · `asyncio.run(main())` · `await asyncio.gather(*tasks)` | Check 10 URLs concurrently with aiohttp · Compare sequential vs async timing · Why is async better than threading for I/O? |
| 120 | **CAPSTONE** — Prometheus exporter | Full custom exporter for SRE metrics | CPU memory disk process count Gauges · HTTP /metrics endpoint · Collect every 15 seconds | **Project:** `sre-exporter.py` — 8 SRE metrics via /metrics. README with example Prometheus config. Commit. Run and verify with curl. |

### Week 25 — Concurrency & Async Python

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 121 | Threading — I/O bound tasks | Threading: concurrent · GIL: no CPU parallelism · Good for: I/O network file · ThreadPoolExecutor | `with ThreadPoolExecutor(max_workers=10) as ex: futures = [ex.submit(check, srv) for srv in servers]` | Check 20 URLs concurrently with ThreadPoolExecutor · Compare 20 sequential vs concurrent — measure time · What happens if a thread raises an exception? |
| 122 | Multiprocessing — CPU bound | `ProcessPoolExecutor` real parallelism · Good for: CPU computation, data processing · `Queue Pipe` | `with ProcessPoolExecutor(max_workers=4) as ex:` · `multiprocessing.cpu_count()` | Process 1000 log files in parallel · When to use processes vs threads vs asyncio? · What is the GIL? |
| 123 | asyncio deep dive | Event loop: non-blocking I/O · `async def` coroutine · `await` yields control · `asyncio.Queue` producer-consumer | `async def producer(): await queue.put(item)` · `asyncio.create_task()` · `async with async for` | Build async producer-consumer with asyncio.Queue · Rate-limit async requests to 5/sec · What is a coroutine vs a function? |
| 124 | Concurrency patterns for SRE | Health check: concurrent + timeout · Circuit breaker · Worker pool · Rate limiting | `asyncio.wait_for(check(), timeout=5)` · Circuit breaker: count failures open after N · Semaphore to limit concurrency | Implement check_with_timeout(url, timeout=5) · Simple circuit breaker class · Rate-limited API caller (max 10 req/sec) |
| 125 | **CAPSTONE** — parallel health checker | Concurrent health checking of N services | Check 50 endpoints in parallel · Timeout each at 3s · Aggregate + alert | **Project:** `parallel-health-checker.py` — async check of N endpoints, timeout per check, retry on failure, JSON report, --workers flag. Benchmark: 50 checks sequential vs async. Commit. |

### Week 26 — Docker, Kubernetes & Python SDKs

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 126 | Docker concepts & docker-py | Container: isolated process · Image: read-only template · docker run build ps exec logs · docker-py Python SDK | `client = docker.from_env()` · `client.containers.list()` · `container.logs() container.stats()` | List running containers with docker-py · Get CPU + memory stats for container · Pull and run nginx from Python |
| 127 | Kubernetes concepts & kubectl | Pod: smallest unit · Deployment: manages replicas · Service: stable endpoint · Namespace: logical partition | `kubectl get pods -n production` · `kubectl describe pod web-01` · `kubectl logs web-01 -f` · `kubectl exec -it web-01 -- bash` | List all pods in all namespaces · Describe a failing pod and read events · Find all pods with CPU requests > 500m |
| 128 | Kubernetes Python client | `pip install kubernetes` · `config.load_kube_config()` · CoreV1Api AppsV1Api · List watch patch resources | `v1 = client.CoreV1Api()` · `pods = v1.list_namespaced_pod('production')` | List all pods with status · Find all pods in CrashLoopBackOff · Get node resource usage (capacity vs allocatable) |
| 129 | Building a K8s health dashboard | K8s client + Prometheus + rich output · Cluster health pattern · Watch events and alert | `rich` library for terminal UI · Table of pods with color-coded status · Watch pod events · Alert on CrashLoopBackOff OOMKilled | Display all pods with colored status using rich · Find all recently restarted pods (restarts > 5) · Output cluster health as JSON |
| 130 | **CAPSTONE** — K8s health dashboard | Full SRE automation tool — Phase 5 finale | All Phase 5 skills combined · Rich terminal + JSON modes | **Project:** `k8s-health-dashboard.py` — connects to K8s, colored pod status table, finds unhealthy pods, checks node resources, exports Prometheus metrics, --namespace --output flags. Full README + tests. Tag v1.0.0. |

---

# PHASE 6 — Generative AI: LLMs, RAG, Agents
**Month 7 · Weeks 27–32 · 30 days**
**Goal:** Understand LLMs deeply. Build RAG pipelines. Create agentic systems. Stay relevant in AI.

### Week 27 — How LLMs Actually Work

> **Bridge note (before Day 131):** You've reached AI territory. For the next 70 days you'll be coding with AI assistance — Claude Code, Cursor, or the Claude web app. Spend **1 evening (not a full day, just 90 min)** before Day 131 learning this properly. You'll save weeks of bad habits.
>
> **AI coding workflow principles:**
> - **Context is everything.** Before asking for code, paste the relevant file. Don't describe it.
> - **Small asks, tight loops.** "Add error handling to this function" beats "build me a monitoring system."
> - **Read every line before accepting.** Never copy code you don't understand — Month 3 rule still applies.
> - **Ask for tests alongside code.** "Write this function AND a pytest test for it."
> - **Use the model's full context.** For refactors, paste the whole file not a snippet.
> - **When stuck, ask the AI to explain its own output.** "Walk me through what this does line by line."
> - **Commit AI-assisted code with a marker:** `feat: add retry logic (AI-assisted)` — honest attribution
>
> **Your tools for the rest of the journey:** Claude web app (conversations, review), Claude Code (terminal-native coding agent for larger tasks), VS Code + Claude extension (inline help). Pick one as your primary; don't jump between all three.

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 131 | Tokens and tokenization | Token ≈ 0.75 words · Tokenizer splits into sub-word units · Why it matters: cost + context limit · Vocabulary ~100k | `import tiktoken; enc.encode('Hello, world!')` · Count tokens before sending | Count tokens in your SRE notes · Why does 'tokenization' cost more than 'tokens'? · Build a token counter for log files |
| 132 | Transformers & attention (conceptual) | Self-attention: each token attends to all others · Query Key Value · Multi-head attention · Context window = max tokens | Visualize attention: 'cat' attends to 'sat' · Why longer context costs more exponentially | Draw transformer block from memory · Why can't LLMs remember across conversations? · GPT (decoder-only) vs BERT (encoder)? |
| 133 | Embeddings — dense vectors | Embedding: float vector representing meaning · Similar meaning = close vectors · 1536 dimensions · Cosine similarity | `openai.embeddings.create(model='text-embedding-3-small', input=text)` · `cosine_similarity(vec1, vec2)` | Embed 10 SRE terms. Which are closest? · Implement cosine_similarity() from scratch · Why do similar documents have similar embeddings? |
| 134 | Temperature, sampling, context | Temperature 0: deterministic, 1: creative · top_p nucleus sampling · Context = system+messages+response tokens · Prompt caching | `client.messages.create(temperature=0)` · `max_tokens: limit response` · Context: 200k tokens for Claude | Call Claude at temp 0 vs 1. Note differences. · What happens if input exceeds context? · Calculate cost: 1000 calls × 500 tokens |
| 135 | **CAPSTONE** — LLM concepts doc | Consolidate for CCA cert · Explain without jargon | Write explanations as if teaching beginner · Draw transformer from memory | **Project:** Create `llm-concepts.md` — explain tokenization, embeddings, attention, temperature, context window in your own words. Commit to interview-qa/genai/. |

### Week 28 — Claude API & Prompt Engineering

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 136 | Claude API — Messages API | `pip install anthropic` · Messages: role:user / role:assistant · System prompt · streaming=True | `msg = client.messages.create(model='claude-sonnet-4-6', max_tokens=1024, messages=[...])` · `print(msg.content[0].text)` | Send first message to Claude API · Build chat loop with message history · Add streaming output |
| 137 | Context + Prompt Engineering | Prompt engineering = crafting the instruction · Context engineering = managing what else is in the window (RAG chunks, tool results, history, system prompt) · In production, context is bigger problem than prompt · System prompt + few-shot + CoT + XML tags · Context: order matters, lost-in-the-middle problem, context poisoning | `system='You are an SRE. Respond in JSON only.'` · Few-shot: 2 examples before real query · `'<scratchpad> think here </scratchpad>'` · Context budget: 200k tokens — but quality degrades past 50k · Place critical instructions at start AND end | Write system prompt for SRE incident classifier · Few-shot classify log severity · Get Claude to return structured JSON only · What is the lost-in-the-middle problem? · Design a context budget for a 10-turn agent conversation |
| 138 | Tool use (function calling) | Tools let Claude call your functions · Define: name description input_schema · Claude decides when to call · You execute + return result | `tools=[{'name':'get_disk_usage','description':'...','input_schema':{...}}]` · Handle tool_use block · Execute + return tool_result | Define get_cpu_usage tool. Have Claude call it. · 2-tool system: get_logs + search_runbook · What if Claude calls tool with invalid args? |
| 139 | OpenAI API comparison | Same concepts different SDK · `openai.chat.completions.create()` · Function calling same structure · Key differences: pricing models context | `client.chat.completions.create(model='gpt-4o', messages=[...])` · `response.choices[0].message.content` | Rewrite Claude tool-use example for OpenAI · Build abstraction: `llm_call(provider, messages)` · When choose Claude vs GPT-4? |
| 140 | **CAPSTONE** — SRE log classifier | First real AI-powered SRE tool | System: expert SRE classify severity · Input: log line → Output: JSON · Few-shot with 5 examples | **Project:** `log-classifier.py` — reads log file, sends each ERROR line to Claude for classification (severity/urgency/action), outputs JSON report. Uses few-shot. Commit. |

### Week 29 — Vector Databases & Embeddings Deep Dive

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 141 | Embeddings in practice | Choosing model: size vs quality · Batch for efficiency · Cache to avoid re-embedding · PCA t-SNE for visualization | `openai.embeddings.create(input=texts, model='text-embedding-3-small')` · Batch 100 texts · Cache in dict or SQLite | Embed your 40 Linux days — find most similar · Build embedding cache · Plot clusters with matplotlib |
| 142 | ChromaDB + local LLMs (Ollama, llama.cpp) | ChromaDB: open source vector DB runs locally · `add()` documents, `query()` by similarity · **Ollama**: run LLaMA/Mistral/Phi locally, one command · **llama.cpp**: C++ runtime for quantized models on CPU/GPU · Why SRE needs this: air-gapped environments, no egress, cost control, offline ops | `client = chromadb.Client()` · `collection.query(query_texts=['disk full'], n_results=3)` · `ollama run llama3.2` · `ollama serve` exposes OpenAI-compatible API on :11434 · `llama-cpp-python` for Python integration | Store all bash toolkit docs in ChromaDB · Query 'how do I check disk usage?' · Install Ollama, run llama3.2 locally · Swap Claude API for local Ollama in one of your scripts · When would you choose local vs API? List 3 scenarios each |
| 143 | Chunking strategies | Fixed size: every N chars/tokens · Recursive: split on paragraph sentence word · Semantic: split on meaning change · Chunk overlap | `RecursiveCharacterTextSplitter` · `chunk_overlap=50` | Chunk SRE notes 3 ways: compare retrieval quality · Best chunk size for SRE content? · How does overlap affect retrieval? |
| 144 | Pinecone & FAISS comparison | FAISS: Meta's local similarity search · Pinecone: managed cloud vector DB · FAISS: fastest local no filtering · Pinecone: scalable filtering namespaces | `import faiss; index = faiss.IndexFlatL2(1536)` · `index.add(vectors); index.search(query, k=5)` | Same search in ChromaDB vs FAISS — compare speed · When choose Pinecone over ChromaDB? · What is approximate nearest neighbor search? |
| 145 | **CAPSTONE** — SRE knowledge base | Embed your own SRE knowledge · Searchable store | Embed all Phase 1 day notes · Store in ChromaDB · Search: 'how to find zombie processes' | **Project:** `sre-knowledge-base.py` — embeds all sre-learning-journal markdown into ChromaDB, search CLI (--query 'question' --top-k 5). Run 10 SRE questions through it. Commit. |

### Week 30 — RAG — Full End-to-End Pipeline

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 146 | RAG architecture | 3 phases: ingest retrieve generate · Why RAG beats fine-tuning for fresh data · RAGAS evaluation: precision recall faithfulness | Ingest: chunk→embed→store · Retrieve: embed query→similarity→top-k · Generate: chunks+query→LLM→answer | Draw full RAG pipeline from memory · Failure modes of RAG? · When RAG over fine-tuning? |
| 147 | Building the ingestion pipeline | Document loading: PDF markdown text · Chunking with metadata: source date section · Deduplication · Incremental updates | Load all markdown from sre-learning-journal/ · Chunk with RecursiveCharacterTextSplitter · Add metadata: `{'source': 'linux/week1/day01.md'}` | Build ingestion pipeline for your entire journal · Add --force-reindex flag · How to handle updates when source files change? |
| 148 | Retrieval strategies | Similarity search: cosine/dot product · MMR: Maximum Marginal Relevance diversity · Hybrid: vector + keyword (BM25) · Re-ranking | `collection.query(query_texts=q, n_results=5)` · BM25 + vector: combine scores · cross-encoder reranking | Compare top-5: similarity vs MMR · Implement simple BM25 + vector hybrid · When does MMR help more than similarity? |
| 149 | LlamaIndex for production RAG | High-level RAG framework · VectorStoreIndex: auto-ingest + query · ServiceContext config · Query engines | `documents = SimpleDirectoryReader('sre-journal/').load_data()` · `index = VectorStoreIndex.from_documents(documents)` · `response = query_engine.query('How do I debug a zombie process?')` | Build LlamaIndex RAG over Phase 1 notes · Compare manual RAG vs LlamaIndex · Add custom system prompt to query engine |
| 150 | **CAPSTONE** — RAG over SRE runbooks | Full production RAG pipeline | Ingest all notes + 10 sample runbooks · Retrieve top 5 chunks · Claude synthesizes answer · Show sources | **Project:** `sre-rag-assistant.py` — full RAG — ingests journal + runbooks, answers SRE questions with sources, CLI + streaming. Evaluate 5 test questions. Commit. |

### Week 31 — AI Agents Deep Dive

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 151 | Agent anatomy + memory types | Agent loop: observe→plan→act→observe · Tools = agent's hands · Memory types: in-context (conversation), external (vector DB long-term), episodic (past runs), working (current task) · ReAct pattern: Reason + Act | While not done: think, pick tool, call tool, observe · `messages` list growing · `semantic_memory.search('past disk issues')` · Log every run to SQLite | Trace 3-step agent execution on paper · Difference between chatbot and agent? · Add external memory pattern: recall past incidents · Failure modes of autonomous agent? |
| 152 | LangGraph — stateful agents (production standard) | Graph-based framework · Node=function Edge=transition · State=shared dict · Conditional edges branch on state · Checkpointing for long-running agents | `graph = StateGraph(AgentState)` · `graph.add_node('check_logs', check_logs_node)` · `graph.add_conditional_edges('check_logs', should_escalate, {'yes':'alert','no':END})` · `graph.compile(checkpointer=MemorySaver())` | 3-node graph: triage→investigate→report · Conditional edge: if critical→alert else→log · Advantage of LangGraph over while loop? · Why do production agents need checkpointing? |
| 153 | Pydantic AI — type-safe agents | Type-safe agent framework from Pydantic team · Dependencies injected, outputs validated · Best for production reliability · Your type hints become agent contracts | `from pydantic_ai import Agent` · `agent = Agent('claude-sonnet-4-6', result_type=IncidentReport)` · `@agent.tool def get_disk(ctx, path: str) -> DiskInfo:` · Runtime validation via Pydantic models | Rebuild Day 152 SRE agent in Pydantic AI · Compare: LangGraph vs Pydantic AI — which is clearer? · When would type-safety prevent a production bug? · Define IncidentReport Pydantic model with 5 fields |
| 154 | Multi-agent orchestration — AutoGen + CrewAI | AutoGen: Microsoft's event-driven multi-agent · CrewAI: role-based agent teams · Orchestrator assigns to specialist sub-agents · Human-in-the-loop: approval before destructive action | AutoGen: `AssistantAgent`, `UserProxyAgent`, `GroupChat` · CrewAI: `Agent(role='Log Analyst', goal='...')`, `Task(description='...')`, `Crew(agents=[...], tasks=[...])` · `asyncio.gather()` parallel agents | Build same orchestrator in both AutoGen and CrewAI — compare · When is a multi-agent system actually better than one agent with more tools? · Failure modes of multi-agent systems · Human-in-the-loop before any `rm` or restart |
| 155 | **CAPSTONE** — multi-tool SRE agent (pick your framework) | Real agentic SRE workflow · Multi-step investigation · Pick framework based on project fit | Tools: read_logs search_runbook check_disk propose_fix · Framework of your choice (LangGraph recommended) · Human approval before action | **Project:** `sre-agent.py` — agent with 4 tools, takes incident description → investigates → proposes fix → asks approval. Document WHY you picked your framework in README. Commit. |

### Week 32 — MCP: Model Context Protocol Deep Dive

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 156 | MCP architecture — the full protocol | JSON-RPC 2.0 over stdio or SSE · 3 primitives: Tools (actions) Resources (data) Prompts (templates) · Lifecycle: initialize → capabilities negotiation → request/response → shutdown | `pip install mcp` · MCP message: `{jsonrpc:'2.0', method:'tools/call', params:{name:'get_disk'}}` · `mcp dev server.py` — MCP Inspector | Draw full MCP lifecycle on paper: connect→negotiate→call→respond→shutdown · stdio vs SSE transport: when use each? · Why JSON-RPC 2.0 instead of REST? · Run: `python -c 'import mcp; print(mcp.__version__)'` |
| 157 | Building MCP Tools — your first server | Tool = callable function with JSON Schema inputs · `@mcp.tool()` decorator: name+description auto-generated from function · Return TextContent ImageContent EmbeddedResource · Raise McpError for errors | `from mcp.server.fastmcp import FastMCP` · `mcp = FastMCP('sre-tools')` · `@mcp.tool() async def get_disk_usage(path: str) -> str:` · `mcp.run(transport='stdio')` · `mcp dev server.py` to test | Build MCP server with 3 tools: get_cpu_percent() get_disk_usage(path) get_top_processes(n) · Add docstrings — MCP uses them as tool descriptions · Test each tool using `mcp dev server.py` Inspector · What happens when a tool raises an exception? |
| 158 | MCP Resources and Prompts | Resource = read-only data at URI: `logs://nginx/access` `file:///etc/hosts` · Resource template: parameterised `logs://{server}/{logfile}` · Prompt = reusable template → slash command in Claude Desktop · Tools DO. Resources READ. Prompts SCAFFOLD. | `@mcp.resource('logs://{server}/{logfile}') async def get_log(server:str, logfile:str) -> str:` · `@mcp.prompt() def incident_triage(severity:str, description:str) -> str:` · `claude_desktop_config.json` to connect to Claude Desktop | Add 2 resources: logs://nginx/access and config://prometheus · Add prompt `/sre-runbook` with service_name and symptom args · Add server to claude_desktop_config.json · Test /sre-runbook prompt appears as slash command in Claude Desktop |
| 159 | MCP Sampling, Security & Multi-server | Sampling: server asks CLIENT to make LLM call → `ctx.request_context.session.create_message()` · Multi-server: Claude connects to many simultaneously · Input validation: guard all paths · Rate limiting inside server · `uvx mcp-server-git` install community servers | Sampling: when disk > 90% ask Claude to draft alert · `claude_desktop_config.json` with multiple servers listed · Input guard: `assert path.startswith('/var/log')` · Add mcp-server-git alongside your server | Add sampling: disk > 90% → Claude drafts alert message · Add input validation to every tool · Add mcp-server-git to Claude Desktop config alongside yours · 3 security risks of shell-access MCP server. Write mitigations. · Rate limiter inside server: max 10 calls/min per tool |
| 160 | **PHASE 6 CAPSTONE** — Production SRE AI assistant with full MCP stack | Production MCP server: Docker container proper logging graceful shutdown · All Phase 6 combined: MCP + RAG + LangGraph + LangSmith + cost tracking · **OpenClaw study session** (2 hours): the closest production analog to what you're building | MCP server: 6 tools + 2 resources + 2 prompts · `Dockerfile: FROM python:3.12-slim` · LangGraph agent using MCP tools via langchain-mcp-adapters · LangSmith traces every run · Human-in-loop: agent pauses and waits y/n | **Project:** `sre-ai-assistant/` — (1) `mcp_server.py`: 6 tools, 2 resources, 2 prompts, Dockerfile (2) `agent.py`: LangGraph stateful agent + RAG runbook search (3) LangSmith tracing (4) `cost_tracker.py` (5) Full README + architecture diagram + 5-min demo video. Tag v1.0.0. · **Plus: OpenClaw study (see below)** · This is the centrepiece of your SRE + AI portfolio. |

#### Day 160 OpenClaw study session — 2 hours, structured

OpenClaw (openclaw.ai) is a production personal AI agent that runs locally, uses MCP natively, and has a self-extending skill system. It's the closest real-world analog to what you just built. Spend 2 hours reverse-engineering it before you tag v1.0.0 of your own project.

**Hour 1 — read the code:**
1. Clone the repo: `git clone https://github.com/openclaw/openclaw && cd openclaw`
2. Find and read these files in order: `README.md` → main entry point → MCP server setup → skill loader → agent loop
3. Note every architectural decision you don't understand. Search for it in the docs.

**Hour 2 — answer these 7 questions in writing in `interview-qa/genai/openclaw-study.md`:**
1. How does OpenClaw discover and load skills at runtime? Does it use the MCP `tools/list` mechanism or something custom?
2. How does it handle multi-step tasks? Is it a stateful agent (like your LangGraph) or stateless?
3. What model does it default to? Can you swap it for a local Ollama model?
4. How does it handle credentials and secrets? (This is where most agents fail.)
5. What is its memory model — does it persist conversation history? Across sessions?
6. How does it sandbox skill execution? What can a malicious skill do?
7. **The big one:** What does OpenClaw do better than your `sre-ai-assistant`? What does yours do better?

**Outcome:** You will have a written comparison document showing how a real production agent solves the same problems you just solved. This becomes a portfolio piece — interviewers love seeing engineers who reverse-engineer competitors. Commit it. |

---

# PHASE 7 — AI System Design & GPU Operations
**Month 8 · Weeks 33–36 · 20 days**
**Goal:** Architect production AI systems. Understand GPU ops. Design for scale, reliability, cost.

### Week 33 — AI System Design Patterns

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 161 | Latency, throughput, cost tradeoffs | TTFT: time to first token · Throughput: tokens/sec requests/sec · Cost: input+output tokens × price · You can optimise 2 of 3 | Measure TTFT with streaming · Batch: higher throughput higher latency · Model routing: fast cheap vs slow expensive | Draw latency/throughput/cost triangle · Real-time chatbot: which matters most? · Nightly log analysis: optimal strategy? |
| 162 | Caching strategies for LLM apps | Semantic cache: cache by meaning · Prompt cache: cache repeated prefixes (Claude) · Response cache: exact match · Cache invalidation: TTL version-based | Semantic cache: embed query find similar · `cache_control` for system prompts · Redis for response caching | Cache for FAQ chatbot: what to cache? · Hit rate needed for caching to be worthwhile? · How to handle cache invalidation for live data? |
| 163 | Fallback chains, circuit breakers | Primary → fallback → fallback chain · Circuit breaker: stop calling failing service · Token bucket rate limiter · Graceful degradation | `try claude except RateLimitError: try gpt-4 except: return cached` · Circuit breaker: fail after 5 errors reset after 30s | Implement 3-level fallback chain · Circuit breaker for LLM calls · Design rate limiting for 1000 concurrent users |
| 164 | Streaming, batching, async patterns | Streaming: SSE for real-time · Batching: group requests for throughput · Async everywhere: don't block · Queue-based: decouple request from processing | FastAPI + SSE for streaming · Batch 10 requests every 100ms · Redis Queue + worker pool | Build streaming FastAPI endpoint for Claude · Batch 10 log classification requests · Design queue-based async LLM processing |
| 165 | **CAPSTONE** — system design review | Design production RAG API | Architecture: API→queue→LLM→cache→DB · Identify SPOFs · Cost model: 1M requests/month | **Project:** `sre-ai-system-design.md` — production RAG API for 10k requests/day. Architecture diagram, caching strategy, fallback chain, rate limiting, cost estimate. Commit to projects/. |

### Week 34 — GPU Operations & NVIDIA (NCP-AIO prep)

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 166 | GPU vs CPU for AI workloads | CPU: few fast cores general purpose · GPU: thousands slow cores parallel math · CUDA: NVIDIA parallel computing · Why matrix multiply loves GPUs | `nvidia-smi` · `nvidia-smi --query-gpu=utilization.gpu,memory.used --format=csv` · CUDA cores vs tensor cores | GPU vs CPU for transformer inference? · What is VRAM and why does it matter for LLMs? · First 5 things you'd check on a GPU? |
| 167 | Model inference — quantization, batching | FP32 vs FP16 vs INT8 · Quantization: reduce precision save memory · Batch size: more items per forward pass · KV cache: store attention keys/values | FP16: 2x less VRAM same quality · INT8: 4x less VRAM slight quality drop · KV cache growth: n_tokens × n_layers × d_model | Model needs 24GB VRAM. You have 16GB. What do you do? · Batch size vs latency tradeoff? · Explain KV cache in your own words |
| 168 | NVIDIA DCGM & GPU monitoring | DCGM: Data Center GPU Manager · Metrics: GPU utilisation memory temp power · `dcgmi` command line · Prometheus: dcgm-exporter for /metrics | `dcgmi discovery -l` · `dcgm-exporter: /metrics` · Grafana dashboard for GPU fleet | Metrics to alert on for inference GPU? · PromQL for GPU memory > 90%? · GPU health runbook: response if temp > 85°C? |
| 169 | Kubernetes for AI workloads | `nvidia.com/gpu`: K8s GPU resource · Device plugin: exposes GPU to scheduler · Node affinity: schedule on GPU nodes · Resource quotas per namespace | `resources: limits: nvidia.com/gpu: '1'` · `kubectl describe node gpu-node \| grep gpu` · `nodeSelector: accelerator: nvidia-tesla-v100` | K8s manifest for GPU inference pod · Share GPU between multiple pods? · What happens when all GPU nodes are full? |
| 170 | **CAPSTONE** — GPU ops runbook | NCP-AIO exam prep · GPU monitoring + incident response | GPU health check script · Prometheus alert rules · K8s GPU deployment manifest | **Project:** `gpu-ops-runbook.md` — GPU monitoring setup (DCGM + Prometheus), alert thresholds, incident response for OOM/high temp/utilisation, K8s GPU scheduling notes. Commit to projects/. |

### Week 35 — Observability for AI Systems

| Day | Topic | Theory | Examples | Challenges |
|-----|-------|--------|----------|------------|
| 171 | LLM-specific metrics | TTFT: time to first token · TBT: time between tokens · Total latency = TTFT + (TBT × output_tokens) · Error rate: 4xx 5xx LLM errors | `Histogram: ttft_seconds{model='claude'}` · `Counter: llm_requests_total{model,status}` · `token_count_total{type='input'}` | Add Prometheus metrics to sre-rag-assistant.py · What is p99 latency and why track it not average? · Write 5 PromQL expressions for LLM monitoring |
| 172 | OpenTelemetry tracing for AI | Trace: end-to-end journey · Span: one unit of work · Baggage: context propagated · OTLP: export protocol | `with tracer.start_as_current_span('llm-call'):` · Export to Jaeger Zipkin Grafana Tempo | Add OTel tracing to sre-ai-assistant · Trace: user request → retrieval → LLM call → response · What goes in the LLM span? |
| 173 | Grafana dashboards for AI | Dashboard: AI system health at a glance · Alerting: PagerDuty/Slack · SLI/SLO: define and track | LLM latency panel: p50/p95/p99 · Error rate panel · Token cost panel · Availability over 30 days | Design 6-panel Grafana dashboard · SLOs: availability 99.9% p99 latency < 5s · What alert would wake you up at 3am? |
| 174 | Full system design workshop | Whiteboard architecture review · Tradeoff analysis · Design AI incident response system | Components: API queue LLM RAG DB monitoring · Failure modes: what breaks? how to recover? · Cost model: 50k incidents/month × 2000 tokens | Design AI system for 50k SRE incidents/month · 3 single points of failure · Monthly LLM cost estimate · Disaster recovery plan? |
| 175 | **CAPSTONE** — AI system design doc | Production system design document | Architecture diagram · Component specs · Runbooks per failure mode · Cost projection | **Project:** `ai-system-design-doc.md` — design production SRE AI assistant for 50k incidents/month. Architecture diagram (ASCII or linked image), component specs, caching strategy, observability, cost model, DR plan. Commit. |

### Week 36 — Design Mock Interviews

| Day | Topic | Challenges |
|-----|-------|------------|
| 176 | System design mock — RAG at scale | 45-min mock: Design RAG for 10M documents. State assumptions, draw architecture, estimate cost. What corners did you cut? |
| 177 | System design mock — ML inference platform | 45-min mock: Design model serving platform for 100 models. Handle 100x traffic spike. Blue-green deployment for models. |
| 178 | CCA practice — architect exam questions | 30 mock MCQ. Write 5 architect-level prompts. Explain: constitutional AI RLHF safety. |
| 179 | NCP-AIO practice — GPU ops exam | 30 mock MCQ. Explain: CUDA architecture tensor cores NVLink. K8s GPU scheduling: multi-instance GPU. |
| 180 | **Phase 7 complete** | Review all 4 weeks. Update system design doc with mock interview lessons. Write phase7-reflection.md. Commit all outstanding work. |

---

# PHASE 8 — Certification Prep: CCA + NCP-AIO
**Month 9 · Weeks 37–40 · 20 days**
**Goal:** Pass both certifications. Consolidated, not crammed — you've been building to this.

### Week 37 — CCA Deep Dive

| Day | Topic | Challenges |
|-----|-------|------------|
| 181 | CCA: Prompt engineering mastery | Write 10 production system prompts for different use cases. Eval each with edge cases. |
| 182 | CCA: Claude API deep dive | Build feature demo for every Claude API capability. Batch API async. Vision API with a system diagram. |
| 183 | CCA: Safety & responsible AI | Write: when to refuse vs help with nuanced requests. 10 edge cases. Design safety guardrails. |
| 184 | CCA: 50 practice questions | 50 MCQ in 60 minutes. Score yourself. Target > 80%. Review every wrong answer. |
| 185 | **CAPSTONE** — CCA mock exam | **Project:** `cca-mock-exam.md` — 50 questions, all CCA domains, self-scored with explanations. Target 85%+. Schedule real CCA exam. |

### Week 38 — NCP-AIO Deep Dive

| Day | Topic | Challenges |
|-----|-------|------------|
| 186 | NCP-AIO: GPU architecture | Draw NVIDIA Ampere architecture from memory. Explain streaming multiprocessor. Why HBM bandwidth is crucial? |
| 187 | NCP-AIO: CUDA and inference optimization | Model parallelism vs data parallelism. When to use TensorRT over PyTorch? What is Flash Attention? |
| 188 | NCP-AIO: K8s for AI workloads | Manifest: 2 pods sharing GPU with MIG. Deploy DCGM exporter as DaemonSet. ResourceQuota: max 4 GPUs/namespace. |
| 189 | NCP-AIO: 50 practice questions | 50 MCQ in 60 minutes. Target 80%+. Flashcard every wrong answer. |
| 190 | **CAPSTONE** — NCP-AIO mock exam | **Project:** `ncp-aio-mock-exam.md` — 50 questions, GPU/CUDA/K8s/DCGM/inference. Self-scored. Target 85%+. Schedule real NCP-AIO exam. |

### Week 39 — Final Review & Gap Filling

| Day | Topic | Challenges |
|-----|-------|------------|
| 191 | CCA weak areas targeted review | Review 3 weakest CCA topics. 20 targeted practice questions. Update cca-prep/ notes. |
| 192 | NCP-AIO weak areas review | Review 3 weakest NCP-AIO topics. 20 targeted GPU questions. Update gpu-ops-runbook.md. |
| 193 | Full portfolio review | All 9 project READMEs reviewed and polished. Tag v1.0.0 on any untagged projects. |
| 194 | CCA timed mock — final | Full 60-min mock. No looking anything up. If > 85%: register for exam. |
| 195 | NCP-AIO timed mock — final | Full 60-min mock. No looking anything up. If > 85%: register for exam. |

### Week 40 — Exam Week & Reflection

| Day | Topic | Notes |
|-----|-------|-------|
| 196 | Day before CCA | Light review only. Read through cca-prep/ notes once. Sleep 8 hours. No cramming. |
| 197 | **CCA EXAM DAY** | Trust your preparation. Read every question fully. Flag uncertain, come back. Post result as GitHub issue. |
| 198 | Day before NCP-AIO | GPU architecture flashcards. DCGM metric names. K8s GPU scheduling review. Sleep 8 hours. |
| 199 | **NCP-AIO EXAM DAY** | Post result as GitHub issue. Update LinkedIn with both certifications. |
| 200 | **Day 200 — Journey complete** | **Project:** Write `journey-reflection.md` — what you learned, what surprised you, what you're proud of. Final commit. Tag v9.0.0. Share your GitHub with the world. |

---

## Apple SRE Interview Q&A Bank

Save your answers to `interview-qa/` as you go. By Month 9 you will have answered 100+ real interview questions.

**Process & OS**
- Walk me through what happens when you type `ls -la` in the terminal
- What is a zombie process? How is it created? How do you remove it?
- Explain the difference between SIGKILL and SIGTERM
- What is virtual memory and how does a page fault work?
- Explain load average — what do the three numbers mean?
- A process is using 100% CPU. Walk me through your debugging steps.
- What is the difference between a process and a thread?
- What happens during a context switch?
- How does the kernel decide which process runs next?

**Filesystem**
- What is an inode? What does it store? What doesn't it store?
- Explain the difference between a hard link and a soft link
- How would you find which process has a file open?
- A disk shows 90% full but you've deleted all big files. Why?
- Explain file descriptors. What is 2>&1?

**Networking & Performance**
- A server is running slowly. Top shows low CPU. What do you check?
- How would you find which process is using port 443?
- What does TIME_WAIT mean and is it a problem?
- Explain the TCP three-way handshake

**Bash & Scripting**
- What does `set -euo pipefail` do?
- Write a script to find the top 5 CPU-consuming processes
- What is the difference between `[ ]` and `[[ ]]`?
- How do you debug a bash script that isn't working?
- What does `2>&1` mean?

---

## Appendix — Agentic AI Frameworks Ecosystem (Reference)

A quick-reference map of the agentic AI landscape you will encounter. This is what Phase 6 prepares you to navigate. Save this and return to it whenever you need to pick a tool.

### Tier S — Use these in production

| Framework | What it is | When to reach for it | Covered in |
|-----------|-----------|----------------------|------------|
| **LangGraph** | Graph-based stateful agent framework | Production agents with branching logic, checkpointing, human-in-the-loop | Week 31 Day 152 |
| **Pydantic AI** | Type-safe agent framework | When reliability matters — dependencies injected, outputs validated by Pydantic | Week 31 Day 153 |
| **LlamaIndex** | RAG-focused framework | Document ingestion, chunking, retrieval at scale | Week 30 Day 149 |
| **MCP (Model Context Protocol)** | Open protocol for LLM ↔ tool connections | Exposing your infrastructure to any LLM client | Week 32 (full week) |
| **Raw Claude API + your own control flow** | No framework at all | Many SRE use cases don't need a framework — direct API is cleaner | Weeks 28–32 |

### Tier A — Know these, use when they fit

| Framework | What it is | When to reach for it | Covered in |
|-----------|-----------|----------------------|------------|
| **LangChain** | Foundation framework for LLM apps | Building blocks (chains, prompts, memory) — often used alongside LangGraph | Week 31 (as context) |
| **AutoGen** | Microsoft's multi-agent framework | Event-driven multi-agent systems with defined communication | Week 31 Day 154 |
| **CrewAI** | Role-based agent teams | Structured "team" workflows with specialist agents | Week 31 Day 154 |
| **Haystack** | Multimodal RAG + agents | Document-heavy use cases needing text + images together | Mentioned in Week 30 |

### Tier B — Worth knowing about

| Framework | What it is | When to reach for it |
|-----------|-----------|----------------------|
| **Semantic Kernel** | Microsoft C#/Java-first framework with Python support | Enterprise Microsoft stacks |
| **Mastra** | TypeScript-first with strong observability | JavaScript ecosystems |
| **MetaGPT** | Simulates software dev teams | Impressive demos, limited production fit |
| **Langflow / Dify** | Visual low-code workflow builders | Rapid prototyping before coding properly |

### Tier C — Study for concepts, not for production

| Framework | What it is | Why study it |
|-----------|-----------|--------------|
| **AutoGPT** | Pioneered autonomous agent loops | Historical importance — read the code once |
| **BabyAGI** | Iterative planning loop | Great for understanding the concept in ~200 lines |

### Production personal-agent case studies

| Project | What it shows |
|---------|---------------|
| **OpenClaw** | MCP-native local agent with self-extending skill system — study this in Week 32 Day 160 |

### Local LLM runtimes (for air-gapped / cost-sensitive SRE work)

| Tool | What it is | When to use it | Covered in |
|------|-----------|----------------|------------|
| **Ollama** | Simplest local LLM runner — one command to pull and run | Quick local prototyping, dev environments, learning | Week 29 Day 142 |
| **llama.cpp** | C++ inference engine for quantized models | Production local serving on CPU or modest GPUs | Week 29 Day 142 |
| **vLLM** | High-throughput inference server | Production LLM serving at scale (GPU required) | Phase 7 Day 167 |
| **TGI (Text Generation Inference)** | HuggingFace's production server | HF ecosystem, managed model deployments | Mentioned Phase 7 |

### Model sources and hubs

| Tool | What it is | Why it matters |
|------|-----------|----------------|
| **Hugging Face Transformers** | 500k+ pretrained models + Python SDK | Default source for embedding models, rerankers, open-weight LLMs |
| **DeepSeek-V3 / Llama 3 / Qwen / Mistral** | Open-weight frontier LLMs | Run via Ollama or llama.cpp — alternatives to API-only models |
| **sentence-transformers** | Open-source embedding models | Free alternative to OpenAI embeddings for RAG |

### AI coding agents (your daily tools for remaining 70 days)

| Tool | What it is | Best for |
|------|-----------|----------|
| **Claude Code** | Terminal-native coding agent with repo-wide context | Larger refactors, multi-file changes, feature implementation |
| **Claude web / Claude Desktop** | Conversational interface with MCP support | Learning, planning, code review, debugging |
| **Cursor** | AI-native fork of VS Code | Inline suggestions while typing |
| **Gemini CLI** | Google's terminal coding agent | Alternative to Claude Code if you're in Google ecosystem |

**My recommendation:** Pick ONE primary (Claude Code for coding-heavy work, Claude web for learning). Don't jump between all of them.

### RAG-specific alternatives to LlamaIndex

| Tool | What it is | When to use |
|------|-----------|-------------|
| **LlamaIndex** | Default — high-level RAG framework | Most RAG projects | 
| **RAGFlow** | Enterprise RAG with built-in chunking strategies | Document-heavy enterprise search |
| **Haystack** | Modular pipelines, multimodal support | When you need text + image retrieval |

### How to pick a framework (decision tree)

Ask yourself in this order:

1. **Do I need an agent at all?** — Many problems solve with RAG alone, or a simple LLM call. No agent = no framework needed.
2. **Do I need state across steps with branching logic?** → LangGraph
3. **Does output correctness matter more than agent flexibility?** → Pydantic AI
4. **Am I building on RAG?** → LlamaIndex
5. **Do I need multiple specialist agents?** → AutoGen or CrewAI
6. **Am I exposing tools to Claude Desktop or any MCP-compatible client?** → MCP (not an alternative to the above — pairs with them)
7. **Do I need to run offline / air-gapped / cheap?** → Ollama + llama.cpp with an open-weight model

**Rule of thumb:** Start with the simplest thing that works. You can always graduate from "raw API + dict for state" → "LangGraph" → "multi-agent system" as complexity demands. Going the other direction is painful.

---

## What is intentionally NOT in this syllabus

To keep the 9 months focused on SRE + AI, the following are **intentionally skipped**. They are fine topics — just not your path right now. If you need them later, they're additive.

| Topic | Why skipped | When you'd add it |
|-------|-------------|-------------------|
| **TensorFlow / PyTorch** | You're using LLMs, not training models | Only if you move into ML engineering |
| **Image generation** (Stable Diffusion, ComfyUI, Midjourney) | Not relevant to SRE work | Only for creative / product work |
| **Speech-to-text** (Whisper) | Not an SRE use case | If building audio pipelines |
| **Deep RL** | Conceptually covered via RLHF mentions | If you go into model training |
| **n8n / Zapier** | Visual automation tools, not production code | If doing ops automation in no-code orgs |
| **AutoGPT / BabyAGI** | Learning toys, superseded by LangGraph etc. | Read their source once for concepts |
| **Open WebUI / LibreChat** | ChatGPT-style UI clones — not engineering | If you need a team chat interface |

Your 9 months will make you the rare engineer who knows Linux deeply, can write clean Python, understands DSA, has built production SRE automation, AND knows how to architect AI systems. That combination is unusual and valuable. Don't dilute it.

---
*Start every session: "I am on Week X Day Y — [topic]. Continue."*
*Commit every day. Review every Sunday. Build every month.*


---

# PART 2 — Week 1 Full Detail (template for all future weeks)

> This is the level of detail you'll get for every week as you advance. Future weeks will be expanded into this format on demand — just say "expand Week X" when you finish the prior week.

> **Phase 1 · Month 1 · Days 1–5**
> **Goal:** Navigate any Linux/macOS filesystem confidently. Know what lives where. Answer Apple's first-round OS questions cold.
> **Time budget:** 5–6 hours total · ~60–70 min per day
> **You need:** Terminal open · VS Code with `linux/week1/` folder · `day01.md` through `day05.md` ready

---

## Before Day 1 — one-time setup (15 min)

```bash
# 1. Open terminal (Mac: Cmd+Space → Terminal)
# 2. Clone your repo and open in VS Code
git clone https://github.com/YOUR_USERNAME/sre-learning-journal.git
cd sre-learning-journal
mkdir -p linux/week1
code .

# 3. In VS Code: open linux/week1/day01.md on the left
#    Press Ctrl+` to open integrated terminal at the bottom
#    You now have notes + terminal side by side — this is permanent

# 4. Paste this template into EVERY day file before you start:
```

```markdown
# Day XX — [topic]

**Date:**
**Week:** 1 | **Phase:** Linux

---

## Theory — in my own words


## Commands I ran


## Output that surprised me


## What confused me


## Challenge answers


## Apple interview Q — my answer


## Commit hash
```

---

# Day 1 — The Linux Filesystem Hierarchy

## Theory (read this, then close it and explain it back)

### The single most important concept in Linux

On Windows you have `C:\`, `D:\`, `E:\` — a different root for every drive.

Linux has **exactly one tree**. Everything — every file, every disk, every USB drive, even your keyboard — hangs off a single root called `/`.

This is called the **Filesystem Hierarchy Standard (FHS)**. When you plug in a USB drive on Linux, it doesn't appear as `E:\`. It gets **mounted** at a folder like `/mnt/usb`. The USB drive's filesystem becomes part of the one big tree.

**The most important idea in all of Linux: everything is a file.**

- A regular file? A file.
- A directory? A special file.
- Your keyboard (`/dev/input/event0`)? A file.
- A network socket? A file.
- Live CPU info (`/proc/cpuinfo`)? A file. (A fake one — more on this Day 1.)

Once you internalize this, the whole operating system makes sense.

### The apartment building analogy

Think of `/` as the lobby of a giant apartment building.

- `/home` — the residential floor. Your apartment: `/home/siddharth`. All your personal files live here. `~` is shorthand for it.
- `/etc` — the management office. All the building's config files: how to connect to WiFi, what users exist, what services to run at startup.
- `/var` — the mailroom. Stuff that grows and changes: logs, mail, databases. `/var/log` is your best friend as an SRE — every incident starts here.
- `/tmp` — a whiteboard. Gets wiped on reboot. Never store anything important here.
- `/proc` — a holographic display. Looks like files but isn't. Pure kernel data served live. `cat /proc/cpuinfo` doesn't read a file from disk — the kernel generates that output on the fly.
- `/dev` — the utilities cupboard. Devices as files. `/dev/null` is a trash can that eats everything silently. `/dev/sda` is your first hard disk.
- `/usr/bin` — the staff room. All the programs ordinary users can run: `ls`, `grep`, `curl`.
- `/boot` — the engine room. Kernel and bootloader. Touch carefully — break this, machine won't start.

### The 12 directories every SRE must know cold

| Directory | What lives here | SRE relevance |
|-----------|-----------------|---------------|
| `/` | Root of everything | Starting point for all paths |
| `/home` | User home directories | Your scripts, dotfiles |
| `/etc` | System-wide config files | nginx.conf, sshd_config, cron jobs |
| `/var/log` | ALL system + app logs | **First place to look in any incident** |
| `/var` | Variable data that grows | Databases, mail, package caches |
| `/proc` | Virtual FS — live kernel data | `/proc/cpuinfo`, `/proc/meminfo`, `/proc/[pid]/` |
| `/tmp` | Temporary files | Wiped on reboot. Scripts use this for temp work. |
| `/dev` | Device files | `/dev/null`, `/dev/sda`, `/dev/random` |
| `/usr/bin` | User program binaries | `ls`, `grep`, `curl` live here |
| `/bin` | Essential binaries | Available even in rescue mode |
| `/boot` | Kernel + bootloader | Touch with extreme caution |
| `/mnt`, `/media` | Mount points | NFS shares, USB drives, network storage |

---

## Live examples — type every line, do not copy-paste

```bash
# ── Where am I? ───────────────────────────────────────────────
pwd
# Output: /Users/siddharth  (on Mac) or /home/siddharth (on Linux)

# ── Go to root and look around ────────────────────────────────
cd /
ls
# You should see: bin  dev  etc  home  tmp  usr  var  ...

# ── List with detail ──────────────────────────────────────────
ls -l        # long format: permissions, size, date
ls -la       # long format + hidden files (dotfiles starting with .)
ls -lh       # long format + human-readable sizes (KB, MB, GB)
ls -lha      # all three combined

# ── Navigate to key directories ───────────────────────────────
cd /etc
ls
# See: hosts  passwd  nginx/  ssh/  ... (varies by system)

cd /var/log
ls -lh
# See log files with sizes — on Mac this is system.log, on Linux syslog etc.

cd /tmp
ls -la
# Should be mostly empty unless your system just started something

# ── The ~ shortcut — always your home directory ───────────────
cd ~
pwd
# Back to /Users/siddharth

cd -
# Goes back to where you were before (toggle between two locations)
cd -
# Toggle again

# ── /proc — the virtual filesystem ───────────────────────────
ls /proc
# You see directories named by numbers (those are PIDs) and named files

cat /proc/cpuinfo
# Output: Live CPU data. On Mac: may not exist, use sysctl instead:
# sysctl -a | grep machdep.cpu

cat /proc/meminfo
# Output: Live memory stats from kernel. Not a real file on disk.

# ── Useful navigation shortcuts ───────────────────────────────
cd /usr/bin
ls | head -20          # first 20 programs installed

which ls               # where is the 'ls' program?
which python3          # where is Python?
which grep

file /bin/ls           # what TYPE of file is this?
# Output: /bin/ls: Mach-O 64-bit executable arm64 (Mac)
#         /bin/ls: ELF 64-bit LSB executable (Linux)

# ── The black hole ────────────────────────────────────────────
echo "this disappears" > /dev/null
# No output, no error — /dev/null silently ate it

ls /nonexistent 2> /dev/null
# Errors silenced — useful in scripts when you don't care about errors

# ── Create something and find it ──────────────────────────────
echo "hello from day 1" > /tmp/mytest.txt
cat /tmp/mytest.txt
ls -lh /tmp/mytest.txt

# ── The manual — your best friend ────────────────────────────
man ls
# Press: space = next page, b = back, /word = search, q = quit
```

**After running each block:** write the output (or describe what you saw) in your `day01.md` under "Commands I ran".

---

## Challenges — do not skip, do not look at answers first

### Challenge 1 — The Explorer (20 min)

Navigate to **at least 6** different directories using `cd`. For each one:
1. Run `ls -lh`
2. Write in your notebook: **what's inside** and **what you think it's for**

You must include: `/etc`, `/var/log`, `/proc`, `/tmp`, and your home directory `~`.

After exploring, come back and answer:
- What is the **largest directory** on your system? (hint: `du -sh /* 2>/dev/null | sort -rh | head -5`)
- What was the most **surprising** thing you found?
- What is in `/proc` that looks useful for an SRE?

> **Rule:** You cannot break anything by using `ls` and `cd`. Explore fearlessly. The only dangerous commands are ones that write or delete — and we're not doing that yet.

---

### Challenge 2 — The SRE First Response (15 min)

A senior engineer Slacks you:

> "The web server is behaving oddly. Can you SSH in and check the logs?"

You SSH in. Using **only what you learned today**, answer:

1. What command do you run first to orient yourself?
2. Where do logs live on a Linux system?
3. How do you list log files with their sizes to find the biggest one?
4. Write the exact sequence of 5 commands you'd run.

Write your answer in `day01.md` under "Challenge answers". **Do not Google.** This forces you to think.

---

### Challenge 3 — /proc Curiosity (10 min)

Run these two commands:

```bash
cat /proc/cpuinfo     # On Mac: sysctl -a | grep machdep.cpu | head -20
cat /proc/meminfo     # On Mac: sysctl -a | grep hw.memsize
```

Answer in your own words:
1. How many CPU cores does your machine have?
2. How much total memory does it show?
3. **Most important:** How do you know these are NOT real files stored on disk? What makes `/proc` different?

---

### Challenge 4 — GitHub commit (5 min)

In your `day01.md`, write:
- The **5 directories** you'll remember most and why
- **One command** that surprised you
- Your answer to: "What is `/dev/null`?" in your own words

Then:
```bash
cd ~/sre-learning-journal
git add linux/week1/day01.md
git commit -m "feat(linux): Week 1 Day 1 — filesystem and directory structure"
git push
```

> This habit starts today. Every session ends with a commit. No exceptions.

---

## Apple interview Q — answer this out loud before reading the guidance

> **"You SSH into a production server and need to quickly understand the system. What are the first 5 directories you look at and why?"**

**What Apple is testing:** Do you know the filesystem well enough to navigate under pressure without thinking?

**Strong answer structure:** Name the directory → say what lives there → say why it matters in an incident.

**Example of a strong answer:**
> "First I'd check `/var/log` because all system and application logs land there — it's the first place I go when something's wrong. Then `/etc` to understand the service configuration — what's installed, how it's configured. Then `/proc` to get live system state: CPU, memory, running processes. Then `/tmp` to see if any recent scripts or processes left artifacts. And `/home` or the application directory to understand who's been working on the system recently."

**Write your own version in `day01.md`** — don't copy mine. Then post it in chat for review.

---

## Day 1 checklist — before you move to Day 2

- [ ] Ran every example command above
- [ ] Completed all 4 challenges
- [ ] Wrote outputs and answers in day01.md
- [ ] Can name all 12 key directories from memory
- [ ] Can explain what `/proc` is without looking it up
- [ ] Answered the Apple interview Q in writing
- [ ] Committed and pushed to GitHub

---

# Day 2 — Essential Directories Deep Dive

## Theory

### /etc — the management office

Every configuration file that affects the whole system lives here. When nginx starts, it reads `/etc/nginx/nginx.conf`. When SSH authenticates you, it checks `/etc/ssh/sshd_config`. When the system boots and needs to know what users exist, it reads `/etc/passwd`.

Rule of thumb: **if you're changing how the system behaves, you're editing something in `/etc`.**

Key files to know:
- `/etc/hosts` — local DNS overrides. Add `127.0.0.1 myapp.local` and `myapp.local` resolves locally.
- `/etc/passwd` — user accounts (not passwords — that's `/etc/shadow`)
- `/etc/hostname` — the machine's name
- `/etc/crontab` — system-wide scheduled jobs
- `/etc/ssh/sshd_config` — SSH server configuration

### /var/log — your most important directory as an SRE

Every incident investigation starts here. Every service that runs on Linux writes its logs to `/var/log` or a subdirectory of it.

Key logs:
- `/var/log/syslog` or `/var/log/messages` — general system log
- `/var/log/auth.log` — authentication attempts (SSH logins, sudo usage)
- `/var/log/kern.log` — kernel messages
- `/var/log/nginx/access.log` — nginx web requests
- `/var/log/nginx/error.log` — nginx errors
- `/var/log/postgresql/` — database logs

On macOS: `/var/log/system.log` is the main system log.

### /proc — the matrix

`/proc` is a **pseudo-filesystem**. The files you see don't exist on disk. When you `cat /proc/cpuinfo`, the kernel generates that text output on the fly and hands it to you.

Why does this matter for SRE? Because `/proc` gives you live system state:
- `/proc/cpuinfo` — CPU details
- `/proc/meminfo` — memory breakdown
- `/proc/loadavg` — the three load average numbers
- `/proc/[PID]/` — everything about a running process: its file descriptors, memory maps, command line, status

When a process is misbehaving, `/proc/[PID]/` is where you look.

### /dev — devices as files

The "everything is a file" principle lives here.

Special devices you need to know:
- `/dev/null` — the black hole. Anything written here disappears. Used in scripts to silence output.
- `/dev/zero` — endless stream of zero bytes. Used to create empty files or wipe disks.
- `/dev/random` — truly random bytes. Slow (waits for hardware entropy).
- `/dev/urandom` — pseudo-random bytes. Fast. Use this for most purposes.
- `/dev/sda`, `/dev/sdb` — hard disk devices (Linux). `sda1` = first partition on first disk.

---

## Live examples

```bash
# ── /etc deep dive ────────────────────────────────────────────
cat /etc/hostname          # machine name
cat /etc/hosts             # local DNS overrides
cat /etc/shells            # shells available on this system
ls /etc/ | grep -i conf    # find all .conf files at top level
find /etc -name "*.conf" 2>/dev/null | head -10   # all .conf recursively

# ── /var/log exploration ──────────────────────────────────────
ls -lh /var/log            # list logs with sizes
ls -lht /var/log | head -5 # 5 most recently modified logs
# On Mac:
cat /var/log/system.log | tail -20    # last 20 lines
# Watch a log file live (open a new terminal to generate activity):
tail -f /var/log/system.log

# ── /proc exploration ─────────────────────────────────────────
cat /proc/loadavg          # load averages + running process count
# Output: 1.23 0.95 0.80 2/420 12345
#         1min  5min 15min  running/total  last_pid

cat /proc/uptime           # seconds since boot
# Output: 86400.33 340218.12
#         uptime   idle_time

ls /proc/ | grep -E '^[0-9]+$' | head -10  # PIDs of running processes
cat /proc/1/cmdline | tr '\0' ' '           # command that started PID 1

# ── /dev exploration ──────────────────────────────────────────
ls -la /dev/null /dev/zero /dev/random /dev/urandom
# These are "character special" files (c in ls output)

echo "test" > /dev/null             # silently discard
echo "test" 2> /dev/null            # silently discard errors
dd if=/dev/zero bs=1 count=10 | xxd # 10 zero bytes in hex

# ── Combining — find the biggest log file ─────────────────────
du -sh /var/log/* 2>/dev/null | sort -rh | head -5

# ── Finding things across the filesystem ──────────────────────
find /etc -name "hosts" 2>/dev/null
find /var/log -name "*.log" -size +1M 2>/dev/null   # logs over 1MB
find /tmp -mtime -1 2>/dev/null                      # files modified in last day
```

---

## Challenges

### Challenge 1 — /etc investigation (15 min)

1. Run `cat /etc/hosts`. What does each line do? Explain in your own words.
2. Run `cat /etc/shells`. What is this file for?
3. How many `.conf` files exist under `/etc`? Find out with one command.
4. What is the most recently modified file in `/etc`? Use `ls -lt /etc | head -5`.

### Challenge 2 — /var/log SRE simulation (15 min)

A production service just crashed. You SSH in. Run:

```bash
ls -lht /var/log | head -10
```

1. Which 3 log files would you look at first and why?
2. Run `tail -50 /var/log/system.log` (Mac) or `tail -50 /var/log/syslog` (Linux). What do you see?
3. Write a one-liner to search for the word "error" in all files in `/var/log` (case-insensitive).

### Challenge 3 — /proc live data (15 min)

1. Run `cat /proc/loadavg`. Write down what each number means.
2. Run `cat /proc/uptime`. Convert the first number to hours. How long has your machine been running?
3. Find the PID of your terminal process. Then run `ls /proc/[YOUR_PID]/`. What directories and files do you see there?

### Challenge 4 — /dev/null in practice (10 min)

Run this command and explain what happens to both stdout and stderr:

```bash
ls /etc /nonexistent 2>/dev/null
ls /etc /nonexistent > /dev/null
ls /etc /nonexistent > /dev/null 2>&1
```

Explain the difference between the three. Write your explanation in `day02.md`.

**Commit:** `git commit -m "feat(linux): Week 1 Day 2 — essential directories deep dive"`

---

## Apple interview Q

> **"What lives in `/etc` versus `/var` versus `/proc`? What is the difference?"**

Write your answer in 4 sentences. No jargon. As if explaining to a smart person who's never used Linux.

---

# Day 3 — Navigation & File Operations

## Theory

### The 10 commands you'll use every single day

These are not commands you look up. These are commands that come out of your fingers without thinking. By the end of this day, they will.

**Navigation:**
- `pwd` — print working directory (where am I?)
- `cd path` — change directory
- `cd ..` — go up one level
- `cd -` — toggle to last location
- `cd ~` — always go home

**Listing:**
- `ls` — simple list
- `ls -l` — long: permissions, owner, size, date
- `ls -la` — long + hidden files (dotfiles)
- `ls -lh` — long + human-readable sizes
- `ls -lt` — long + sorted by modification time (newest first)
- `ls -lS` — long + sorted by size (largest first)

**Creating:**
- `touch file.txt` — create empty file (or update timestamp)
- `mkdir dir` — create directory
- `mkdir -p a/b/c` — create full path including parents

**Copying and moving:**
- `cp source dest` — copy file
- `cp -r source/ dest/` — copy directory recursively
- `mv source dest` — move (also used to rename)

**Deleting:**
- `rm file.txt` — delete file (permanent, no trash)
- `rm -r directory/` — delete directory recursively
- `rm -rf directory/` — force, no prompts (use with caution)
- `rmdir directory/` — delete empty directory only

### The most dangerous command in Linux

```bash
rm -rf /
```

This deletes everything from root down. There is no trash. There is no undo. It is permanent. Modern systems have a `--no-preserve-root` guard but some don't. **Never, ever run this.**

The safer pattern when cleaning up: always specify exactly what you're deleting. `rm -rf /tmp/myspecificfolder/` not `rm -rf /tmp/*`.

---

## Live examples

```bash
# ── Create a test playground ──────────────────────────────────
cd ~
mkdir -p sre-practice/logs sre-practice/configs sre-practice/scripts
ls -la sre-practice/
tree sre-practice/   # if tree is installed; brew install tree on Mac

# ── Create files ──────────────────────────────────────────────
cd sre-practice/
touch logs/access.log logs/error.log logs/debug.log
touch configs/nginx.conf configs/app.conf
touch scripts/health_check.sh scripts/backup.sh
ls -la logs/ configs/ scripts/

# ── Brace expansion — create many files at once ───────────────
touch logs/server-{01,02,03,04,05}.log
ls logs/
# Creates: server-01.log server-02.log ... server-05.log

# ── Copy files ────────────────────────────────────────────────
cp logs/access.log logs/access.log.bak
cp -r logs/ logs-backup/
ls -la

# ── Move (rename) ─────────────────────────────────────────────
mv logs/debug.log logs/debug.log.old
mv configs/app.conf configs/app.conf.backup
ls logs/ configs/

# ── Absolute vs relative paths ────────────────────────────────
cd ~
ls sre-practice/logs           # relative path
ls ~/sre-practice/logs          # absolute using ~
ls /Users/$(whoami)/sre-practice/logs   # fully absolute

# ── Navigation tricks ─────────────────────────────────────────
cd /var/log
pwd
cd ~/sre-practice
pwd
cd -          # back to /var/log
pwd
cd -          # back to ~/sre-practice
pwd

# ── View file stats ───────────────────────────────────────────
stat sre-practice/logs/access.log
# Shows: inode, permissions, owner, size, access/modify/change times

# ── Disk usage ────────────────────────────────────────────────
du -sh sre-practice/         # total size of directory
du -sh sre-practice/*/       # size of each subdirectory
df -h                         # disk space on all mount points
df -h /                       # disk space on root partition
```

---

## Challenges

### Challenge 1 — Build a directory structure (15 min)

Create this exact structure using only `mkdir` and `touch`:

```
~/sre-project/
  app/
    src/
      main.py
      utils.py
    tests/
      test_main.py
  deploy/
    k8s/
      deployment.yaml
      service.yaml
    scripts/
      deploy.sh
      rollback.sh
  logs/
    app.log
    error.log
  README.md
```

Do it with the fewest commands possible. Hint: `mkdir -p` can create multiple paths, and `touch` can create multiple files.

### Challenge 2 — Copy, move, rename (10 min)

1. Copy the entire `deploy/` directory to `deploy-backup/`
2. Rename `app/src/utils.py` to `app/src/helpers.py`
3. Move both `logs/*.log` files into a new directory `logs/archive/`
4. Check final structure with `ls -lR ~/sre-project/`

### Challenge 3 — Safe deletion (10 min)

1. Delete `deploy-backup/` you just created
2. Delete just the `deploy.sh` file (not the whole scripts directory)
3. What would happen if you ran `rm -r ~/sre-project/`? (Don't actually run it — just explain.)

**Commit:** `git commit -m "feat(linux): Week 1 Day 3 — navigation and file operations"`

---

# Day 4 — Viewing & Searching Files

## Theory

### The tools SREs use 50 times a day

**Viewing file contents:**
- `cat file` — print entire file to screen (bad for large files)
- `less file` — page through file. Space=next, b=back, /word=search, q=quit. **Use this for large files.**
- `head -n 20 file` — first 20 lines
- `tail -n 20 file` — last 20 lines
- `tail -f file` — live: follow file as new lines are added. Press Ctrl+C to stop.

The most important: `tail -f`. When something breaks in production, you SSH in, run `tail -f /var/log/nginx/error.log`, and watch log lines appear in real time.

**Searching:**
- `grep pattern file` — find lines matching pattern
- `grep -i pattern file` — case insensitive
- `grep -n pattern file` — show line numbers
- `grep -r pattern dir/` — recursive: search all files in directory
- `grep -v pattern file` — invert: show lines that do NOT match

**Finding files:**
- `find /path -name "filename"` — find by name
- `find /path -name "*.log"` — find by pattern
- `find /path -type f` — only files (`-type d` for directories)
- `find /path -size +100M` — find files over 100MB
- `find /path -mtime -1` — modified in last 1 day

---

## Live examples

```bash
# ── Viewing files ─────────────────────────────────────────────
cat /etc/hosts                     # small file — cat is fine
less /etc/hosts                    # same file but with paging
head -5 /etc/hosts                 # first 5 lines
tail -5 /etc/hosts                 # last 5 lines

# ── tail -f — live log watching ───────────────────────────────
# Open TWO terminal windows.
# Terminal 1: watch the log
tail -f /var/log/system.log         # Mac
# tail -f /var/log/syslog           # Linux

# Terminal 2: generate some log activity
ping -c 3 google.com               # or any command

# Watch Terminal 1 — new lines appear as they're written

# Press Ctrl+C in Terminal 1 to stop

# ── grep — the workhorse ──────────────────────────────────────
grep "error" /var/log/system.log                    # case sensitive
grep -i "error" /var/log/system.log                 # case insensitive
grep -i "error" /var/log/system.log | head -20      # first 20 matches
grep -n "kernel" /var/log/system.log | head -10     # with line numbers
grep -v "^#" /etc/hosts                             # remove comment lines
grep -c "error" /var/log/system.log                 # count matches

# ── grep recursive ────────────────────────────────────────────
grep -r "localhost" /etc/ 2>/dev/null | head -10    # find localhost in all config files
grep -rl "127.0.0.1" /etc/ 2>/dev/null              # just filenames (-l flag)

# ── find files by name ────────────────────────────────────────
find /etc -name "*.conf" 2>/dev/null
find /var/log -name "*.log" 2>/dev/null
find /usr/bin -name "python*" 2>/dev/null

# ── find files by size ────────────────────────────────────────
find /var/log -size +1M 2>/dev/null    # over 1 megabyte
find /var/log -size +10M 2>/dev/null   # over 10 megabytes
find / -size +100M 2>/dev/null         # over 100MB anywhere (slow)

# ── find files by time ────────────────────────────────────────
find /var/log -mtime -1 2>/dev/null    # modified in last 1 day
find /tmp -mtime +7 2>/dev/null        # older than 7 days in /tmp

# ── Combining grep and find ───────────────────────────────────
find /etc -name "*.conf" 2>/dev/null | head -5  # find conf files
# Then read one:
cat $(find /etc -name "hosts" 2>/dev/null | head -1)
```

---

## Challenges

### Challenge 1 — Live log watching (10 min)

1. Open two terminals (or two VS Code terminal panels with the `+` button)
2. Terminal 1: `tail -f /var/log/system.log` (Mac) or `tail -f /var/log/syslog` (Linux)
3. Terminal 2: run a few commands (ping, ls, anything)
4. Watch Terminal 1. Write in `day04.md`: what kind of events appeared?
5. Stop with Ctrl+C.

### Challenge 2 — grep in production (15 min)

Using the log file from above:

1. Extract all lines containing the word "error" (case-insensitive). How many are there?
2. Find all lines that do NOT contain "kernel" — pipe through `head -20`.
3. Find all `.conf` files in `/etc` that contain the word "localhost".
4. Write the exact command for each.

### Challenge 3 — find in production (15 min)

1. Find all `.log` files in `/var/log` and list them sorted by size (combine `find` with `ls -lS` or `du -sh`).
2. Find all files modified in the last hour anywhere in `/var/log`.
3. Find any file on your system larger than 500MB (use `find / -size +500M 2>/dev/null`). What did you find?

**Commit:** `git commit -m "feat(linux): Week 1 Day 4 — viewing and searching files"`

---

# Day 5 — Week 1 Capstone

## Scenario

You are an SRE at a company. It's 2am. Your PagerDuty fires:

> **ALERT:** Production web server `web-01` is not responding. HTTP health checks failing. On-call engineer needed immediately.

You SSH into the server. You have never seen this machine before. You have one goal: **figure out what's wrong as fast as possible.**

You know only what you learned this week.

---

## Theory — the SRE first-response mental model

When you land on an unknown server in an incident, you follow a consistent pattern:

**Orient → Observe → Hypothesize → Act**

**Orient:** Get your bearings. What is this machine? What is it supposed to do?
```bash
hostname                  # what is this machine called?
uptime                    # how long has it been running? high load?
whoami                    # who am I logged in as?
pwd                       # where am I?
```

**Observe:** What is the system's state right now?
```bash
df -h                     # is disk full? (very common cause of failures)
free -h                   # is memory exhausted?
top                       # what is consuming CPU/memory?
ps aux | head -20         # what processes are running?
```

**Check the logs:** What happened just before the failure?
```bash
ls -lht /var/log | head -10          # which logs were recently modified?
tail -100 /var/log/nginx/error.log   # read the most relevant log
tail -100 /var/log/syslog            # system-level errors
```

**Understand the services:** What should be running? Is it running?
```bash
ls /etc/nginx/           # is nginx installed?
ls /etc/ | grep -i app   # any application config?
```

---

## The capstone exercise

Create a file called `~/sre-learning-journal/linux/week1/day05.md` and write your answers to all of the following. This is not a test with right answers — it's a forcing function to make you think.

### Section 1 — Your first-response runbook (30 min)

Write a numbered list of your **first 15 commands** when landing on an unknown production server. For each command:
- The exact command
- What it tells you
- What "bad" output looks like vs "normal" output

Example format:
```
1. hostname
   What: The machine's name — confirms you're on the right server
   Normal: A sensible hostname like web-01.prod.company.com
   Bad: Empty, or a hostname you don't recognise

2. uptime
   What: How long running, and the 1/5/15 minute load averages
   Normal: Load averages below the number of CPU cores
   Bad: Load average of 24.0 on a 4-core machine = something is seriously wrong
```

### Section 2 — Disk space investigation (20 min)

Run these commands and document what you find:

```bash
df -h
du -sh /var/log/* 2>/dev/null | sort -rh | head -10
find /var/log -name "*.log" -size +10M 2>/dev/null
```

Answer:
1. How full is your disk right now?
2. What is the largest log file?
3. If the disk were 100% full on a production server, what would you do?

### Section 3 — Apple interview answer (15 min)

Write a full, structured answer (minimum 8 sentences) to this question:

> **"You're on call and get paged at 2am. An alert says the production server is down. Walk me through exactly what you do from the moment you SSH in."**

This should show: systematic approach, knowledge of where to look, how you prioritise, how you communicate.

### Section 4 — Week 1 self-assessment

Answer honestly:
1. Which concept is clearest to you now?
2. Which concept is still fuzzy?
3. What is the one thing from this week you'll definitely remember in 6 months?

---

## Commit and push

```bash
cd ~/sre-learning-journal
git add linux/week1/
git commit -m "feat(linux): Week 1 Day 5 — capstone and first-response runbook"
git push
```

Then in this chat, paste:
> "Week 1 complete. Here is my first-response runbook: [paste Section 1]. Please review it as a senior SRE."

I will review it, give you specific feedback, and confirm whether you're ready for Week 2.

---

## Week 1 milestone — what you should be able to do

By the end of Day 5 you should be able to:

- [ ] Navigate the Linux filesystem without hesitation from memory
- [ ] Know what lives in `/etc`, `/var/log`, `/proc`, `/tmp`, `/dev` without looking it up
- [ ] Explain what `/proc` is and why its files aren't "real" files on disk
- [ ] Use `ls` with `-l`, `-a`, `-h`, `-t`, `-S` flags confidently
- [ ] Use `grep` to find text in files (with `-i`, `-n`, `-r`, `-v`)
- [ ] Use `find` to locate files by name, size, and modification time
- [ ] Use `tail -f` to watch a log file live
- [ ] Give a structured, confident answer to the Apple first-response interview question
- [ ] Have 5 committed files in your sre-learning-journal on GitHub

**If you cannot do all of these:** stay on Week 1 for another day and repeat the weakest area. We do not advance on a calendar.

**If you can do all of these:** post your capstone answers in chat and we move to Week 2 — File Permissions.

---

## Week 2 preview

Next week you will learn:
- How Linux permission bits (rwx) work and how to read `ls -l` output
- `chmod`, `chown`, `chgrp` — changing permissions and ownership
- The special bits: setuid, setgid, sticky — and why they matter for security
- `/etc/passwd`, `/etc/shadow` — the user database
- How to write a permissions audit script that finds dangerous configurations

The Apple interview questions next week: *"Explain what `-rwxr-xr--` means bit by bit"* and *"What is the setuid bit and give a real example?"*

---

*Post your Week 1 capstone here when done. No advancing without review.*
