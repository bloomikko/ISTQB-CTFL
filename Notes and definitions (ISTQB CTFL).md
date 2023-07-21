# Notes and definitions / ISTQB Foundation Certification v4.0
**acceptance test-driven development (ATDD)**  
tests are written before the user story is implemented, based on the acceptance criteria of the software

**behavior-driven development (BDD)**  
test cases are written in natural language, common format is using Given/When/Then attributes

**black-box / specification-based test techniques**  
- *equivalence partitioning*: divides the data into partitions with the expectation that all elements of given partition will be processed in the same way by the test object &rarr; if a value fails in an equivalence partition, the defect should be detected by other values too
- *boundary value analysis (BVA)*: inspects the boundaries of equivalence partitions
  - if two elements belong to the same partition, all elements between them must also belong to that partition
  - typical defect is misplaced or missing boundaries
  - 2-value BVA: examining each boundary value with closest value from neighboring partition
  - 3-value BVA: the same as 2-value, but examines both values surrounding the boundary value
- *decision table testing*: specify how different combinations of conditions result in different outcomes, for example creating a True/False table for login screen (email, password, expected output)
- *state transition testing*: explores the system by showing its possible states and valid state transitions, transition is initiated by an event
  - all states coverage: every single state of the test object must be visited
  - valid transitions coverage / 0-switch coverage: test cases cover all the valid transitions
  - all transitions coverage: the transitions shown in a state table, the test cases must cover all valid transitions and attempts to execute invalid transitions

**collaboration-based test approaches**  
- *collaborative user story writing*: user story represents a feature that will be valuable for the end user
  - three critical aspects:
    - card: medium describing the user story (for example, an entry in Jira/Confluence)
    - conversation: explanation how the software will be used
    - confirmation: acceptance criteria for the user story
  - for example, "As a [role], I want [goal to be accomplished], so that I can [resulting business value for the role]", which is followed by the acceptance criteria
  - different techniques can be used, such as brainstorming and mind mapping
- *acceptance criteria*: attached to the user story, conditions that an implementation of the user story must meet to be accepted by stakeholders, usually written in scenario-oriented or rule-oriented way:
  - scenario-oriented: for example Given/When/Then format
  - rule-oriented: for example bullet point verification list
- *acceptance test-driven development (ATDD)*: see separate definition
  - process: specification workshop where the user story and its acceptance criteria are analyzed &rarr; creating the test cases which are based on the acceptance criteria

**configuration management (CM)**  
- provides a discipline for identifying, controlling and tracking work products
- keeps a record of changed configuration items when a new baseline is created
- requirements to properly support testing
  - all configuration items are uniquely identified, version controlled, tracked for changes and related to other configuration items so that traceability can be easily maintained during test process
  - all configuration items must be referenced in the test documentation

**confirmation testing**  
confirms that an original defect has been fixed, for example by testing all test cases which previously have failed or adding new tests to cover any changes that were needed to fix the defect

**continuous delivery (CD)**  
part of DevOps delivery pipeline where high quality code is released constantly

**continuous integration (CI)**  
developers submit high quality code accompanied by component (unit) tests and static analysis

**debugging**  
finding reasons of found failure, afterwards analyzing and eliminating them (example process: reproduction of a failure &rarr; diagnosis &rarr; fixing the cause)

**defect**  
fault, bug, cause from an error or mistake

**Definition of Done**  
Agile-based definition for exit criteria

**defect management**  
process for handling defects found during testing &rarr; at minimum includes a workflow for handling individual anomalies from their discovery to their closure

**defect report**  
- document from defect management, usually has these objectives:
  - provides sufficient information to resolve the issue
  - provides a mean to track the quality of the work product
  - provides ideas for improving development and test processes
- usually includes e.g. unique identifier, title, date, context of the defect, description of the failure to enable reproduction, expected results and actual results

**DevOps**  
approach to create synergy by getting development and operations to work together to achieve a set of common goals

**dynamic testing**  
testing that involves the execution of the software, usually done to trigger failures in the software that are caused by defects

**entry criteria**  
preconditions for undertaking a given activity, examples include availability of resources and testware

