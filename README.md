# OWL

OWL is a community driven testing lab comprising of an extensible set of open source vendor neutral validation tools and testing frameworks designed to validate the functionality, scalability, and interoperability of wallets, agents, and other components within the decentralized trust ecosystems. 

The OWL name is a nod to the Telecom industry's interoperability "Labs", such as at [UNH](https://www.iol.unh.edu/), where environments are created to enable vendors and product creators to bring their products to test with others. The not-an-acronym name OWL is to prevent confusion with the OpenWallet Foundation's "Labs" maturity level.

## OWL Agent Test Harness
Agent Test Harness (OATH) is a collaborative platform and environment that is crucial for ensuring that different decentralized trust agent implementations, which are responsible for handling decentralized identifiers (DIDs) and exchanging verifiable credentials, can interoperate seamlessly. OATH currently includes support for Credo-TS and ACA-Py, among others. It's strength is in the emphisis of:
* Interoperability over individual agent functionality
* Real agent communication over test or reference agents
* Protocol RFCs over specific vendor agent implementations
* Elevating communication and ease of test writing to the level of code
* Industry-standard test libraries using Behavior-Driven Development (BDD)
* An API to drive agent interoperability, agnostic of underlying technology.

A summary of OATH's daily interoperability test runs are published on the website [https://aries-interop.info](https://aries-interop.info).

### Features

* Interoperability Testing: Agent Test Harness is specifically designed to test the interoperability of agents by executing interactions between them, ensures that agent implementations can communicate using standard protocols, exchange verifiable credential, resolve DIDs, and other core functions reliably.
* Automation: The Agent Test Harness automates the testing of agents, making it easier for developers to continuously verify the compliance and performance of their implementations. Developers can configure what agent implementations with whom they want to test interoperability and for each, what specific tests they want executed. Implementations can even include their CI pipelines select Agent Test Harness interoperability tests.
* Extensibility: The framework is highly extensible, allowing developers to add their implementations for testing and to construct custom tests and scenarios that suit a wide variety of use cases. This flexibility is important for testing a wide range of decentralized identity solutions across different industries.
* Comprehensive Coverage: The test harness covers a wide array of functionalities that decentralized trust agents should support, including secure messaging, protocols, and credential issuance, verification and revocation across a range of credential formats.
* Community-Driven: Agent Test Harness is intended to be developed and maintained by a global community of contributors to ensure that it stays up-to-date with the latest standards and best practices in the decentralized identity space.
* Protocol RFC focused tests: With interoperability as the key consideration, the Protocol RFCs are used for test specification ignoring what a specific vendors agent might do outside of that protocol's requirements.  
* Use OATH Agents as a service: The decentralized trust agents supported in OATH can be used as services outside of the interop test environment. For example the Mobile Wallet Test Harness uses these agents as issuers and verifiers for much of the mobile testing.

