# ScrumGuide
## Discourse Ethos

Take a customer-centric approach when presenting solutions and Ideas. Look at customer profile and based on their pain points present solutions rather than coming up with the most elaborate, most optimal and most modern solutions and then trying to massage them in a way to fit the customer problem.

We take a roundtable approach to our conversation style. We explore ideas together without being focused on a particular outcome; it is more or less an open-ended journey of discovering solutions. Think of the distinction between Dostoevsky and Ayn Rand. You know where Ayn Rand is going to end right from the beginning but with Dostoevsky, you have no idea where that's going to come out and probably neither did he.
> "The usefulness of a pot comes from its emptiness"
> Tao Te Ching, Lao Tzu

There is no need to compete with each other on the number of ideas we present. We are all part of the same team with the same end goal.
> "The best people are like water, which benefits all things and does not compete with them."
> Tao Te Ching, Lao Tzu
When presenting solutions or ideas, the burden of proof is on the presenter to come up with reasoning sound enough, so that other team members agree and reach consensus.

Objections, questions and dissent are highly encouraged because it is the core component of disruptive ideas. No one shuts comments, questions or objections because he or she has a higher rank and no one gets booted out by virtue of grandstanding.

Everyone who participates believes that their audience and their peers are intelligent and highly knowledgeable in their fields, so no one is to shut down questions.

When making objections to proposals/ ideas, the burden of proof lies on the individual that is objecting. Best versions of arguments that run counter to the original idea should get presented because one would like to figure out where he/she is wrong and want to use that objection to improve their proposals or to change it.

Objections and questions need to be answered and explored and not brushed off.

Take all the time that is needed to answer questions and objections.
> "Nature doesn't hurry, yet everything is accomplished"
> Tao Te Ching, Lao Tzu

## Table of Contents

