# KIP0 Definition of the Keeper Improvement Proposal
```
id: KIP0
title: Definition of the Keeper Improvement Proposal 
author: hazard <hazard@keeperdao.com>
type: standard
status: draft
created: 2020-09-02
requires: none
replaces: none
replaced-by: none
```
## Preamble
### Proposal

Adopt the following standards defining the Keeper Improvement Proposal (KIP) and associated governance processes. 

### Background

This document both defines and is an example of the KIP - a standard document for all governance actions taken by KeeperDAO. An accessible governance process requires clear, consistent standards for how changes are proposed, and how consensus on those proposals is reached. Providing these things is the goal of this document.

The KIP format builds on the Ethereum Improvement Proposal of the Ethereum Foundation, the Maker Improvement Proposal of MakerDAO, as well as practices from the IETF and W3C. Additional information on the consensus procedure can be found in the Beigepaper.

### References
None


## KIP0a Definitions

* **KIP** A Keeper Improvement Proposal, or KIP, is the standard document for all governance actions.

* **Governance token**  The ERC-20 smart contract [0xfa5047c9c78b8877af97bdcb85db743fd7313d4a](https://etherscan.io/address/0xfa5047c9c78b8877af97bdcb85db743fd7313d4a) (ticker: ROOK) on the Ethereum blockchain.
 
* **General public** Members of the general public are defined to be persons who are not members of the DAO.
 
* **Tokenholders** Members of the DAO are cryptographic keys which control any non-zero amount of the governance token.
 
* **Sophon** Sophons are persons with specific expertise that act as governance facilitators and advisors. See [KIP0d].
 
* **Public discussion channel** A service, freely accessible to members and non-members of the DAO, that allows discussion to take place in real-time.
 
* **Public governance forum** An internet forum, freely accessible to all members and non-members of the DAO, that allows discussion to take place in organized, semi-permanent topics. 
 
* **Permanent governance repository** A version-controlled repository containing all KIPs, KIP templates, and supporting material submitted by authors as part of the governance process.


## KIP0b Proposals

### KIP0b1 Proposal style

A KIP must be formatted in [Markdown](https://en.wikipedia.org/wiki/Markdown) following the template available at [proposal-template.md](https://github.com/keeperdao/kip/KIP0/templates/proposal-template.md). It should completely describe a single idea in plain language. Where appropriate, the keywords *must*, *must not*, *should*, *should not*, and *may*, as defined in [RFC2119](https://www.ietf.org/rfc/rfc2119.txt), should be used.

The content of the proposal must meet the following minimum standards:
- **Soundness** It should make technical sense.
- **Accuracy** It should contain true statements and motivations.
- **Well-formed-ness** It should follow the conventions of grammar, spelling, and the KIP guidelines themselves.

Heading titles should only capitalize the first letter of the first word, except where capital letters canonically appear, for example the abbreviation "DAO".

### KIP0b2 Proposal identifiers

A KIP must be assigned an id which allows it to be uniquely referenced. The format of the id is given by the following naming conventions:

- **Regular proposals** must follow the naming convention `KIPAbC`, where `A` is 
the proposal number, `b` is the section letter, and `C` is the subsection number. 

- **Subproposals** must follow the naming convention `KIPAbC-SPDeF`, where `A` is the proposal number, `b` is the section letter, `C` is the subsection number, `D` is the subproposal number, `e` is the subproposal section letter, and `F` is the subproposal subsection number.

In either case, the following additional rules apply:
- String literals `KIP` and `SP` must be in uppercase. 
- Section letters must be in lowercase. 
- Proposal, subproposal, and subsection numbers count up sequentially from 1, except for the proposal number of KIP0.


### KIP0b3 Proposal header fields

The header contains metadata formatted in [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style, preceded and followed by three backticks ( ``` ). The header fields must appear in the following order. All fields are required, however some may take the value "none" where appropriate, as noted below.

- `id` The unique proposal identifier (see [KIP0b2]).

- `title` Proposal title. Titles should be a few words, less than a complete sentence.

- `author` Comma-separated list of names and email addresses of the proposal authors. List items must be formatted "Random J. User \<email-address\>".

- `type` See [KIP0b4].

- `status` See [KIP0b5].

- `created` Date of proposal creation. Must be formatted as [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) (yyyy-mm-dd) timestamp. 

- `requires` Comma-separated list of proposals which are required by the current proposal. Can be "none".

- `replaces` Comma-separated list of proposals which this proposal replaces. Can be "none".

- `replaced-by` Comma-separated list of proposals which replace this proposal. Can be "none".


### KIP0b4 Proposal types

* **General** Used for operational decisions, resource allocation, and matters that mostly affect the DAO's internal stakeholders, along with the parties named in the proposal.

* **Technical** Used for propsals that impact all integrated systems. New smart contracts, APIs, algorithms, and technical conventions fall under this type.

* **Meta** Used for proposals about the proposal process itself, or defining a subproposal process. 


### KIP0b5 Proposal statuses

* **Pre-Draft** The proposal is a work in progress available for public comment, but has not yet been entered into the permanent governance repository.

* **Draft** The proposal has received public comment and been entered into the permanent governance repository.

* **Last-Call** The proposal has received Sophon review and recommendation. It is ready for final evaluation by DAO tokenholders.

* **Accepted** The proposal has been ratified by tokenholders and is now finalized. It represents part of the current policy of the DAO, unless or until it has been replaced (see [KIP0e1]).

* **Rejected**

* **Deferred**

* **Withdrawn** The proposal has been withdrawn by the author, or as the result of inactivity for an extended period of time.


### KIP0b6 Proposal licensing

Unless otherwise specified, the content of a KIP becomes public domain on creation, and is licensed with [CC0](https://creativecommons.org/publicdomain/zero/1.0/).


## KIP0c Proposal Lifecycle 

### KIP0c1 Creation

Before posting the proposal, the author may discuss the concept in the public communication channel, or open a thread in the public governance forum.

To post a proposal, the proposal author must carry out the following steps: 

1. Write the text of the proposal following the guidelines in [KIP0].
2. Assign the proposal a status of `pre-draft` (see [KIP0b5]).
3. Post the proposal on the public governance forum.

### KIP0c2 Pre-draft public comment period

During the public comment period, the author should work with forum-goers to obtain rough consensus on the proposal. This should include making revisions or adjustments in response to feedback.

* Default pre-draft feedback period: 1 week

It is the responsibility of the author to obtain rough consensus, and ultimately the choice of when to move to the next stage is in their hands. However, attempting to fast-track unpopular or unsettled matters will only increase the chances that the matter will be rejected by Sophon reviewers, or objected to during the Tokenholder objection vote.

### KIP0c3 Pre-draft to Draft

To transition a proposal status from `pre-draft` to `draft`, the following steps are carried out:

1. The author must submit the complete proposal text as a pull request to the permanent governance repository. 
2. A Sophon must examine the pull request to determine whether the proposal meets the guidelines laid out in [KIP0]. The Sophon must provide specific feedback to allow the author to revise the pull request if necessary.
3. The author must respond to all feedback from the Sophon, either by correcting the issues in the pull request, or giving an explanation.
5. A Sophon must assign the proposal a status of `draft`.
6. A Sophon must merge the pull request into the permanent governance repository.

### KIP0c4 Sophon review period

Once the proposal has reached "Draft" status, it will be reviewed in detail by Sophons, and receive attention from at least one who is a subject matter expert related to the content of the proposal. They should strive to complete this work in a reasonably timely manner. See [KIP0d3].

* Maximum draft feedback period target: 1 month

If Sophons have not reviewed and formed a recommendation on a proposal after 1 month, the author should notify them asking for an update. If this happens repeatedly, it may need to be addressed by appropriate governance action.

### KIP0c5 Draft to Last-Call

To transition a proposal status from `draft` to `last-call`, the following steps are carried out:

1. A Sophon must open a pull request that assigns the proposal a status of `last-call`.
2. A Sophon must publish the recommendation in the pull request.
3. A Sophon must merge the pull request into the permanent governance repository.
4. A Sophon must open a objection vote associated to the proposal and recommendation.

### KIP0c6 Objection vote period

The objection vote period allows tokenholders to express their disapproval of the Sophon recommendation, or else abstain. It is a silence procedure, meaning that lack of objection is taken to mean consent. 

* Default objection vote period: 1 week

### KIP0c7 Last-call to Accepted, Rejected, or Deferred

To transition a proposal status from `last-call` to `accepted`, `rejected`, or `deferred`, the following steps are carried out:

1. The objection vote in KIP0c6 must resolve and show insufficient objection to the published recommendation. 
2. A Sophon must open a pull request that assigns the proposal a status of `accepted`, `rejected`, or `deferred`, matching the Sophon recommendation.
3. A Sophon must merge the pull request into the permanent governance repository.

### KIP0c8 Last-call to Draft 

To transition a proposal status from `last-call` to `draft`, the following steps are carried out:

1. The objection vote in KIP0c6 must resolve and show sufficient objection to the published recommendation. 
2. A Sophon must open a pull request that assigns the proposal a status of `draft`.
3. A Sophon must merge the pull request into the permanent governance repository.

### KIP0c9 Resubmission 

A KIP can be resubmitted from Pre-draft to Draft as many times as the author desires. Depending on the circumstances of its rejection, deferral, or objection, it may not have immediate priority for review.

## KIP0d Changes after acceptance 

Major changes should not occur to KIPs with `accepted` status. Instead, a new proposal should be created. Exceptions are given below.

### KIP0d1 Amendment process

KIP0d1 defines the subproposal process for amending a KIP. 

A minor amendment is a change to a KIP that preserves the KIP number. Amendments can be performed as long as the change does not alter the logic of the KIP or its external dependencies. 

All KIP0d1 subproposals must use the template located at [KIP0d1-SP-template.md](https://github.com/keeperdao/kip/KIP0/templates/KIP0d1-SP-template.md).

### KIP0d2 Replacement

A proposal can define one or more replacement targets in the `replaces` field header field (see [KIP0b3]). If the proposal moves to `accepted` status, the replacement target(s) header must be updated to record the KIP that replaced them in their `replaced-by` header field. 

If a KIP is replaced, its dependencies (recorded in the `required` header field) must also appear on the KIP that replaces it.

## KIP0e Sophons 

Sophons are expert members of the DAO who use their long-term focus and technical understanding to "speak for the protocol" by analyzing and publishing recommendations on KIPs that fall into their area of expertise. They work together to generate a shared, public recommendation on proposals, in order to ensure that all proposals have received some level of qualified review, prior to being put before tokenholders.

In addition to areas of subject matter expertise, Sophons should represent the major interest groups in the DAO. This will help the governance function better. At minimum, Contributors, Keepers, and the Community should be represented.

There is no financial incentive attached to being a Sophon. There is no hard limit on the number of Sophons. That is to be regulated by future proposal.

### KIP0e1 Requirements

To serve as a Sophon, an individual must meet the following requirements.

- Must be a member of the DAO, i.e. should hold the governance token.
- Must have a durable identity, whether real or pseudonymous.
- Should have history or relationship with the DAO in some way.
- Should have a stake in the DAO's continued success.

### KIP0e2 Recommendations
Sophons examine proposals in order to publish a non-binding recommendation. The recommendation made by the Sophons should be one of the following three possibilities:

* **Accept** In the opinion of the Sophons, the proposal has merit and could be adopted by the DAO.
* **Reject** In the opinion of the Sophons, the proposal does not have merit and should not be adopted by the DAO.
* **Defer** In the opinion of the Sophons, the proposal has merit, but is either not possible to immediately implement, or conflicts with another matter.

Not all Sophons must participate in the creation of a recommendation, however no Sophon should be excluded. Sophons should reach rough consensus so that a single recommendation is published. 

The manner of creating rough consensus is left undefined. They may conduct a roundtable discussion of the proposal or pursue other means compatible with the working style they develop.

### KIP0e3 Onboarding process 

KIP0e3 defines the subproposal process for onboarding one or more Sophons. 

All KIP0e3 subproposals must use the template located at [KIP0e3-SP-template.md](https://github.com/keeperdao/kip/KIP0/templates/KIP0e3-SP-template.md).

### KIP0e4 Offboarding process 

KIP0e4 defines the subproposal process for offboarding one or more Sophons.

All KIP0e4 subproposals must use the template located at [KIP0e4-SP-template.md](https://github.com/keeperdao/kip/KIP0/templates/KIP0e4-SP-template.md).