**error**  
a mistake, for example a coding error which causes a defect

**estimation techniques**  
- *estimation based on ratios*: previous project data is used to form standard ratios for similar projects, usually organization's own project historical data is used for this
- *extrapolation*: measurements are made as early as possible to gather the data &rarr; with enough observations over time, the effort required for the remaining work can be estimated by extrapolating the observation data
- *wideband delphi*: experts make experience-based estimations in isolation &rarr; results are collected and possible deviations are analyzed &rarr; new estimations are made in isolation based on feedback &rarr; process is repeated until consensus is reached
- *three-point estimation*: experts make three estimations, the most optimistic estimation, the most likely estimation and the most pessimistic estimation, which are combined as their weighted arithmetic mean 
  - formula: (most optimistic + 4 * most likely + most pessimistic) / 6

**exit criteria**  
conditions which must be achieved in order to declare an activity completed, examples include achieved level of coverage, number of unresolved defects and failed test cases

**experience-based test techniques**  
- *error guessing*: the tester anticipates the occurrence of errors, defects and failures, based on the tester's knowledge
- *exploratory testing*: tests are simultaneously designed, executed and evaluated while the tester learns about the test object, many times used as session-based approach or if there is a major time pressure on the testing
- *checklist-based testing*: the tester designs the tests based on a checklist &rarr; usually checklist items are phrased in the form of a question (common danger: the developers will learn to avoid making the same errors, so the checklist might become useless for testing if it is not constantly updated)

**failure**  
state followed from a defect, example: developer makes a coding mistake by error &rarr; the code has a defect &rarr; the application crashes because of this defect (&rarr; failure)

**fault attack**  
tests are based on a list of possible errors, defects and failures &rarr; the list usually is built based on experience, defect and failure data or common knowledge about software failures

**fault masking**  
one defect prevents the detection of another

**hot fix**  
unplanned release, for example to quickly address a critical bug

**impact analysis**  
analyzing the width of the area to be tested, many times used with regression testing to optimize its extent

**independence of testing**  
tackles the problems of tester's cognitive biases, varies by who tests the product: can range from no independence (testing person is the author of the work product) to external testers from outside of the organization (very high independence)

**INVEST**  
evaluation pattern for user stories: Independent, Negotiable, Valuable, Estimable, Small, Testable

**iteration planning**  
planning of a smaller iteration of the developed product: the tester for example does more profound risk analysis of user stories and determines the testability of them

**maintenance testing**  
testing the system after changes happen: often includes risk analysis of the change, analyzing the size of the existing system and the size of the change

**product risk**  
risks which relate to the product quality characteristics, for example missing or wrong functionality, incorrect calculations, runtime errors, poor architecture or inefficient algorithms

**project risk**  
- related to the management and control of the project
  - organizational issues (e.g. delays and inaccurate estimates)
  - people issues (e.g. insufficient skills, conflicts and communication problems)
  - technical issues (e.g. poor support for used tools)
  - supplier issues (e.g. third-party delivery failure or bankruptcy of the supporting company)

**qualitative approach of risk assessment**  
forming the risk level by using a risk matrix (see definition)

**quality assurance (QA)**  
process-oriented and preventive approach focusing on implementation and improvement of processes

**quality control (QC)**  
the activities which support the achievement of appropriate levels of quality

**quantitative approach of risk assessment**  
multiplying the risk likelihood and risk impact

**regression testing**  
testing also surrounding environment after a change is applied &rarr; sometimes the change can unexpectedly affect other areas of the system

**release planning**  
a plan which looks ahead to the release of the product, in this the tester for example writes testable user stories and acceptance criteria

**retrospective**  
post-project meeting, where the project is analyzed with all relevant stakeholders

**review process activities**  
- *planning*: for example defining the scope of the review, work product to be reviewed, quality characteristics, exit criteria
- *review initiation*: making sure everyone and everything involved in the review is ready
- *individual review*: every reviewer does their part of the review and log their observations
- *communication and analysis*: every single detected anomaly is discussed and further actions are decided
- *fixing and reporting*: creating defect reports, reaching exit criteria and reporting the review results

