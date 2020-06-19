# Inplementing Devops In The Real World

[Pluralsight course](https://app.pluralsight.com/library/courses/8af477a5-c4a3-420d-8d5b-19517a5b1e4f/table-of-contents)

## Why Devops Matters

- 200x more frequent software deployments
- 24x faster recovery from failure
- 3x lower change failure rate
- 22x less time on unplanned work

**Core Values**
- Trust (but verify)
- Empowerment
- Accountability
- Continuous Improvement (iterative)
- Data-driven Decisions
- Customer Empathy

An environment is designed for throughput, allowing for everything to keep moving through the pipeline more efficiently.

This can often require changes in the company's philosophy, the team layouts, and the tools used in the workplace.

**Objections to Devops**
- "we have a QA team, we already do this" - This isn't a devops approach, and instead requires a complete restructuring in that case.
- "this doesn't scale to our company" - This is wrong, this can always work, and has for some pretty large companies already.
- "We don't have the tech skills that startups do"
- "Our executives don't think IT has value" - This sounds about right, as executives generally don't see the value in a restructuring of this scale, and the mindset stems from a lack of trust in the IT department.

** Further Reading**
- The Pheonix Project
- Devops Handbook
- Starting and Scaling Devops in the Enterprise
- Lean Enterprise

These books are less traditional, but still apparently worth a read:

- The Goal
- Team of Teams
- American Icon
- Creativity Inc.
- Designing Delivery

### Standup

A regular meeting where you go through your progress and blockers on each task, allowing for each team to sync up too.

Allows for transparency, throughput of projects, and a focus on the final delivery. 

These meetings can draw attention to important information, and will orient everyone towards most important. Blockers are also tackled, helping each other out on the team.

- Keep it brief
- Keep a shared calendar with milestones
- Dont' force everyone to talk
- Set an example to show that asking for help is OK

### On-call rotation

Individuals are rotated through this role, developing their empathy and focus on the customer is present.

- Puts the focus on the customer/service
- Encourages code documentation and improvement
- Helps other team members stay focused
- Record of experiences to help the team

Make sure it's easy to see who's on call for each team.
Also make sure executives are includes, so that they remain aware of what everyone is working on.

### Sprints

Helps to maintain the backlog of work, as well as the work that each team member is working on. 

There's always a retrospective of the previous sprint, figuring out what worked and what didnt, and how to update.

The team should decide how many backlog tasks can be completed in a sprint.

Don't change the scope of the sprint to make sure that quality of work is consistent.

The timeframe of a sprint should constantly shrink down, so that the team become more efficient.

- Designate a product owner to take charge
- Begin with month-long sprints and shorten them as you go
- Don't use planning sessions to design software
- If you add work to the sprint, subtract other work
- Change process regularly to improve

### Triage new feature request

Review new feedback and feature requests from the client, reviewed by the whole team.

This is part of the devops process beacuse of continuous improvement and a focus on the customer.

- Review all software requests
- Cross-functional participation, how much feedback or use does a feature get
- Immediatly adjust the backlog - what's more or less important, what new stories are there?

Mention new features AND bugs in meetings
Support team should attend, and be able to give their feedback from clients.
The majority of requests are either unfeasable or will take too long to implement.
Product Owner should be constantly filling in new items and archiving old items.

### Merging code with master branch

Never work on the Master branch - that should always be able to show to the client, always fully functional. 

Due to this, any code should be written in a small batch in offshoot branches.

Make sure to continuously test the branched code to make sure it functions completely before it's pushed to master. 
This allows for faster feedback and reduces bug fixing time later on.
This also leads to less "new" code to test for bugs, saving time.

Visual indicators to the build status is vital, and can help the entire team know that something has broken. 

Avoid having any branch around for too long. The more work has been done on a single branch, the more bugs it's likely to create, and the harder it is to integrate later on.

Make working code a forcing function - that's always the end goal.

### Pair on Infrastructure

New infrastrucutre features may be required for your apps. In this case, you might pair up with another engineer to create the servers you need. 

This is useful for crosstraining, as devops can know just enough to be dangerous in this case.

"Generalists with specialties" or t-shaped engineers are the most likely type of engineers you've hired.
People will have different skills and knowledge.

All config details need to be held in source control, making sure the information is written down somewhere.

Test rigorously where the hardware actually is to make sure that things actually work.

- Make your work visible, make sure everyone can see what you're working on, with backlogs and stories.
- Pair ops with dev/engineers to combine groups and information
- Test infrastructure just like software, with TDD etc, to make sure that everything is functional.

### Detect Service Interruption

Telemetry tools are vital, and keeping them upfront and visible are important.

Figuring out where the exact issue is makes you a better devops, instead of just rebooting a server.

Communication is Key, and it's worth sharing information instead of hiding it.

- Identidy the core metrics that measure availability. 
- Add technology that allows for inside-out and outside-in testing
- Make metric dashboards visible and act proactive on them, keep them around the office etc.
- Have a unified way to communicate the status of the servers.

### Send status updates to executives

Make sure clients and team managers are aware of statuses. 

Devops is a cultural change, and not everyone will understand what's going on. It's vital that people understand what and why you're changing things in the office

Show core business metrics to other teams around the office. This can often spread the idea of DevOps, and can benefit the rest of the office. 

Build momentums through demonstrated progress - however do so carefully. This can cause stress or turmoil in the workplace due to the small, regular releases.

- CHoose core metrics to share, don't share everything
- Maintain a regular rhythm
- show good and bad news - it'll build up trust

### Onboarding New Engineers

There will always be a core team, but there could also be new engineers joining and leaving the team to learn how to use DevOps and increasing the use of the mindset.

A company should never be tribal. Information is always shared among a company. Learn from Source Control, Deployment, Pipeline and internal wikis

This is a good time to test a new deployment pipeline

Working together in pairs can accellerate their preparation, as both partners can teach and learn from each other.

- New team members pair with existing ones
- Encourage use of the application itself
- Add new engineers to on-call rotation
- Iterate on-boarding documents on feedback

### Monthly Op Reviews

 