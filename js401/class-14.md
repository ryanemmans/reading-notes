# CascadiaJS - Day 2

## Brooklyn Zelenka - CTO at Fission - “Web3 for Fun and Profit”

What is Web3?

- “A technological and social movement characterized by openness, interoperability, and user agency.”
  - More or less an evolved version of the internet, as of 2020
  - Decentralization (networks), non-discrimination, bottom-up design, universality, consensus
  - Network Topologies - Star (centralized), Hub (decentralized), Mesh (distributed)
  - Return to peer-to-peer computing (distributed)
- Agency & Ownership
  - User Agency - lower barrier to entry, empower users to participate (entry)
  - Digital Scarcity - Control your ID, own your data, provable uniqueness (*Sign your Git commits!)
  - User-Controlled Data - user managed encryption
  - OAuth Sequence - Auth flow
  - UCan Sequence - JWT++
    - Everything is self contained, no longer living in a database
  - Permissionless - open source is now open data
- Commons Networks - owned by everyone, participating therefore strengthening
- The End of (Infra) History -
- Toolbox - cloud, serverless, local-first, offline, P2P, commons, blockchain
  - Resources - proto.school, js.ipfs.io, ethereum devs, github automerge, npm ucans

## Ian Sutherland - “Developer Experience for Internal Teams”

Engineering lead and DX Team Lead at Neo Financial, maintains React and Node.js team member

- Examples of good DX
  - Stripe, APIs and SDKs, great documentation, sandbox environment
  - GitHub - Actions, CLI, web-based VS Code, Codespaces
- Neo - Canadian FinTech startup - consumer banking products
- DX is a way to improve productivity and reduce time spent, making work easier
- Working locally and Continuous Integration and Deployment all bring challenges
- Custom Tools - CLI apps, desktop apps, web apps, documentation, videos, talks, training
- Developer Relations - feedback, support, listen
- Best practices - use your team, treat tools like production software, metrics and analytics, solicit feedback, documentation, automatic updates, make tools fun (sparingly)

## Jacques Favreau - Senior Engineer at Netflix - “The Fellowship of the String”

Successful refactoring with empathy and small bites

- Spoke on the challenges of shifting Netflix from Java over to React and Node with a growing team
  - Incorporating empathic approach to achieve successful change, finding balance between code work and human work.
  - Define the problem, gather your voices, technical solution, marketing, technical pre-work, manual changes
    - Work backwards from goal to realize prerequisites
    - Codemods (ESLint) - programmatic way to translate web syntax into another - Compilers for Humans

## Daria Caraway - Senior UI Engineer at Netflix - “A Wild TypeScript Safari”

- Generic type - stand in representation for a type that is provided by the input or consumer
- Union type - value that can be one of many types
- Conditional type - similar to JS conditional expression, allows for if-then statement
- `keyof` operator - type operator that crates a union type from the keys of the provided type
- Utility type - globally availability type that represents commony type transformations provided by TS
- `Exclude` - returns provided type minus any union members that match union to exclude
- `Pick` - returns new type from provided type with only the keys you give it
- I’m looking forward to learning more about TypeScript after 401.

## Garann Means - "JavaScript, Cyber-abuse and the Illusion of Privacy"

- Security Through Obscurity
- Trust No One!

## Feross Aboukhadijeh - “It's a Jungle Out There!”

- Spoke on the increasing presence of malware in NPM packages, scary stuff.
