# KIP-0: KeeperDAO Governance Framework
```
id: KIP-0
author: hazard <hazard@keeperdao.com>
type: standard
status: draft
created: 2021-09-02
tags:
```
## Preface 

### Proposal

Adopt the guidelines below that describe a governance process for KeeperDAO.

### Summary

KIP-0 sets up some governance guidelines. Easy to follow guidelines let more people participate in governance, which is what we want. This KIP defines a simple format for writing KeeperDAO improvement proposals (KIPs), and illustrates how a KIP goes from idea to reality, through consensus. Finally, it defines governance helpers called *Sophons* that coordinate the governance process.

### Templates 

- [KIP-0.3.1 Minor amendments](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.3.1-SP-template.md)
- [KIP-0.4.3 Sophon onboarding](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.3-SP-template.md)
- [KIP-0.4.4 Sophon offboarding](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.4-SP-template.md)

## 1 KeeperDAO improvement proposals

### 1.1 Style
Try to write in plain English, because not everyone is a native speaker. Lay it out to look something like this KIP, or use the [KIP template](https://github.com/keeperdao/kip/tree/master/KIP0/templates/proposal-template.md) to help. It doesn't have to be perfect. Governance is about communicating. As long as we can communicate, it's good.

### 1.2 Names and references

We're going to refer to KIPs by name, so it helps to have a naming system. All KIPs get a number (this KIP gets number 0, so it's `KIP-0`). Sections and subsections help divide the KIP into parts. These are numbered too, because it's handy to reference them. The current part is labelled with the number `1.2`. 

We can combine these together to make a full reference to this section, `KIP-0.1.2`, which gives it a unique name among all the other KIPs. We could read this as "KIP 0, section 1, subsection 2". Sounds fancy!

### 1.3 Header fields

A Sophon can add this part for you, don't worry. The header contains a bunch of metadata that we can use to build computer tools that work with KIPs. If you don't know what to write in a field, just write `none`.

* **`name`** The name of the proposal, like "KIP-1337". See [1.2].

* **`author`** A list of author names (or usernames if anonymous), along with e-mail addresses or another way to contact them.

* **`type`** There's two types of proposals. 

    * `standard` Used for proposals that specify something that will last a long time, like this proposal. People might need to build on it or rely on it for a while. These can be changed and stuff.
    * `act` Used for propsals that happen all at once. Once they're done, they're done.

* **`status`** Proposals have a status to let people know if what they are reading is a final thing, or just a draft.

   * `pre-draft` It's not even a draft. This is used for when a proposal is being talked about and revised on a public forum, before it gets submitted as a pull request.
   * `draft` The proposal has been merged into the KIP repository. It will get review and then, if it's good, it can continue.
   * `final` The proposal has gotten a review from Sophons, who recommended what to do with it, and tokenholders did not object. The proposal is now final.

### 1.4 Licensing

