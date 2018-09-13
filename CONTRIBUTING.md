# Contributing to this repository

First of all, thanks for taking the time to read this document and contributing to our codebase.

Please read each section carefully:

## Getting started

The first thing to do before starting to work on your feature would be to have a conversation with the team about it, we may have some pointers or examples that might make your life much easier!

Jump into the `#<your slack channel name here>` channel and give us a shout, or come around the Web area and have the conversation face to face!

The other thing you will need before you start is a [Jira ticket](https://asosmobile.atlassian.net/browse/WD) describing what it is that you're set to do, or if its a bug make sure there are clear reproduction steps on the description.

If your team doesn't have access or doesn't use Jira, we'll create the ticket for you.

Things to talk about in our first conversation:

* Planned implementation
* Feature toggle approach
* Test plan
* Q&A

## Working on your feature

### Branching

On this project we follow mainline development (or trunk based development), and our default branch is `develop`.

Therefore you need to branch from `develop` and merge into `develop`.

**Please refrain from rebasing**

We use the following convention for branch names `feature/WD-XXXX-short-description`, where `WD-XXXX` is the Jira ticket number, short description is to have an idea what the branch is about and the `feature` part is for features, but it can vary on other kinds of tickets.

Here are some examples:

* `feature/WD-1234-new-icon` , a new feature
* `fix/WD-2345-ios11-bug` , a bug fix
* `task/WD-5677-add-price` , a task inside a feature
* `chore/WD-7899-upgrade-react` , a chore is something that doesn't add functionality to the user but needs to be done

### Coding style

Generally try to match the style and conventions of the code around your changes. Ultimately we want code that is clear, concise, consistent and easy to read.

Broadly we're in-tune with the following style guides:

* JavaScript
    * https://github.com/prettier/prettier
    * https://github.com/airbnb/javascript
* React
    * https://github.com/airbnb/javascript/tree/master/react
* CSS
    * https://github.com/airbnb/css

### Feature toggles

The preferred approach for new features is to wrap them in a feature toggle instead of making the changes directly. This is evaluated on a case by case basis, we probably would have talked about this in our initial discussion.

For more details on how feature toggles work and how to use them, please refer to [this document](docs/feature-toggles.md).

### Unit tests

On this project we have and try to maintain a **100% coverage** on our code.

All the tests, coverage and linting are run at build time on our pipeline, so before opening a PR, please run the following command to make sure your branch will pass all the tests:

```
yarn ci
```

## Opening a PR

Once you're confident your branch is ready to review, open a PR against `develop` on this repo.

Please make sure you fill the PR template correctly, stating the Jira ticket, changelog and the checkboxes.

At this point you will need at least one approval from someone in your team before the QA process can start.

After the first PR approval, a QA can begin the testing process. Following the agreed Test Plan your team's QA will test your feature. We can lend a test environment if required.

When your feature has been fully tested, you now need a second approval from our team to make sure everything still makes sense.

You can also have someone on your team review the code as well to have more confidence. The more approvals the better!

## Merging and deploying

When your feature branch/PR has been tested and has two approvals from our team, it is then ready to merge. Please contact the maintainer team to action the merge.

After the merge has happened, the resulting build can be promoted to integrated environments such as PT02.

For deployment to Production, you will have to wait until our next scheduled release (weekly for some teams, adhoc for others).

After the release has happened, if your feature was behind a feature toggle, you can now test it in Production to make sure everything works as expected.

If the feature has been deemed to be working well it can now be activated by default with a Manifest deployment, which can be on demand and reasonably fast.

## Removing toggle and Celebrating

After your feature is live and toggled on by default, it's now time to remove the toggle code (don't expect the maintainer team to do this) and celebrate! 🍻
