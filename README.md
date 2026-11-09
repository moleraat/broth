I want to explore the state-space of governance of resources. I want to track the production, the distribution, and the structures that emerge. The components and their mechanisms.

Simplest first attempt at creating an environment for exploring the development and tradeoffs of organizational structures. Agents need energy to act and are compute/memory bound. 

To start:
- Grid world.
- One energy resource type. Randomly spawned, infinite depth.
- N agents spawned. They can replicate and die. They can act physically on the world, act mentally in their world, and communicate.
- Limited ceiling of compute and memory allocated to env. Start with base scheduler and allocator. Make very modifyable. 
- Communication pipes. One-to-one, one-to-many, many-to-one. Channels?
- Data can be set to public or private (within a group). Need to impl read write access
- Decision making procedures. Needs to define voting rights and procedures. Then needs to define how the decision is persisted and can be later mutated. Also lifetime? Work to be done? Observation, performance, and resource allocation?
- Memory location should have a direct cost (exaggerate time difference for i/o based on relative addresses)?

Problems / open questions:
- How will replication work? Leave open to implementation? Maybe just define interface for now.
- How to define different agent actions? Want it to not be a fixed list, but maybe start with some primatives? Allow ability to compose actions into new callable actions
- How will communication work? How will it be tracked? big ol DAG?
- How will grouping work? Base nodes (agents) should be able to be added to and removed from composite nodes (groups)
- Unsure if scheduler / allocator is the right shape for abstration here. Good for computers, but not sure if it generalizes to humans. 

Core properties:
- Positive sum. Certain resources (compute, memory) are finite. Certain resources (food?) can be practically infinite.
- Want to track what is being worked on, how much is being produced, how products are allocated, and the process for deciding how things get routed
- Track specialization and stratification