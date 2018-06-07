# Asos Standards
Summary of how to setup new repos to work with InnerSource / Maintainer Model. Will also include coding standards etc as they evolve.

## Maintainer Model introduction
Maintainer model is a small scale version of inner source, which is basically open source done internally. The idea behind all three is to improve transparency, participation and collaboration. Ultimately this is all about opening up the code base in a manner that encourages wide interaction in a controlled manner to ensure that quality not only remains good, but improves.

Each application lives in its own repo and that repo has one or more members of a maintainer team. More commonly these individuals are referred to as Committers. They are the custodians of the repo and have the ultimate say about what changes are made to the code base. These changes can come from the committers, but importantly from anyone in Asos who wants to contribute. Such people are known as Contributors and they contribute via Pull Requests.

Pull Requests can be because the repo has a listed bug, a request for enhancement or active feature development underway. A committer might also have an original idea to improve the code or add functionality without it being on a roadmap or bug list. Regardless of the origination of the change, it is crucial that the ground rules are clear and understood around how to contribute and what to expect from committers. Chief amongst this is acceptance that Committers have the final say and are, like everyone else, busy with various things. So, everyone needs to respect timelines and understand that PRs might not be processed immediately.

Prior to any pull request, every effort should be made to get committers and contributors together to discuss the work, agree on the design and align expectations. No one should be surprised to see a PR nor should they be impatient for a merge. Equally, committers should make every effort to be available to discuss potential contributions and to honour any commitments to peer review/pair on the code.

Given the fact some people are in different parts of the building, or in different buildings / working from home, there is a need to be asynchronous about working together through the PR process. Fortunately, Github makes this easy through the PR review mechanism and the options available to protect directories in each repo. For example, each repo will be configured to require at least one and ideally two reviewers against any PR.

Branching
Each repo will have its own branching strategy. Typically this will be either Trunk-Based Development or some variation of Git Flow. Whichever way the repo works, it is important to follow the process rather than use a preferred approach. Have a chat with the Committer/Maintainer team if you feel they could benefit from a different approach, otherwise respect their decision. 

Each repo should have a contributing.md file in the repo that spells out the cadence for the repo. A sample file will be provided to use as a template TODO - add a link to a generic base file. This will detail how to name branches, amongst other things.

Merging
GitHub presets will be used to determine the preferred approach to merging. This may allow rebasing, plain merging or squash merging, or any combination of the three. As with branching, this is a Committer team decision and should be respected. 

The contributing.md file in the repo spells out the cadence for the repo.  This will detail the branching process, test process, release process and the PR process. It will outline what is expected in a good PR, since this becomes central to the process. Please follow the team's cadence and again, if you would like to operate differently, only do so after discussing and agreeing with the team. 

Releasing
TODO

Coding Standards
TODO

