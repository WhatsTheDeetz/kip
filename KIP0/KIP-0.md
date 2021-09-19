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

Adopt the following standards defining the KeeperDAO Improvement Proposal (KIP) and associated governance processes. 

### Background

This document both defines and is an example of the KIP - a standard document for all governance actions taken by KeeperDAO. An accessible governance process requires clear, consistent standards for how changes are proposed, and how consensus on those proposals is reached. Providing these things is the goal of this document.

The KIP format builds on the Ethereum Improvement Proposal of the Ethereum Foundation, the Maker Improvement Proposal of MakerDAO, as well as practices from the IETF and W3C. Additional information on the consensus procedure can be found in the Beigepaper.

### Templates 

- [KIP-0.3.1 Minor amendments](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.3.1-SP-template.md)
- [KIP-0.4.3 Sophon onboarding](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.3-SP-template.md)
- [KIP-0.4.4 Sophon offboarding](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.4-SP-template.md)

## 1 KeeperDAO improvement proposals

### 1.1 Style
A KIP must be formatted in [Markdown](https://en.wikipedia.org/wiki/Markdown) following the template available at [proposal-template.md](https://github.com/keeperdao/kip/blob/master/KIP0/templates/proposal-template.md). It should completely describe a single idea in plain language. Where appropriate, the keywords *must*, *must not*, *should*, *should not*, and *may*, as defined in [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt), should be used.

The content of the proposal must be sound (make technical sense, accurate (contain true statements and motivations), and well-formed (follow the conventions of grammar, spelling, and the KIP guidelines).

References to headings within the same KIP should use `[a.b]`, where `a` is the section number, and `b` is the subsection number. References to headings in a different KIP must use `[KIP-a.b.c]`, where `a` is the KIP number, `b` is the section number, and `c` is the subsection number.

Headings below the subsection level should not be numbered. Headings should only capitalize the first letter of the first word, except where appropriate, for example the abbreviation "DAO". Heading numbers should be followed by a single space, not a period or any other punctuation.

### 1.2 Identifiers and references

Regular proposals must follow the naming convention `KIP-a.b.c`, where `a` is the proposal number, `b` is the section number, and `c` is the subsection number. 

Subproposals must follow the naming convention `KIP-a.b.c-SP-x.y.z`, where `a` is the proposal number, `b` is the section number, `c` is the subsection number, `x` is the subproposal number, `y` is the subproposal section number, and `z` is the subproposal subsection number. 

**Examples**
- `KIP-55.1.2` would be read "KIP 55, section 1, subsection 2".
- `KIP-55.1.2-SP-7.8.9` would be read "KIP 55, section 1, subsection 2, subproposal 7, section 8, subsection 9".


### 1.3 Header fields

The header contains metadata formatted in [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style, preceded and followed by three backticks ( ``` ). The header fields must appear in the following order. All fields are required, however some may take the value "none" where appropriate, as noted below.

* **`id`** The unique proposal identifier [1.2].

* **`author`** Comma-separated list of names and email addresses of the proposal authors. List items must be formatted "Random J. User \<email-address\>".

* **`type`** The type of the proposal, one of: 

    * `standard` Used for operational decisions, resource allocation, and matters that mostly affect the DAO's internal stakeholders, along with the parties named in the proposal.
    * `act` Used for propsals that impact all integrated systems. New smart contracts, APIs, algorithms, and technical conventions fall under this type.

* **`status`** The status of the proposal, one of:

   * `pre-draft` The proposal is a work in progress available for public comment, but has not yet been entered into the permanent governance repository.
   * `draft` The proposal has received public comment and been entered into the permanent governance repository.
   * `final` The proposal has received a Sophon recommendation of "Accept", or "Reject", (see 4.2), and tokenholders did not object. 

### 1.4 Licensing

Unless otherwise specified, the content of a KIP becomes public domain on creation, and is licensed with [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

## 2 Proposal lifecycle

### 2.1 Submission

**Pre-submission**  
Before posting the proposal, the author may discuss the concept in the public communication channel, or open a thread in the public governance forum.

**Submitting**  
To post a proposal, the proposal author must carry out the following steps: 

1. Write the text of the proposal following the guidelines in [KIP-0].
2. Assign the proposal a status of `pre-draft` (see [1.3]).
3. Post the proposal on the public governance forum.

### 2.2 Crowd consensus

**General public comment period**  
During the public comment period, the author should work with forum-goers to obtain rough consensus on the proposal. This should include making revisions or adjustments in response to feedback.

* Default pre-draft feedback period: 1 week

It is the responsibility of the author to obtain rough consensus, and ultimately the choice of when to move to the next stage is in their hands. However, attempting to fast-track unpopular or unsettled matters will only increase the chances that the matter will be rejected by Sophon reviewers, or objected to during the Tokenholder objection vote.

**Status change: pre-draft to draft**  
To transition a proposal status from `pre-draft` to `draft`, the following steps are carried out:

1. The author must submit the complete proposal text as a pull request to the permanent governance repository. 
2. A Sophon must examine the pull request to determine whether the proposal meets the guidelines laid out in [0.1]. The Sophon must provide specific feedback to allow the author to revise the pull request if necessary.
3. The author must respond to all feedback from the Sophon, either by correcting the issues in the pull request, or giving an explanation.
5. A Sophon must assign the proposal a status of `draft`.
6. A Sophon must merge the pull request into the permanent governance repository.

### 2.3 Sophon consensus

**Sophon review period**  
Once the proposal has reached "Draft" status, it will be reviewed in detail by Sophons, and receive attention from at least one who is a subject matter expert related to the content of the proposal. They should strive to complete this work in a reasonably timely manner.

* Maximum duration: 1 month

If Sophons have not reviewed and formed a recommendation on a proposal after 1 month, the author should notify them asking for an update. If this happens repeatedly, it may need to be addressed by appropriate governance action.

### 2.4 Tokenholder consensus

**Tokenholder review and objection period**  
The objection vote period allows tokenholders to express their disapproval of the Sophon recommendation, or else abstain. It is a silence procedure, meaning that lack of objection is taken to mean consent. 

* Default duration: 1 week

**Status change: draft to final**  
To transition a proposal status from `draft` to `final`, the following steps are carried out:

1. A Sophon must publish the recommendation (see 4.2).
2. A Sophon must open a objection vote associated to the proposal and recommendation.
3. The objection vote must resolve 
   * If the vote result shows insufficient objection to the published recommendation, then:
      1. A Sophon must open a pull request that assigns the proposal a status of `final`.
      2. A Sophon must merge the pull request into the permanent governance repository.
   * If the vote result shows sufficient objection to the published recommendation, then:
      1. The proposal remains a draft.

### 2.5 Resubmission 

A KIP can be resubmitted from `pre-draft` to `draft` as many times as the author desires. Depending on the circumstances of its rejection, deferral, or objection, it may not have immediate priority for review.

## 3 Change requests 

Major changes should not occur to KIPs with `final` status. Instead, a new proposal should be created. A major change is defined as a change which breaks references or otherwise results in backwards incompatibility. 

Minor changes, defined as changes which either add new content or adjust existing content for formatting or correctness, without resulting in backwards incompatibility, are permitted via a change request process.

### 3.1 Amendment process

KIP-0.3.1 defines the subproposal process for amending a KIP. 

An amendment is a change to a KIP that preserves the KIP number. Amendments can be performed as long as the change does not alter the logic of the KIP or its external dependencies. 

All KIP-0.3.1 subproposals must use the template located at [KIP-0.3.1-SP-template.md](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.3.1-SP-template.md).

## 4 Sophons 

Sophons are expert members of the DAO who use their long-term focus and technical understanding to "speak for the protocol" by analyzing and publishing recommendations on KIPs that fall into their area of expertise. They work together to generate a shared, public recommendation on proposals, in order to ensure that all proposals have received some level of qualified review, prior to being put before tokenholders.

In addition to areas of subject matter expertise, Sophons should represent the major interest groups in the DAO. This will help the governance function better. At minimum, Contributors, Keepers, and the Community should be represented.

There is no financial incentive attached to being a Sophon. There is no hard limit on the number of Sophons. That is to be regulated by future proposal.

### 4.1 Requirements

To serve as a Sophon, an individual must meet the following requirements.

- Must have a durable identity, whether real or pseudonymous.
- Should have history or relationship with the DAO in some way.
- Should have a stake in the DAO's continued success.
- Should have demonstrated expertise in an area of desirable need.

### 4.2 Recommendations
Sophons examine proposals in order to publish a non-binding recommendation. The recommendation made by the Sophons should be one of the following three possibilities:

* **Accept**: in the opinion of the Sophons, the proposal has merit and could be adopted by the DAO.
* **Reject**: in the opinion of the Sophons, the proposal does not have merit and should not be adopted by the DAO.
* **Defer**: in the opinion of the Sophons, the proposal has merit, but is either not possible to immediately implement, or conflicts with another matter.

Not all Sophons must participate in the creation of a recommendation, however no Sophon should be excluded. Sophons should reach rough consensus so that a single recommendation is published. 

The manner of creating rough consensus is left undefined. They may conduct a roundtable discussion of the proposal or pursue other means compatible with the working style they develop.

### 4.3 Onboarding process 

KIP-0.4.3 defines the subproposal process for onboarding one or more Sophons. 

All KIP-0.4.3 subproposals must use the template located at [KIP-0.4.3-SP-template.md](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.3-SP-template.md).

### 4.4 Offboarding process 

KIP-0.4.4 defines the subproposal process for offboarding one or more Sophons.

All KIP-0.4.4 subproposals must use the template located at [KIP-0.4.4-SP-template.md](https://github.com/keeperdao/kip/tree/master/KIP0/templates/KIP-0.4.4-SP-template.md).

