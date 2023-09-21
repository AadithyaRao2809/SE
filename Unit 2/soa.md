### SOA
*Service Oriented Architecture*
##### SOA Overview
- **Goal:** Make software components reusable via service interfaces.
- **Key Features:**
  - Utilizes common communication standards.
  - Enables rapid integration into new applications without deep integration.
  - Each service encapsulates a discrete business function, promoting loose coupling.
  - Exposed using standard network protocols (SOAP/HTTP or JSON/HTTP) for data interaction.
  - Comprises structured collections of software modules providing functionality.

##### Benefits
- **Greater Business Agility:** Faster time to market.
- **Legacy Functionality Leveraging:** Ability to use existing functionality in new markets.
- **Improved Collaboration:** Enhances cooperation between business and IT.Providing standardized interfaces, clear service contracts, and reusable services.
- **Service Reusability:** Encourages the reuse of services.

##### Service
- A logical representation of a repeatable business activity with a specified outcome.
- Discrete pieces of software, written in any language.
- Accessed through message exchange, like "callable entities."
- Offers application functionality with wrappers.

##### Service Characteristics
- Services adhere to a service contract and communication agreement.
- Loosely coupled to minimize dependencies while maintaining awareness of each other.
- Stateless to reduce resource consumption.
- Autonomous and reusable.
- Utilize open standards to facilitate interoperability.
- Can be discovered through metadata.
- Can be composed to form larger services.

##### SOA Roles
- **Service Provider:** Creates web services and offers them through a registry, defining terms of service.
- **Service Broker/Registry:** Provides information about available services.
- **Service Requester/Consumer:** Discovers services in the broker and connects to the provider.

[[unit-2|Unit 2]]