For more information, visit the [OWL Agent Test Harness GitHub repository](https://github.com/openwallet-foundation/owl-agent-test-harness).

## OWL Mobile Wallet Test Harness
The Mobile Wallet Test Harness (OMWTH) is an automated acceptance testing framework tailored for mobile wallets to simulate and validate app functionality across mobile devices, locally or in a cloud environment, real or simulated. The main components that make up the framework are Python, Behave, and Appium. It takes the best mobile testing practices and decentralized trust agent testing practices and combines them to create an extensible testing platform for validating any Mobile Wallet end to end from the Holder’s perspective (wallet focused), utilizing any/multiple issuers and verifiers.

### Features
* Automated acceptance testing for any Mobile VC Wallet, in and out of a CI/CD Pipelines
* Integration with Python and Behave for behavior-driven development
* Utilization of Appium for cross-platform mobile testing
* Interfaces with Cloud Device Services and local emulators, with the ability to easily extend interfaces to other device services.
* Interfaces with AATH supported frameworks, so you can test your wallet with any frameworks acting as issuer and/or verifier. Frameworks such as ACA-py, Credo-ts, Aries VCX, etc.
* Issuer/Verifier agnostic tests - Run the same wallet tests against almost any AATH issuer/verifier.
* Agent interface that can be quickly implemented and support any new issuer or verifier, even if web based with no API. Then run your existing tests with that new issuer/verifier.
* Utilizes the Page Object Model to isolate tests from app screens.


For more information, visit the [OWL Mobile Wallet Test Harness GitHub repository](https://github.com/openwallet-foundation/owl-mobile-wallet-test-harness).

## Akrida
Akrida provides a scriptable framework for generating load against a deployment of agents for messaging and exchanging credentials. This allows users of OWF technologies to apply a significant generated load on their deployment to ensure it will scale as needed, and to identify and address bottlenecks.

Built on the [Locust](https://locust.io) framework, Akrida is primarily used to test server infrastructure by replicating the load of multiple holder agents while communicating with other issuer, verifier, and mediator agents involved in the system.

### Features
* Load Testing Framework: Built on the Locust platform, providing a proven solution for load testing various environments.
* Decentralized Identity Simulation: Supports multiple agent types (holder, mediator, issuer, verifier) to create realistic testing scenarios.
* Independent User Scaling: Each user operates independently via separate processes, allowing for more accurate simulation of real-world clients.
* Multiple Holder Agents: Locust can run several holder agents per instance, controlled by a master instance for scalability.
* Easy-to-Use Interface: Provides user-friendly metrics and interfaces for managing load tests.
* Open Source: Akrida is open-source, encouraging community engagement and contributions.
* Support for Clustering: Capable of scaling through clustering, allowing for extensive load tests.
* Protocol Compatibility: Uses Aries Framework Javascript for DIDComm protocol, making it compatible with many existing DIDComm clients.
* Subprocess Handling: Implements subprocesses for handling CPU-intensive tasks like encryption, ensuring that high-load tests run efficiently.
* Error Handling and Recovery: Incorporates robust error handling mechanisms to manage subprocess failures and maintain test integrity.
* Test Coverage: Includes various test scripts designed to evaluate specific functions such as issuing credentials, receiving messages, and checking issuer status.

For more information, visit the [OWL Akrida GitHub repository](https://github.com/openwallet-foundation/owl-akrida).


## Test Harness Road Maps and Backlogs
The OWL project will be managed through one project board in GitHub Projects. This includes a kanban board along with short term and long term road maps. All OWL Test Harness are contained in this one project and can be filtered to display the test harness of current interest.

[OWL Project Board](https://github.com/orgs/openwallet-foundation/projects/4)

## Community

The OWL Users Group Meetings are held monthly and include status and discussions on the test harnesses of OWL. 

* [OWL Users Group Meeting in Hyperledger](https://lf-hyperledger.atlassian.net/wiki/spaces/ARIES/pages/18496334/Aries+Test+Harness+User+Group+-+ATHUG) (*To be moved to OWF*)

* [OWL Users Group Meeting in OpenWallet Foundation](https://zoom-lfx.platform.linuxfoundation.org/meetings/openwalletfoundation?view=week&occurrence=1729782000)

Daily discussions about the OWL projects take place on the Discord channel.

* [OWL Discord Channel](https://discord.com/channels/1022962884864643214/1214965981470924911)

## Governance

The OWL project has adopted a consensus-based governance model, ensuring that decisions are made collaboratively with input from the community. Contributors discuss issues and work towards agreements that reflect the collective interest, with the goal of achieving consensus among participants. Key decisions regarding the project’s direction, feature additions, and roadmap are reached through open discussions, with an emphasis on transparency and inclusivity. In cases where consensus cannot be easily achieved, the group of active maintainers have the authority to guide decision-making. This governance approach fosters an open, community-driven environment that encourages diverse input and ensures that OWL remains aligned with the needs of its contributors and users.

