**The Evolution of the Mantid Project**

# 1. Background

The [ISIS facility](https://www.isis.stfc.ac.uk/) started the Mantid project in 2007 and the project has been in active development since then. The project has become a major collaboration between neutron centres since its inception, with [SNS](https://neutrons.ornl.gov/sns), [ESS](https://europeanspallationsource.se/), [ILL](https://www.ill.eu/) and [CSNS](http://english.ihep.cas.cn/csns/) joining the collaboration (in that order). The [Mantid project website](https://www.mantidproject.org/) describes Mantid as providing a framework that supports high-performance computing and visualisation of scientific data.

The Mantid project is at risk of becoming a victim of its own success. Mantid is now the standard for neutron data reduction and yet the current governance has not kept pace with the growth the project has seen. The current Project Management Board (PMB) recognises this and the purpose of this document is to establish a new vision and governance model that fits with current and emerging needs of the facilities, the neutron community and project contributors.

## 1.1. Current governance model

The [governance model for the project](https://github.com/mantidproject/documents/blob/master/Project-Management/PMB/Mantid%20Governance%20Model.doc) was last updated in 2014. There is a project management board (PMB), a technical standards committee (TSC) and a user committee, each entity has a chair, and representatives from each member in the collaboration and regular meetings. There is a single project manager defined as part of the governance model. There are procedures for third party contributions which have been actively used by developers at [FRMII](https://www.frm2.tum.de/en/the-neutron-source/), [SINQ](https://www.psi.ch/en/sinq) and [ANSTO](https://www.ansto.gov.au/), to add code and features for their facilities which are not officially members of the project.

The current model is based on the structure implemented when the project was a single facility entity. The model has not evolved to match the ways of working at the facilities over the last few years. It has become out of step with reality and needs updating.

## 1.2. Current challenges

What Mantid is and what it needs to be has changed over the years. The practice has been to incorporate features from elsewhere into Mantid to make it a "one-stop shop". This has served to increase the complexity. However, an increase in resource across the collaboration to manage this complexity has not been able to be matched. The increased complexity has meant the time it takes for contributors to start committing has increased which has ultimately made it hard for the project to benefit from an ideal wide community of contributors. How do we empower the technical staff to work on the project to modify the software by using their expertise in collaboration with scientists from the broader community?

Each member facility has different scientific specialities, operational challenges and therefore priorities. It naturally follows that each member in the collaboration has a different organisation and strategy for scientific software development. Other facility constraints also necessitate that the software itself is used in different layers of the software stack at each facility and the Mantid "one-size-fits-all" makes it difficult to use only parts of Mantid as components. Not all facilities have the same structure for contributing. Example 1: ISIS has a fairly fixed staffing allocated to Mantid that work on varying aspects of the project. ORNL has a dynamic staffing where even the people contributing to Mantid in a given month changes and they can be brought back out to work on other projects.
How does the will of the facility/budget authority’s influence get factored in? How will they have a say over what is done and “large” decisions (e.g. the move to Mantid workbench).

Mantid is used by a number of facilities now as the default data processing (and analysis) platform and as such it has become or could be considered as mission critical. Changes need to be considered and nuanced enough to fit the domain. It is, as defined in the Mantid new developers pages, everyone’s responsibility not to break the build. We need to build trust; in the developers, in the project managers, and between facility management. The participants, largely, want performant, high quality data reduction software. They do not want functionality that was working to break or be removed. Trust and communication between the participants is the way for the software to grow.

# 2. Going Forwards

## 2.1. Vision

Each member facility wants Mantid to be a stable, high quality, data reduction solution for now and for the foreseeable future.

To achieve this the collaboration acknowledges the current challenges and proposes to address them by building on the recent, natural move of some facilities to embark on "spin-out" projects.

It is not necessary to have a single code base to be part of the Mantid brand. Mantid need to provide performant, high quality, adaptable solutions that scale to meet the emerging scientific requirements of the future.

Mantid will move from being a framework to being an ecosystem of multiple, complementary, interoperable, quality-driven (and verified) software projects for neutron and muon data reduction and front-line data analysis. Collectively these will form an open-source software collection freely available to anyone who wishes to use it as part of their own software developments.

It will be the people that keep the different parts together. Everyone at each member facility has challenges fulfilling the needs of their facility and the wider neutron and muon scientific community. Each member facility acknowledges that the most effective way of meeting local and international needs is by the generous sharing of expertise and a concerted approach to avoid unnecessary duplication of effort.

The Mantid ecosystem will be managed by The Mantid Collaboration. The Collaboration is a dynamic alliance of neutron and muon facilities that allows members to play to their strengths and their current resources to develop the Mantid Ecosystem. Any facility involved in neutron and/or muon research can be a facility member. Any member may initiate a project and each member chooses independently which projects they wish to commit resource to. The Collaboration uses lightweight governance that chooses agreeing and adhering to standards over lots of meetings to ensure projects are interoperable. All members participate based on their contributions and merit. No one individual or organization has any special status or veto.

The unifying theme across the ecosystem will be a commitment to empowering technical contributors and applying the [Agile Manifesto principles](https://agilemanifesto.org/principles.html) to the development of software for working with neutron and muon data.

Mantid will value quality and innovation equally.

## 2.2. Goals

Move from being a framework to being an ecosystem of complementary software projects.

Become the largest open source collection of interoperable scientific software for the neutron and muon community and a brand that is the sum of its parts.

Value and encourage:

- small, quick to compile, and easy to extend components.
- generalisation where it makes sense and specialisation where it makes more sense.
- software that is simple to test, simple to teach and simple to use.

Mantid projects have a responsibility to be both agile and stable for the world class facilities that depend on them.

Mantid projects are to be trusted in production.

# 3. Risks

The Mantid framework is open source and the main code base has a GNU GPL Version 3 license. As best practise has evolved over the years the Mantid project and various partners and contributors have adopted various techniques. It is now timely to review the latest best practice for governance of open source projects.

The current challenges the member facilities face mean that unless we review and agree a new governance model the Mantid project will continue to diverge ad hoc. This will introduce instability in the core as fewer developers commit and review code. In turn this risks facilities not being able to use Mantid confidently in production or remaining on earlier versions that could in time become insecure or even simply stop working on newer operating systems. 

If the Mantid project as a single repository continues the learning curve for new developers will continue to increase and there will be the temptation for developers or member facilities to work on their own "cut down versions" that are easier for them to navigate and extend as they see fit. This brings with it the inevitability of duplication of effort when developers stop discussing common problems and working together on solutions. It would be better to develop these "cut down versions" together so everyone benefits from a slicker codebase.

The challenge for similar projects e.g. SasView has been in ensuring a sufficient core team that can review pull requests and do QA/QC on the contributions. Here modularisation of the code base has helped to firewall core functionality and reduced the risk of large scale breaking of builds.

The risks of modularisation or componentization should not be ignored and the associated governance structure should be stress tested to consider how it would work in some key scenarios before it is adopted.

# 4. Strategy & Risk Mitigation

The collaboration cannot, and does not, plan a “big bang” switch. It is clear that moving to a new way of working will take a lot of careful thought and planning and we all need to continue to support the use of Mantid as-is in production. At a high level there will need to be work on several fronts such as governance, continuing operations and re-architecting Mantid into component parts.

It is proposed that 3 initial online working groups are set up:

- Mantid Open Governance (MOG)
- Mantid Operations as Usual (MOU pronounced "moo")
- Mantid As Components (MAC)

Each member who wishes to influence the outcomes of the working groups should play an active part to ensure the agreed way forward meets their facility's needs.

These working groups will report back to the current PMB with initial outcomes by the end of September. A final submission will be reported back to the current PMB by the end of October for comment by the Mantid Review Panel at the end of 2020.

## 4.1. Mantid Open Governance (MOG) working group

- to draft and get agreement on
  - the governance of the Collaboration and
  - the minimum governance requirements on each project in the ecosystem.

- should use the key requirements (or a good list of needs) found at [opengovernance.dev](https://github.com/opengovernance/opengovernance.dev) and [opensource.guide](https://opensource.guide/leadership-and-governance/) as a starting point.

- should also establish guidelines and practicalities for: 
  - deprecating features / supported platforms 
  - refactoring and redesign of core features 
  - conflicting scientific priorities 
  - conflicting priorities between software quality and features

## 4.2. Mantid Operations as Usual (MOU) working group

- to draft and get agreement on
  - the activities needed to package the last version of Mantid in its single repository format and
  - the outstanding known features that the ecosystem will likely need to deliver in the future

- should ensure that the latest version of Mantid in its single repository format is as robust as is practically possible and there are processes for keeping this current feature set working in production for as long as is needed.

## 4.3. Mantid As Components (MAC) working group

- to draft and get agreement on
  - what constitutes a component and
  - how the last version of Mantid in its single repository format could be separated out into components that can then be reused most effectively and
  - the "core" components and
  - a baseline example project for each facility that reuses the components to deliver the same functionality as the last version of Mantid in its single repository format.

- should learn from other projects e.g. Eclipse, to effectively "componentize" Mantid to achieve the Collaboration's high level goals.

# 5. Governance for the Collaboration

As a starting point for the Mantid Open Governance (MOG) working group some guiding principles and an outline structure is proposed based on current PMB suggestions.

## 5.1. Guiding Principles

The overarching requirement for changing the governance of Mantid it to ensure that the collaboration and development continues to the satisfaction of all of the project stakeholders. The longevity of the Mantid project is impressive, but the continued focus on “Mantid as a project” does not fit with the ongoing nature of the work and the maintenance aspects of running mission-critical software development. Thus the view needs to shift to “Mantid as a collaboration” that is fit for both long-term users of the software and new users.

Mantid serves two inter-connected communities:
- **Neutron and muon scientists** – ensuring the components developed are useful and needed by their scientific facilities and the communities they serve. Ideally, this community should be an open, transparent, inclusive, and diverse community of contributors and experimental end-users that are active and engaged in identifying common and facility-specific areas of scientific interest. The community should make reasonable effort to establish and keep up-to-date scientific roadmaps for all facility members.

- **Developers and software support** – agreeing standards to ensure interoperability between components and ensuring the components developed adhere to those standards. Ideally, this community should be an open, transparent, inclusive, and diverse community of contributors and project committers that are active and engaged in developing scientific software for member facilities. The community should make reasonable effort to empower each other to reduce technical debt and work on projects that matter most to their facility. A facility does not have to be involved in a project unless it wants to be.

Openness to contribution benefits the core of the project and, at a given time, probably increases the number of developers overall. Members and contributors can come and go as specific functionality is required for their needs with a "who pays the piper, calls the tune” and “you break it, you fix it” approach. This has its own issues – specifically with ensuring that the core codebase is maintained and kept stable - but is generally more inclusive to new developers. There is the added advantage that this makes grant funded work, or short-term engagement, feasible and increases the pool of possible developers where long-term commitments aren’t possible.

## 5.2. Structure

What is proposed for the Collaboration governance is a structure that prioritises the development of open source software with strong stakeholder engagement and facility collaboration.

See [Appendix](#Appendix) for diagram.

### 5.2.1. Mantid Collaboration Board

The Collaboration relies on the high-level support of its facility members.
To ensure ongoing commitments from members, there needs to be a forum for those members to:

- discuss provision of resources to maintain the "core" components and development support
- provide formal oversight of the Collaboration and its work
- review the progress of the Collaboration against its goals
- inform each other of local facility management issues

 This board should be comprised of high level (division or director level) managers from member facilities holding budget authority and who are committing resources long-term to the Collaboration.

This board should meet in-frequently – maybe twice yearly.  This could be once in person during the annual user workshop and once via video conference.

The chair of the board is elected with a majority vote for a term of 3 years.

### 5.2.2. Mantid Collaboration Support Team

The Collaboration relies on the development (and other) support resource from facility members to work together to help arrange events and maintain the common resources such as the Mantid website and IT infrastructure including Git code repositories, issue databases, CI servers and configurations, development-oriented mailing lists and newsgroups, download sites and project websites. The team would also be responsible for organising regular online developer meetings and face-to-face developer meetings at least annually.

This team is a distributed team with members agreed by the Mantid Collaboration Board.

This team reports to the Mantid Collaboration Board.

### 5.2.3. Mantid Core Development Committee

The development of Mantid requires a development management committee that operates in a similar manner to management committees of other open source projects i.e. it should be technically based and managed by open discussion with a view to consensus, though with a defined way to make decisions. This group would lead the development and release of "core" Mantid components and be responsible for coordinating the developments across the facilities, defining the areas of common work and benefits, as well as planning and executing the long-term strategic developments (via the core team, see below).

This committee is comprised of technical project managers or team leads from member facilities who have delegated responsibility for allocating effort to various Mantid work. This committee is open to all and all members participate based on their contributions and merit. No one individual or organization has any special status or veto.

This committee should meet regularly - maybe monthly via video conference.

The Mantid Collaboration Board appoints one of the Mantid Core Development Committee members as the chair via majority vote for a term of 3 years.

This committee reports to the Mantid Collaboration Board via the chair.

Each committee member provides its list of technical priorities for the next few release cycles. These priorities should have an emphasis on identifying changes that are motivated by newly available technologies (e.g. C++17), soon to be deprecated technologies (e.g. qt4), and consistency across the software (e.g. design reviews).

The Mantid Scientific Committee provides its list of scientific priorities for the next few release cycles.

This committee then determines the priorities by consensus and schedules the work. A mix of work addressing both technical and scientific priorities is the preferred approach for each release cycle. Part of this is identifying what high priority work multiple members would like done and connecting the facilities to work together on those features. This means that a given facility may work on a lower priority item first with another member rather than their top priority alone.

Taking into consideration the resource available to each committee member, this committee would:

- **Own the Mantid Core Roadmap**

  This involves engaging with stakeholders and coming up with a rolling 3 year plan for cross-facility development across all of the "core" component projects to meet prioritised technical and scientific requirements. This roadmap should include the development and implementation of a maintenance strategy, and consider information security issues and determine solutions.

- **Schedule Core Releases**

  This involves engaging with stakeholders to plan and manage releases

- **Monitor and present progress and plans to the Mantid Collaboration Board**

  This involves managing the development backlog for the Core and implementing a decision-making process that enables efficient progress.

- **Agree technical standards and specifications for interfacing with "core" components**

  Any member can propose a standard or specification but for it to become part of the recognised "core" standards, this committee must review and agree it.

- **Promote and grow the developer and software support community**

  Acting as the point of entry for new developers/contributors this involves being the face of the collaboration, encouraging participation, maintaining development standards of the "core" components and advise Mantid projects on development standards.

### 5.2.4. Mantid Core Development Team

This team executes the long-term strategic developments of the "core" Mantid components. It also manages the "core" Mantid components tech-stack, tech standards, releases, maintenance work and executes the work to ensure the codebase keeps up with its dependencies. It is responsible for self-organising development cycles to align with release cycles.

This team should be in frequent contact to progress development and meets regularly via video conference to self-organise and execute the core developments as determined by the Mantid Core Development Committee. It is important this team does not deal directly with any facility, technique, or instrument specific code. All work undertaken will be directed by the Mantid Core Roadmap.

This team is a distributed team open to all and all members participate based on their contributions and merit. No one individual or organization has any special status or veto. To distribute the expertise, as a minimum, the team includes members from different member facilities as agreed by the Mantid Collaboration Board.

This team reports to and feeds into the Mantid Core Development Committee.

### 5.2.5. Mantid Scientific Committee

The Mantid Scientific Committee ensures that the Collaboration remains scientifically relevant and up to date and continues to meet the growing scientific demands for various technique areas. The committee focuses on the scientific recommendations to the Mantid Core Development Committee for what should be the focus for the work to be done. It is also responsible for collecting and prioritising the needs of the end-users (mostly instrument scientists and facility users) and for also encouraging committee members to take an active role in contributing to non-core Mantid projects ensuring that the ecosystem remains relevant.

The Mantid Scientific Committee brings together representations from neutron and muon user community and facility scientists. Each organisation that contributes to or deploys Mantid should have representation - one or two senior scientists (expert users of Mantid) - on this committee.

 This committee will organise the annual user meeting to give feedback to and get input from the wider community of Mantid users. At such an event a general discussion about scientific computing at neutron sources for current and future scientific needs could be held. The benefit would be a collectively discussed overview that would assist in the definition of scope for Mantid projects and align Mantid projects with existing or future projects that develop against it.  

This committee should meet twice a year. This could be once in person during the annual user workshop and once via video conference.

The Mantid Collaboration Board appoints one of the Mantid Scientific Committee members as the chair via majority vote for a term of 3 years.

This committee reports to the Mantid Collaboration Board and feeds into the Mantid Core Development Committee via the chair.

# 6. Governance for Mantid projects

As a starting point for the Mantid Open Governance (MOG) working group some guiding principles describe the fundamental rules for creating and governing projects in the Collaboration based on current PMB suggestions.

## 6.1. Guiding principles

There are projects that exist under a larger umbrella organisation such as Apache or Eclipse utilising the umbrella organisation’s processes and procedures. There are also projects which exist as single entities such as Matplotlib and SASView. In all cases, such projects have some form of governance. Common aspects of all are rules and process for contributions, and development standards which contributions are expected to follow. Licensing and intellectual property (IP) depends on each project or to which foundation a project belongs.

It would be possible, and it is perhaps beneficial to extend the proposed structure to include projects other than Mantid. There are some examples of domain entities which aim to provide a collective of software projects. An example of this within the SANS community is the canSAS collaboration which has within its remit providing for a repository of orphaned community code. The ORSO collaboration, recently started for reflectometry, is also aiming to provide a home for some common domain-specific software projects.

## 6.2. Project requirements

All Mantid projects (including "core" component projects) are required to:

- Provide a tangible benefit for those who are involved.
- Have a scientific steering committee distinct from any other project that advises on the scientific goal the project has been set up to meet and tests and validates solutions.
- Have a technical steering committee distinct from any other project that empowers developers to develop a solution that meets the scientific goal and identify changes that are motivated by newly available technologies, soon to be deprecated technologies, and consistency across the software projects.
- Promote collaborative open source development.
- Be self-organizing, open, and transparent.
- Have a document describing the purpose, scope, and operational rules for the project.
- Be sized so end-of-service life and extension can be chosen over end-of-life feature deprecation to reduce the effort and costs put into software support and maintenance.
- Communicate their project plans and plans for new features (major and minor) in a timely, open, and transparent manner.
- Use common and, where possible, modern technologies.
- Prioritise software quality and create high-quality components capable of supporting production grade products on top of them.
- Expose well-defined APIs.

# 7. Appendix

## 7.1. Collaboration structure

[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggVERcblx0QVtOZXV0cm9uIGFuZCBtdW9uIHNjaWVudGlzdHMgY29tbXVuaXR5XSAtLT58IGZlZWRzIGludG8gfCBCW01hbnRpZCBTY2llbnRpZmljIENvbW1pdHRlZV1cblx0QSAtLT4gfGNvbnRyaWJ1dGVzIHRvfEgoTWFudGlkIFByb2plY3RzKilcbiAgQiAtLT58ZmVlZHMgaW50b3wgQ1tNYW50aWQgQ29yZSBEZXZlbG9wbWVudCBDb21taXR0ZWVdXG4gIEMgLS0-fCByZXBvcnRzIHRvIHwgRlxuICBEW01hbnRpZCBDb3JlIERldmVsb3BtZW50IFRlYW1dIC0tPnxmZWVkcyBpbnRvICYgcmVwb3J0cyB0byB8Q1xuICBEIC0tPiB8Y29udHJpYnV0ZXMgdG8gfElcbiAgRVtNYW50aWQgQ29sbGFib3JhdGlvbiBTdXBwb3J0IFRlYW1dIC0tPiB8cmVwb3J0cyB0byB8RltNYW50aWQgQ29sbGFib3JhdGlvbiBCb2FyZF1cbiAgR1tEZXZlbG9wZXJzIGFuZCBzb2Z0d2FyZSBzdXBwb3J0IGNvbW11bml0eV0gLS0-IHxjb250cmlidXRlcyB0byB8SShNYW50aWQgQ29yZSBQcm9qZWN0cyopXG4gIEcgLS0-IHwgZmVlZHMgaW50byB8RFxuICBHIC0tPiB8Y29udHJpYnV0ZXMgdG8gfEgiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCIsInRoZW1lVmFyaWFibGVzIjp7ImJhY2tncm91bmQiOiJ3aGl0ZSIsInByaW1hcnlDb2xvciI6IiNFQ0VDRkYiLCJzZWNvbmRhcnlDb2xvciI6IiNmZmZmZGUiLCJ0ZXJ0aWFyeUNvbG9yIjoiaHNsKDgwLCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5Qm9yZGVyQ29sb3IiOiJoc2woMjQwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInNlY29uZGFyeUJvcmRlckNvbG9yIjoiaHNsKDYwLCA2MCUsIDgzLjUyOTQxMTc2NDclKSIsInRlcnRpYXJ5Qm9yZGVyQ29sb3IiOiJoc2woODAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeVRleHRDb2xvciI6IiMxMzEzMDAiLCJzZWNvbmRhcnlUZXh0Q29sb3IiOiIjMDAwMDIxIiwidGVydGlhcnlUZXh0Q29sb3IiOiJyZ2IoOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSkiLCJsaW5lQ29sb3IiOiIjMzMzMzMzIiwidGV4dENvbG9yIjoiIzMzMyIsIm1haW5Ca2ciOiIjRUNFQ0ZGIiwic2Vjb25kQmtnIjoiI2ZmZmZkZSIsImJvcmRlcjEiOiIjOTM3MERCIiwiYm9yZGVyMiI6IiNhYWFhMzMiLCJhcnJvd2hlYWRDb2xvciI6IiMzMzMzMzMiLCJmb250RmFtaWx5IjoiXCJ0cmVidWNoZXQgbXNcIiwgdmVyZGFuYSwgYXJpYWwiLCJmb250U2l6ZSI6IjE2cHgiLCJsYWJlbEJhY2tncm91bmQiOiIjZThlOGU4Iiwibm9kZUJrZyI6IiNFQ0VDRkYiLCJub2RlQm9yZGVyIjoiIzkzNzBEQiIsImNsdXN0ZXJCa2ciOiIjZmZmZmRlIiwiY2x1c3RlckJvcmRlciI6IiNhYWFhMzMiLCJkZWZhdWx0TGlua0NvbG9yIjoiIzMzMzMzMyIsInRpdGxlQ29sb3IiOiIjMzMzIiwiZWRnZUxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJhY3RvckJvcmRlciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImFjdG9yQmtnIjoiI0VDRUNGRiIsImFjdG9yVGV4dENvbG9yIjoiYmxhY2siLCJhY3RvckxpbmVDb2xvciI6ImdyZXkiLCJzaWduYWxDb2xvciI6IiMzMzMiLCJzaWduYWxUZXh0Q29sb3IiOiIjMzMzIiwibGFiZWxCb3hCa2dDb2xvciI6IiNFQ0VDRkYiLCJsYWJlbEJveEJvcmRlckNvbG9yIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwibGFiZWxUZXh0Q29sb3IiOiJibGFjayIsImxvb3BUZXh0Q29sb3IiOiJibGFjayIsIm5vdGVCb3JkZXJDb2xvciI6IiNhYWFhMzMiLCJub3RlQmtnQ29sb3IiOiIjZmZmNWFkIiwibm90ZVRleHRDb2xvciI6ImJsYWNrIiwiYWN0aXZhdGlvbkJvcmRlckNvbG9yIjoiIzY2NiIsImFjdGl2YXRpb25Ca2dDb2xvciI6IiNmNGY0ZjQiLCJzZXF1ZW5jZU51bWJlckNvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IiOiJyZ2JhKDEwMiwgMTAyLCAyNTUsIDAuNDkpIiwiYWx0U2VjdGlvbkJrZ0NvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IyIjoiI2ZmZjQwMCIsInRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJ0YXNrQmtnQ29sb3IiOiIjOGE5MGRkIiwidGFza1RleHRMaWdodENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dERhcmtDb2xvciI6ImJsYWNrIiwidGFza1RleHRPdXRzaWRlQ29sb3IiOiJibGFjayIsInRhc2tUZXh0Q2xpY2thYmxlQ29sb3IiOiIjMDAzMTYzIiwiYWN0aXZlVGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsImFjdGl2ZVRhc2tCa2dDb2xvciI6IiNiZmM3ZmYiLCJncmlkQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JrZ0NvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCb3JkZXJDb2xvciI6ImdyZXkiLCJjcml0Qm9yZGVyQ29sb3IiOiIjZmY4ODg4IiwiY3JpdEJrZ0NvbG9yIjoicmVkIiwidG9kYXlMaW5lQ29sb3IiOiJyZWQiLCJsYWJlbENvbG9yIjoiYmxhY2siLCJlcnJvckJrZ0NvbG9yIjoiIzU1MjIyMiIsImVycm9yVGV4dENvbG9yIjoiIzU1MjIyMiIsImNsYXNzVGV4dCI6IiMxMzEzMDAiLCJmaWxsVHlwZTAiOiIjRUNFQ0ZGIiwiZmlsbFR5cGUxIjoiI2ZmZmZkZSIsImZpbGxUeXBlMiI6ImhzbCgzMDQsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlMyI6ImhzbCgxMjQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNCI6ImhzbCgxNzYsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNSI6ImhzbCgtNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU2IjoiaHNsKDgsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNyI6ImhzbCgxODgsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSJ9fSwidXBkYXRlRWRpdG9yIjpmYWxzZX0)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiZ3JhcGggVERcblx0QVtOZXV0cm9uIGFuZCBtdW9uIHNjaWVudGlzdHMgY29tbXVuaXR5XSAtLT58IGZlZWRzIGludG8gfCBCW01hbnRpZCBTY2llbnRpZmljIENvbW1pdHRlZV1cblx0QSAtLT4gfGNvbnRyaWJ1dGVzIHRvfEgoTWFudGlkIFByb2plY3RzKilcbiAgQiAtLT58ZmVlZHMgaW50b3wgQ1tNYW50aWQgQ29yZSBEZXZlbG9wbWVudCBDb21taXR0ZWVdXG4gIEMgLS0-fCByZXBvcnRzIHRvIHwgRlxuICBEW01hbnRpZCBDb3JlIERldmVsb3BtZW50IFRlYW1dIC0tPnxmZWVkcyBpbnRvICYgcmVwb3J0cyB0byB8Q1xuICBEIC0tPiB8Y29udHJpYnV0ZXMgdG8gfElcbiAgRVtNYW50aWQgQ29sbGFib3JhdGlvbiBTdXBwb3J0IFRlYW1dIC0tPiB8cmVwb3J0cyB0byB8RltNYW50aWQgQ29sbGFib3JhdGlvbiBCb2FyZF1cbiAgR1tEZXZlbG9wZXJzIGFuZCBzb2Z0d2FyZSBzdXBwb3J0IGNvbW11bml0eV0gLS0-IHxjb250cmlidXRlcyB0byB8SShNYW50aWQgQ29yZSBQcm9qZWN0cyopXG4gIEcgLS0-IHwgZmVlZHMgaW50byB8RFxuICBHIC0tPiB8Y29udHJpYnV0ZXMgdG8gfEgiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCIsInRoZW1lVmFyaWFibGVzIjp7ImJhY2tncm91bmQiOiJ3aGl0ZSIsInByaW1hcnlDb2xvciI6IiNFQ0VDRkYiLCJzZWNvbmRhcnlDb2xvciI6IiNmZmZmZGUiLCJ0ZXJ0aWFyeUNvbG9yIjoiaHNsKDgwLCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5Qm9yZGVyQ29sb3IiOiJoc2woMjQwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInNlY29uZGFyeUJvcmRlckNvbG9yIjoiaHNsKDYwLCA2MCUsIDgzLjUyOTQxMTc2NDclKSIsInRlcnRpYXJ5Qm9yZGVyQ29sb3IiOiJoc2woODAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeVRleHRDb2xvciI6IiMxMzEzMDAiLCJzZWNvbmRhcnlUZXh0Q29sb3IiOiIjMDAwMDIxIiwidGVydGlhcnlUZXh0Q29sb3IiOiJyZ2IoOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSkiLCJsaW5lQ29sb3IiOiIjMzMzMzMzIiwidGV4dENvbG9yIjoiIzMzMyIsIm1haW5Ca2ciOiIjRUNFQ0ZGIiwic2Vjb25kQmtnIjoiI2ZmZmZkZSIsImJvcmRlcjEiOiIjOTM3MERCIiwiYm9yZGVyMiI6IiNhYWFhMzMiLCJhcnJvd2hlYWRDb2xvciI6IiMzMzMzMzMiLCJmb250RmFtaWx5IjoiXCJ0cmVidWNoZXQgbXNcIiwgdmVyZGFuYSwgYXJpYWwiLCJmb250U2l6ZSI6IjE2cHgiLCJsYWJlbEJhY2tncm91bmQiOiIjZThlOGU4Iiwibm9kZUJrZyI6IiNFQ0VDRkYiLCJub2RlQm9yZGVyIjoiIzkzNzBEQiIsImNsdXN0ZXJCa2ciOiIjZmZmZmRlIiwiY2x1c3RlckJvcmRlciI6IiNhYWFhMzMiLCJkZWZhdWx0TGlua0NvbG9yIjoiIzMzMzMzMyIsInRpdGxlQ29sb3IiOiIjMzMzIiwiZWRnZUxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJhY3RvckJvcmRlciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImFjdG9yQmtnIjoiI0VDRUNGRiIsImFjdG9yVGV4dENvbG9yIjoiYmxhY2siLCJhY3RvckxpbmVDb2xvciI6ImdyZXkiLCJzaWduYWxDb2xvciI6IiMzMzMiLCJzaWduYWxUZXh0Q29sb3IiOiIjMzMzIiwibGFiZWxCb3hCa2dDb2xvciI6IiNFQ0VDRkYiLCJsYWJlbEJveEJvcmRlckNvbG9yIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwibGFiZWxUZXh0Q29sb3IiOiJibGFjayIsImxvb3BUZXh0Q29sb3IiOiJibGFjayIsIm5vdGVCb3JkZXJDb2xvciI6IiNhYWFhMzMiLCJub3RlQmtnQ29sb3IiOiIjZmZmNWFkIiwibm90ZVRleHRDb2xvciI6ImJsYWNrIiwiYWN0aXZhdGlvbkJvcmRlckNvbG9yIjoiIzY2NiIsImFjdGl2YXRpb25Ca2dDb2xvciI6IiNmNGY0ZjQiLCJzZXF1ZW5jZU51bWJlckNvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IiOiJyZ2JhKDEwMiwgMTAyLCAyNTUsIDAuNDkpIiwiYWx0U2VjdGlvbkJrZ0NvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IyIjoiI2ZmZjQwMCIsInRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJ0YXNrQmtnQ29sb3IiOiIjOGE5MGRkIiwidGFza1RleHRMaWdodENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dERhcmtDb2xvciI6ImJsYWNrIiwidGFza1RleHRPdXRzaWRlQ29sb3IiOiJibGFjayIsInRhc2tUZXh0Q2xpY2thYmxlQ29sb3IiOiIjMDAzMTYzIiwiYWN0aXZlVGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsImFjdGl2ZVRhc2tCa2dDb2xvciI6IiNiZmM3ZmYiLCJncmlkQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JrZ0NvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCb3JkZXJDb2xvciI6ImdyZXkiLCJjcml0Qm9yZGVyQ29sb3IiOiIjZmY4ODg4IiwiY3JpdEJrZ0NvbG9yIjoicmVkIiwidG9kYXlMaW5lQ29sb3IiOiJyZWQiLCJsYWJlbENvbG9yIjoiYmxhY2siLCJlcnJvckJrZ0NvbG9yIjoiIzU1MjIyMiIsImVycm9yVGV4dENvbG9yIjoiIzU1MjIyMiIsImNsYXNzVGV4dCI6IiMxMzEzMDAiLCJmaWxsVHlwZTAiOiIjRUNFQ0ZGIiwiZmlsbFR5cGUxIjoiI2ZmZmZkZSIsImZpbGxUeXBlMiI6ImhzbCgzMDQsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlMyI6ImhzbCgxMjQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNCI6ImhzbCgxNzYsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNSI6ImhzbCgtNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU2IjoiaHNsKDgsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNyI6ImhzbCgxODgsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSJ9fSwidXBkYXRlRWRpdG9yIjpmYWxzZX0)