Licenses say who owns the content that gets published in a KIP. Authors are free to define whatever license they want, but to make it easy, just use [CC0](https://creativecommons.org/publicdomain/zero/1.0/). This license makes the KIP a part of the public domain, so that everybody owns it.

## 2 Proposal lifecycle

The proposal lifecycle is how a KIP turns from an idea into something that the DAO does or uses. The lifecycle has a little work for everybody -- the author(s), the forum-goers, the Sophons, and the tokenholders.

### 2.1 Making the proposal

If you have an idea, start writing a proposal! You don't have to share it right away, everybody has a different style. It can help to discuss your idea with friends on the Discord or forum, you might find good ideas you can use.

When you're ready, it's time to post the proposal for people to see. Make a new thread in the KIP section of the governance forum, and a new KIP is born.

### 2.2 Getting public feedback on the forum

After posting your KIP, people on the forum and Discord might talk about it, ask you questions, and offer their own ideas or feedback. Harness the power of the hive-mind, and use their feedback to make your KIP even better. Making a KIP doesn't have to be about showing everybody a perfect idea from the start. Try not to think of it as having to "survive" criticism -- it's more like everybody getting together to work on a project. We're all in the same DAO. 

If people don't seem interested in your KIP, maybe they just don't know about it. As the author, you are the champion of your KIP. Get the word out! Ask people for feedback, and make it known you want to hear from them. 

Give things at least a week or so, to allow people to see your KIP. Once everybody is happy, you can move on to the next stage. Just remember, there's no point to trying to fast-track something that seems unpopular or doesn't have agreement.

### 2.3 Submitting a pull request

Once things look good on the forum, submit a pull request to the KIP repository with your final KIP. 

A Sophon will review it and make any corrections that might need to get made, and also add the metadata in the header. They might ask you to make small changes and stuff, then give it the status `draft` and merge your KIP.

### 2.4 Getting review from Sophons

Now that it's a draft, you can't make changes directly like you could on the forum. Your changes are pull requests now, and these get reviewed by Sophons. 

Now it's time for the Sophons to think about your proposal. They'll review it in detail, and talk amongst themselves. They should try to do this before too long, at least within 1 month of when the pull request was merged. 

When they're done, they'll make a public recommendation. They will recommend one of three things:
- **Accept**: the Sophons think the KIP is good and should be adopted by the DAO.
- **Reject**: the Sophons think the KIP is bad and should not be adopted by the DAO. 
- **Defer**: the Sophons think the KIP is good, but should not be adopted by the DAO right now. Maybe later though.

### 2.5 Getting review from tokenholders

Once Sophons have made their recommendation on your KIP, the next thing they will do is set up a Snapshot voting page for your KIP. This lets tokenholders to say if they don't agree with what the Sophons have recommended.

In a way, tokenholders have already had a chance to review your KIP -- back in [2.2], on the forum. What's different now is that the Sophons have looked at it too, and have said what they think. This can help some people make up their minds if they weren't paying attention before.

The vote stays open for 1 week. It's a funny kind of vote -- it asks "do you agree with what the Sophons think about this KIP?", and lets you answer "no", but not "yes". Not voting *is* saying yes -- here, silence is consent.

### 2.6 Finalizing

Once the vote is closed, it's time to decide. If there was enough objection, then the KIP remains a draft. Why? Because we don't know what to do with it! The Sophons said one thing, and the tokenholders said another. We have more work to do.

On the other hand, if there wasn't much objection, then it looks like we have our answer. The KIP is now final. That doesn't mean it got accepted -- it could have been rejected too. Don't worry though, you can always submit more KIPs.

## 3 Change requests 

What about making changes to a KIP? Maybe something was spelled wrong, or a link was broken. That should be caught by the Sophons when they get the draft ready, but maybe not. Or maybe something was just plain missing, and should be added.

Well, you can either make a new KIP, or you can try to modify the old one. Modifying can cause weird things to happen, so you should be careful. But it's definitely possible! It's too useful not to be.

### 3.1 Change request process

KIP-0.3.1 defines a change request process for changing a KIP. Changes can be performed as long as the change isn't too crazy. Use your head. 

Use the template located at [KIP-0.3.1-SP-template.md](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.3.1-SP-template.md) to make the subproposal.

## 4 Sophons 

Sophons are governance helpers. They usually have some kind of expertise in a particular area, like finance, software, or governance, that makes them super useful. Sophons try to "speak for the protocol," rather than their own interests as individuals. They analyze KIPs and make recommendations together so that every KIP has been given some kind of attention before they're put in front of tokenholders for a vote.

You don't get much for being a Sophon. Mostly you get to look at paperwork. But it can be a rewarding way to experience the DAO.

### 4.1 Onboarding process 

KIP-0.4.1 defines a subproposal process for onboarding one or more Sophons. 

Use the template located at [KIP-0.4.1-SP-template.md](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.1-SP-template.md).

### 4.2 Offboarding process 

KIP-0.4.2 defines a process for offboarding one or more Sophons.

Use the template located at [KIP-0.4.2-SP-template.md](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.2-SP-template.md).

