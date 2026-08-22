https://1drv.ms/x/c/4bdbb19d7dd8d4da/IQDqK399I1wOTJ3w-_3CEaaYAQuMo7O89OTLD0AI5-B6Frw?e=aBXCgI


## What this role actually is
Juspay is a payments infrastructure company processing 300M+ transactions/day at 99.999% reliability. The backend org is famous for being one of the largest **Haskell/PureScript** shops in India. Their proprietary framework is called **Presto**, and roles are often labeled "FP Engineer for Backend." Even when a JD says generic "SDE Backend," the loop tends to be the same across teams, with heavy emphasis on DSA depth, systems thinking, and (for many teams) functional programming.

Your stack is Python/Django/Flask/Node with React/Next.js on the frontend. That is a real gap against their Haskell/PureScript core. Don't hide it — name it early, frame it as fast ramp-up capacity, and lean hard on your DSA and systems fundamentals, which is what actually gets you through most rounds.

## The typical loop (based on recent 2025–2026 candidate reports)
Process length varies (5 to 7 rounds), but the recurring shape is:

1. **Online Assessment (MCQ)**: OS, DBMS, OOP, Computer Networks, aptitude. Cutoff around 67%. Nothing exotic, just don't get rusty on basics.
2. **Coding Test**: 3 DSA problems, LeetCode medium to hard, often not standard/templated problems. Need at least 2 fully correct to clear.
3. **"Tree of Space" round**: A Juspay signature problem. You're asked to design a locking system on a generic M-ary tree (lock/unlock/upgrade a node, respecting ancestor/descendant lock state). This shows up across almost every recent report, so practice it explicitly (search "Tree of Space Juspay" or "GfG Juspay lock tree"). Advice from a past candidate: build the functional programming style solution first, it's easier to optimize incrementally.
4. **Hackathon Part A / B**: Extension of the tree locking problem, sometimes moving into concurrency, mutexes, and semaphores, i.e. handling concurrent lock/unlock requests safely. Treat this as a systems problem, not just a DSA problem.
5. **Systems/Design interview**: Less about drawing boxes, more about reasoning through consistency, availability, reliability, and efficiency trade offs. Often anchored on a project from your own resume, so be ready to go deep on your RFP Automation System or the Flask automation pipeline: why Redis, what happens under load, what fails first, how you'd scale it.
6. **HR / culture fit**: standard.

## Priority prep order (given your 2 to 3 week runway assumption)

### 1. DSA (highest leverage, non negotiable)
* Trees (generic/M-ary, not just binary): traversal, ancestor/descendant queries, lock style problems
* Graphs: BFS/DFS, topological sort — multiple reports mention graph based coding tests
* Two pointers, sliding window, greedy — these show up as the "easy" filter question, don't drop points here
* Fenwick Tree / segment tree at a conceptual level (came up as the "hard" question in one recent loop)
* Concurrency primitives: mutex vs semaphore, race conditions, deadlock avoidance — asked in the context of the lock tree problem

### 2. Core CS fundamentals (for the MCQ round)
* OS: process vs thread, scheduling, deadlocks, memory management
* DBMS: normalization, indexing, transactions/ACID, isolation levels
* OOP: SOLID principles, polymorphism/inheritance trade offs
* Computer Networks: TCP vs UDP, HTTP handshake, basics of load balancing/DNS

### 3. System design, anchored on your own projects
Be ready to defend, not just describe:
* RFP Automation System: what breaks at 10x volume, where the bottleneck is
* Flask automation pipeline with Redis: cache invalidation strategy, what happens if Redis goes down
* Legal AI Agent (Django + Next.js + InLegalLLaMA): latency, model serving trade offs

General payments-adjacent system design concepts worth knowing at a surface level, since this is a payments company: idempotency in payment APIs, retry safety, reconciliation, at least once vs exactly once delivery.

### 4. Functional programming exposure (bridge the gap, don't fake it)
You don't need to become a Haskell expert in two weeks, but walking in with zero exposure will hurt in FP-leaning rounds. Minimum viable prep:
* Spend a few hours on Haskell or PureScript basics: pure functions, immutability, pattern matching, algebraic data types, monads at a conceptual level (just enough to talk intelligently, not to write production code)
* Solve 3 to 5 of your practiced DSA problems in Haskell or PureScript instead of Python, so you have a genuine talking point
* Prepare a clean, honest line for this, consistent with how you've framed skill gaps before: something like "My production experience is in Python and Node, but I've spent time this month getting hands on with Haskell and PureScript because I understand Presto and your backend core are FP first, and I'm genuinely excited to go deep there."

## Questions you should ask them
* How much of the day to day backend work is PureScript/Haskell vs other stacks, for someone coming from an OOP/imperative background?
* What does ramp up look like for an engineer without prior FP experience joining a Presto team?
* What's the on call and incident response process like, given the 99.999% reliability bar?

## How to talk about your background
Lean into:
* 2+ years of production backend experience already (many candidates in these threads are freshers/interns), Redis caching at scale, and a measurable 90% manual effort reduction — concrete, quantifiable impact plays well against candidates with only academic projects
* Full stack range (Django/Flask/FastAPI + Next.js/React) shows you can operate across the SDK and backend centers of excellence they describe in the JD
* Frame the FP gap as intentional preparation, not surprise: "I looked into Presto and your FP-first backend before applying, and I've started building basic fluency in Haskell/PureScript."