**review roles**  
- *manager*: decides what is being reviewed and provides resources
- *author*: creator and fixer of the reviewed work product
- *moderator/facilitator*: ensures the effective running of review meetings
- *scribe/recorder*: collects and records the data from reviews
- *reviewer*: performs the reviews
- *review leader*: has the overall responsibility for the review

**review types**  
- *informal review*: does not have any kind of defined process
- *walkthrough*: led by the work product author
- *technical review*: performed by technically qualified reviewers, led by a moderator
- *inspection*: most formal review types, has a generic review process (see definition of review process activities)

**risk**  
- potential event, hazard, threat or situation whose occurrence causes a harmful effect
- two factors which together form the risk level (a measure for the risk)
  - risk likelihood: the probability of risk occurrence (range varies from greater than zero and less than one)
  - risk impact/harm: the consequences of this occurrence

**risk management**  
- tool for increasing the likelihood of achieving objectives, improving the quality of products and increasing the stakeholders' confidence and trust
- two main activities:
  - risk analysis: providing awareness of product risk in order to focus the testing accordingly
    - risk identification: generating a comprehensive list of risks
    - risk assessment: categorization of identified risks, determining their risk likelihood, impact and level, prioritizing and proposing ways to handle the risks
  - risk control: the measures against identified and assessed product risks
    - risk mitigation: implementing actions proposed from risk assessment to reduce the risk level
    - risk monitoring: ensuring that mitigation actions are effective and identifying emerging risks

**risk matrix**  
table which has impact on x-axis and probability on y-axis, for example with scaling ranging from 1-5

**root cause**  
fundamental reason for the occurrence of a problem, the situation which leads to an error

**software development lifecycle (SDLC)**  
high-level representation of software development process, various ones exist

**SDLC good testing practices**  
- for every software development activity, there is a corresponding test activity
- different test levels have specific and different test objectives, which allows for testing to be appropriately comprehensive while avoiding redundancy
- test analysis and design for given test level begins during the corresponding development phase of the SDLC so that the principle of early testing is adhered
- testers are involved in reviewing work products as soon as drafts of this documentation are available

**shift-left approach**  
principle of early testing

**smoke test**  
tests which determine whether the product is ready for the next testing phase, usually covers the most crucial functionality of the product

**software testing**  
set of activities to discover defects and evaluate the quality of software artifacts, a form of quality control (QC)

**static analysis**  
tool-assisted static testing, for example detecting code defects

**static testing**  
testing that does not involve the execution of the software, usually manual examinations (reviews) and static analysis

**test analysis**  
"what to test", analyzing the test basis in order to identify testable features, define and prioritize test conditions, and evaluate the risks

**test automation benefits and risks**  
- benefits
  - time saved by reducing repetitive manual work
  - preventing simple human errors
  - objectiveness of the tests (e.g. coverage)
  - easier access to test information
  - reduced test execution time
- risks
  - unrealistic expectations about the benefits of a tool
  - inaccurate estimations of time, costs and effort required to introduce a tool and maintain the test automation
  - using automation when manual testing would be more appropriate
  - ignoring the need of human critical thinking
  - dependency on the tool vendors
  - incompatibility issues
  - tool that does not comply with the regulatory requirements and/or safety standards

**test case**  
sequence of actions, which is necessary to verify a specific functionality or feature of the product

**test case prioritization**  
- *risk-based prioritization*: order of test execution is based on the results of risk analysis
- *coverage-based prioritization*: order of the test execution is based on coverage where test cases achieving the highest coverage are executed first
- *requirements-based prioritization*: order of the test execution is based on stakeholder-defined requirement priorities

**test charter**  
statement of test objectives and possibly test ideas about how to test

**test completion**  
usually companied by project milestones, activities include for example analyzing unresolved defects, change requests and product backlog items

**test design**  
"how to test", forming test conditions into test cases, defining test data requirements, designing the test environment and identifying other necessary infrastructure and tools for testing

**test-driven development (TDD)**  
tests are written before any coding happens

**test execution**  
running the tests, comparing the actual test results with the expected ones, logging the test results and analyzing the anomalies