- [Sprints](#sprints)
- [Repository Management](#repository-management)
- [Meetings](#meetings)

## Sprints

### Sprint Frequency

Bi-Weekly

### Sprint management

We use **Kanban** methodology.

- User Stories
- To Do
- Doing
- Delivered
- Accepted

#### Sprint management : User Stories

User stories are short, simple descriptions of a feature told from the perspective of the person who desires the new capability, usually a user or customer of the system.[1]

- Title of the `user story` should be in the following format :
> “As a `<persona>`, I `<[want to]>`, `<[so that]>`.”
- We are aiming at **5 to 15 user stories** per sprint. Create an issue for Each accepted`user story`.
- Once a `user story` is assigned, each team is responsible for that user story for the duration of the sprint.

#### To Do

Approved `tasks` that no one has started working is in `To Do` column

- The presented tasks would get judged by the `scrum master`, and after approval, the tasks are added to the `To Do` column of the board.
- Up until the group in charge starts working on a `task`, it stays in this column.
- Based on the number of `tasks`, The `scrum master` would assign some**pull requests** to get reviewed by each team based on the number of tasks.

#### Doing

`Doing` column holds tasks that team-members are currently working on.

- when the group in charge starts working on a task, the said task would be moved from `To Do` column to this one.  
- It is strongly recommended that each person in the group work on a single, discrete item rather than working on them together.

#### Delivered

`Delivered` column holds a list of tasks that are ready for approval.

- When the task is complete, the team member who was working on a task would push a commit to `internal-review` branch and submit a pull request  and hand it off to the other team member for an internal review.in the commit name, use the following format
 `internal-review : <Team member name> | wip : <Task name>`
 submit a pull request for the issue to `develop` branch.

Pull requests are from `internal-review` to develop branch. Use the following as a guideline for pull requests.

- [ ]  Links to the issue(s) this pull request addresses
- [ ]  Links to any other pull requests in other repositories that this pull request requires.
- [ ]  A description of what this pull request includes.
- [ ]  Lint free, Comments for any public functions
- [ ]  Write tests for all new or modified functionality
- [ ]  Instructions on how to test this pull request
- [ ]  Review request from the team member responsible for acceptance testing

<br><br>

Team members would start reviews at the start of the second week so that the tasks could go under final approval process before the start of the upcoming sprint by `scrum master`.
Below is a basic checklist of items that should get checked during a pull request code review.

- [ ] is the code working and does it address its intended functionality?
- [ ] Do tests exist and do they adequately cover the new or changed behaviour?
- [ ] Is the code being tested by any linter or type checking tools and does it pass?
- [ ] Is there any logging or debugging code that isn't using a library that can get removed?
- [ ] is there any piece of code with duplicate functionality?
- [ ] Is there any part of the code that is commented out?
- [ ] Is all the code easily understood? Is the code adequately commented? Do variable and function names correlate clearly with their function? Is there sufficiently formatted documentation for public and private API methods?

- Issues that don't pass review should be moved by the pull request reviewer back to the `To Do` column.

The reviewer would write a comment on the pull request with the following format.
> `internal-review : <Team member name> | wip : <Task name> | reviewer : <Team Member Name> | Date : <Date and time of rejection>`
> `[Issues why it was rejected]`

- The reviewer would move the pull request and any issues that it satisfies to the `delivered` column when the pull request is approved and The merge the pull request for the issue from `internal-review` branch to `develop` branch. The reviewer team member would write the following comment and other any comments as it is needed.

> `internal-review : <Team member name> | <Task name> | reviewer : <Team Member Name> | Date : <Date and time of aprroval>`

#### Accepted

- The `scrum master` moves the pull request and any issues that it satisfies to the `Accepted column` when the pull request is approved and merges it with `master` branch.
- Issues that don't pass review should be moved by the `scrum master` back to the `To Do` column.

## Repository Management

- The `internal-review` branch contains the latest issues that the teams worked on and prepared before getting the changes reviewed by other team members.
- The `develop` branch contains the tasks that passed internal team review.
- The `master` branch contains the most recent accepted changes. New features are generally developed based on the `master` branch unless they depend on the work done in another branch that has yet to be accepted and merged into `master` branch.

## Meetings

Meetings are expensive; A short 10-minute meeting can lead to an hour or more of lost productivity. It's best to conduct most discussions, especially discussions on technical issues as they come up on Github issues to minimise meetings time.

### General Meeting rules

- [ ] Written agenda:  **No meeting shall proceed without having a written agenda.**
- [ ] Time allocation: `scrum master` would look over time allocation before each meeting based on available time for the meeting and send it to team-members two days before the meeting day.
- [ ]  Meetings must begin on time: You should connect to the meeting conference call 5 minutes before the start time.
- [ ]  Meetings must end on time: our time is precious since many team-members have other commitments. It is the duty of `scrum master` to make sure meetings gets conducted in a disciplined fashion, and they end on time.

### Sprint's first meeting

- [ ] `scrum master`  prepares the agenda and a list of problems to explore and send it to team-members three days before the meeting day.
- [ ]  Each team member must prepare a list of possible `user stories` before the meeting starts based on the **problems** the `scrum master` shared.
- [ ] At meeting start, `scrum master` Records attendees.
- [ ] Each team member presented their list of possible `user stories`.
- [ ] based on the consensus of the group, presented `user stories` gets approved or rejected.
- [ ] the `scrum master` records approved `user stories` and the teams that are in charge of them by creating `issues`.
- [ ] Team members form groups of two and `scrum master` splits and assign `user stories` to each team evenly. It is recommended for group members to shuffle and change so that people get more acquainted and learn about each others strength and weaknesses and form a tighter bond.
- [ ] After getting their user stories from `scrum master`, each team gets off the conference call and have a conference call of their own to break down and compartmentalising that `user story` into discrete quantifiable `tasks`. these one-on-one meetings should take approximately **30 minutes**.
- [ ] After the private conference calls are over, each group joins back the main conference call and present the `tasks` they came up with to `scrum master`. The `scrum master` would either approve or decline those proposals.

### Agenda contents for sprint's first meeting

- [ ] Customer problems to explore
- [ ] Links to any market research or background information on the problems we are going to explore.
- [ ] present relevant pieces of information on solutions that currently exist and the possible issues with those solutions.
- [ ] Links to any relevant previous meeting notes

### Sprint's Second meeting

- these meetings are optional.
- In these meetings, team-members discuss their challenges with the team leader.
- It's recommended for team members to try to solve those challenges amongst themselves first before reaching to team leader. Team-members should post an `issue` with the tag `question`  in the following format:

```
Topic: <name of your topic>
Priority: <low|medium|high>
Description: <a few sentences describing the concern or question>
```

## References

[1] `<https://www.mountaingoatsoftware.com/agile/user-stories>`
