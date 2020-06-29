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

**Further Reading**
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

How long does it take them to be productive to the company. They need to have access to source control, internal wikis etc, to understand the tool and be able to play around with private websites.

### Monthly Operations reviews

These are usually aimed at team leaders and executives. THis allows for an enhanced customer focus - what does this add for the customers and how can you increase accountability.

Keep the focus on the customer metrics - make sure that what you're doing helps the customer more. 
Make sure not to forget the core concept of the product.
	IE - if you work for Netflix, don't stop videos from playing.

Leverage the collective knowledge so that everyone in the meeting can learn from each other to know how to improve their product.

Improve situational awareness for executives - what's going on, budgetary decisions etc.

Eecutives can share core business metrics/beliefs too.

This isn't a problem solving session. These meetings need to be short, and keep everyone in the loop of what's going on.

- Ensure each team defines their own success.
- Keep these meetings very regular - monthly is recommended, but it could be bi-weekly, or quarterly.
- Lead by example and mention challenges. Keep people in the loop, even if there are negative things that need saying, like issues with the product. 
- Actively follow up with problem areas - make sure that things are kept up to date and kept relevant. Follow up on the issues to get them resolved.

### Conduct Incident Retrospectives/Post Mortems

This is mostly aimed at on-call engineers, stakeholders, those that are involved, and is useful for continuous improvement and transparency throughout the company.

DO NOT SIGN BLAME - this is about fixing the issue.

Assemble a timeline of what went wrong, to see how things can be fixed easier next time. Also try and note these as things go down

Don't change what happened. Tell it like it was, not making it sound better than it was.

Explain what worked and what didn't - even minor things. This is about continuously learning, so try to learn from what happened, don't assign the blame.

Develop an action plan to make sure that this doesn't happen again, and assign tasks so that errors don't flag up again.

Keep this record as public as you can - make sure people can see this within the company, if not on a public blog, so that customers can see. 

- Set up the rerospective the day after the next incident
- Choose a method of collecting feedback. Don't use email. Make sure people can interact with live
- Define very crisp and actionable reactive items. Don't say tihngs like "Don't be stupid"
- Assign someone to keep and share minutes. These notes could easily be forgotten


### Collaboration across teams
Each team can be fairly independant, so keeping collaboration open is going to be important to remove bottlenecks and speed up the company.

No team should be entirely independant. They could be relying on each other's tasks, or they share certain tools etc. 

Think locally, act globally - whatever you do to benefit your team, should also benefit other teams. 

Create systems for quick collabooration and decision making. Try to decrease the number of meetings - things like MS Teams or wipeboards. Emails also tend to get involved. 

- Invest in chat room technology.
- Foster cross-team collaboration and communication. You never know when you could pick up a good idea from somewhere.
- Certain things should be standard across the company, such as code repos and programming languages. Make sure that communication tooks are the same too.

### Replacing Team Process

If something is taking too slow internally, it will need to be iterated and improved. This is down to the team leaders, but could also involve the team members and keep the flow moving.

It's hard to improve what you aren't measuring, so keep data on recovery from issues. 

Act on broken processes, or things that don't work. Make something easier to do, not harder.

Automation is often but not always needed. Sometimes you need communcation, or more training, or get someone specific to take ownership of the role. This will improve consistency and accountability.

Experiment and measure. Try new things and test them to see if they work. 

- Solicit feedback from the whole team - make sure they're happy with the changes.
- Listen to others to know when to stop at "good enough" - when do you need to move on.
- Only buy products/services that come with APIs so that you can automate and improve them
- Sell your improvements to other teams - teach them what you've done and share that information.

### Write Documentations and a Knowledge Base

This involves keeping documentation up to date and making sure it's easy to read and share with others. This role usually goes to the developers and the application team, but may be performed by others.

Faster delivery needs more frequent explanations. You may need to teach more often to the customers, or consider slowing down the iterative process here.

Documentation content needs to be easy to create, edit and find.

A changelog is vital, as well as broadcasting this to the customer.

- Set up an open content system that anyone can contribute to
- Make sure there's someone in charge of owning and checking the tool or curating the content
- Define a light review process so that incorrect information isn't broadcast


### Upgrade Deployment Pipeline
Upgrade the pipeline to keep it secure, up to date, and efficient.

Over time, a deployment pipeline will grow into a record of the history of the project. 

Start with simple CI/CD attempts, and build on it over time. Perhaps you partner with teams like Information Security and work alongside them.

Over time, cross-functional skills will come in useful, and you can expand your own personal toolbox of skills this way.

- Do value stream mapping and see where the bottlenecks are to help find points of improvement
- Test changes in non-prod environments, regularly and safely.
- Use of create APIs so that each tool you use can integrate together.


### Right-size Team Roster
Keep the teams at the right size, move the people around from team to team so that everyone is busy and useful at all times.

This is up to the executives, and also the team leaders, who know who they do and don't need at a specific time. 

This keeps the company adaptable and fluid, which makes things cheaper. Making business-based decisions like that also looks good to the stakeholders, who can see that the company funds are being used efficiently.

 Engineer teams may swell before a big release, and then contract after that, as more people are needed for a smaller period of time. 

 Try to make sure that certain skills are in all teams at all times, such as security or flexibility etc.

 - Create a culture of rotating oppertunities. Allow for cross-training individuals and spreading your resources around where needed.
 - Use data to make decisions. 
 - Avoid over-adjusting. If this is too rapid, productivity will go down.
 - Define standards so that engineers can on-board to new teams as fast as possible.


### Packaging Code for Release
This is primarily the role of the on-call engineers, and is done near the end of the week. You need to try and keep this ready to go to production usually. 

The package is a result of a successful CI/CD pipeline. However, there are multiple ways to package up a application.

Packages need to include all pieces needed to deploy - code, images, loading scripts, testing components etc.

Ensure that the package can be recreated. Don't pack it all manually - automate everything. This can lead to errors or missteps. 

- Document the current process to find non-automated steps.
- Consider investing in a package repository tool
- Only use containers as an output of CI, not an input.

### Deploy to Prod

This is the last part of the pipeline, but shouldn't be done on a friday. This should be done so often that it's just boring to the teams.

Use multiple techniques to minimise downtime. - have two environments on the go at once, only one is live, so that if something breaks, you have something ready to go instantly.

Also possible to use A/B release, to roll the new features out to a certain region or group of users.

Use telemetry to measure the positive and negative impact of the releases, both for technical and for clients opinions.

- Try automated deployments with individual services before moving to entire systems
- Blue/green deployment may be the easiest way to start
- closely watch system and business metrics

### Team Lunches

These are mostly for teambuilding and getting everyone involved. Get people talking, bring them together, built trust together.

These connections are important, especially during a time of crisis. Everyone needs to be clear on who is good at taking charge, or handling themselves in a crisis etc. 

Meetups should be planned by a team, but executives too. 

- Buy lunch for the team, keep some budget aside
- For meetings, use video conferencing when you can't meet face to face.
- Dont force the group socialisation, but encourage 1:1 oppertunities too.

### Cross training

This allows teams to swap skills and keep each other up to date of whats going on and what may or may not be needed at a later stage.

Show and tell to educate and demonstrate. Encourage questions so that people can talk about their work. 