**test control**  
uses the information from test monitoring to provide control directives, which offer guidance and necessary corrective actions to achieve the most effective and efficient testing

**testing principles**  
1. testing shows the presence, not the absence of defects (testing cannot prove that there are no defects at all)
2. exhaustive testing is impossible (prioritizing testing is essential)
3. early testing saves time and money (defects which are removed early will not cause subsequent defects)
4. defects cluster together
5. tests wear out (tests must be modified over time in order to maintain their effectiveness)
6. testing is context dependent (there is no one-size-fits-all solution, testing is highly contextual)
7. absence-of-defects fallacy (even if the system is completely tested/verified, it can still be useless for end users due to not meeting the needs and expectations)

**testing role**  
overall responsibility for the technical aspect of testing, these activities include test analysis, design, implementation and execution

**test implementation**  
creating and/or acquiring the necessary means for test execution

**test level**  
group of test activities that are organized and managed together  
1. *component/unit testing*: components in isolation, usually performed by developers
2. *component integration testing*: the interfaces and interactions between components
3. *system testing*: overall behavior and capabilities of an entire system or product
4. *system integration testing*: interfaces of the system, of other systems and external services
5. *acceptance testing*: validation and readiness for deployment to production, ideally performed by end users

**test management role**  
overall responsibility for the test process, test team and leadership of the test activities, these activities include test planning, monitoring, controlling and completion

**test metric**  
shows progress against the planned schedule and budget, also can evaluate the current quality of the test object and the effectiveness of the test activities

**test monitoring**  
gathering information about testing, which is used to assess the test progress and measuring whether the text exit criteria associated to general exit criteria are satisfied

**test plan**  
describes the objectives, resources and processes of a test project

**test planning**  
defining the test objectives and then selecting an approach which achieves these objectives in the best way

**test pyramid**  
- tests are ordered by their granularity (the quantity of small details)
  - the highest layer has the lowest granularity, test isolation and test execution time (for example, end-to-end tests)
  - the lowest layer has the highest granularity, small units which work in isolation (for example, unit tests of the code)

**testing quadrants**  
- grouping the test levels with appropriate test types, activities, test techniques and work products in the Agile software development
- combining two viewpoints of business and technology facing tests form four quadrants
  - quadrant Q1, technology facing and supports the team: tests of components and their integrations
  - quadrant Q2, business facing and supports the team: tests that check the acceptance criteria, such as functional tests, examples, user story tests, user experience prototypes, API testing and simulations
  - quadrant Q3: business facing and critiques the product: user-oriented tests such as exploratory testing, usability testing and user acceptance testing
  - quadrant Q4: technology facing and critiques the product: smoke tests and non-functional tests (except usability tests)

**test report**  
- summarizes and communicates test information during and after testing
  - test progress/status report: support the ongoing control of the testing
  - test completion report: summarizes a specific stage of testing and can give information for upcoming testing activities

**test script**  
step-by-step instructions on how to test a test case

**test suite**  
container which has a set of test cases, usually logically grouped to run a single larger job

**test type**  
1. *functional testing*: evaluates the functions that a component or system should perform, checking the functional completeness, correctness and appropriateness
2. *non-functional testing*: evaluating other than functional characteristics, "how well the system behaves", includes for example performance, compatibility, usability and security reliability
3. *black-box testing*: derives tests from documentation external to the test object
4. *white-box testing*: derives tests from system's implementation, such as code, architecture and different kinds of flows inside the system (usually focuses on code coverage)

**testware**  
output work products from the test activities, for example test plan, reports and cases

**traceability**  
essential attribute throughout the test process, eases evaluating the coverage, determining the impact of changes and facilitates the test audits

**white-box test techiques**  
- *statement testing*: coverage items are executable statements, for example if the test goes through all the lines (statements) of the code the coverage is 100%
- *branch testing*: testing every possible branch (many times if-else statement) of program's control flow graph, the goal is to ensure that all reachable code is executed

**whole team approach**  
any team member with the necessary knowledge and skills can perform any (test-related) task, everyone is responsible for quality
