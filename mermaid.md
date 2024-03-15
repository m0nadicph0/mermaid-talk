---
theme: gaia
_class: lead
paginate: true
backgroundColor: #B2BEBF
color: #3B3936
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# Mermaid
`Diagram As Code`

---

## Introduction

> Mermaid is a text/code based diagramming tool for easy creation of various diagrams and visualizations, using simple text-based syntax.

---

## Example

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hello Bob, how are you?
    Bob-->>Alice: Jolly good!
```

![bg right:50% 100%](mmds/basic.mmd.svg)

---

## Universal Selling Proposition
- Simple Text based syntax.
- Version control friendly.
- Wide range of Diagram Types.
- Offers extensive styling and configuration options.
- Integration with Markdown, Confluence, and other tools.


---

## Supported Tooling
- Live Editor (https://mermaid.live/)
- Draw.io
- Markdown Editors
- Confluence
- VS Code Extension
- GitHub Integration
- GitLab Integration
- Jupyter Notebooks

---

<style scoped>
h1 {
    text-align:center;
    margin-top: 20%;
}
</style>

# Example Diagrams

---
#### Sequence Diagram

```mermaid
sequenceDiagram
    participant CH as Cardholder
    participant MR as Merchant
    participant PG as Payment Gateway
    participant CN as Card Network
    participant TS as Tokenization Service

    Note over CH, MR: Purchase request    

    CH->>MR: Initiates purchase with EMV card
    MR->>PG: Sends payment request
    PG->>CH: Requests card details
    CH->>PG: Provides card details
    PG->>TS: Requests tokenization
    TS->>TS: Tokenize card details
    TS-->>PG: Returns token
    PG-->>MR: Receives token
    MR->>PG: Submits token for payment
    PG->>CN: Processes payment with token
    CN-->>PG: Payment response
    PG-->>MR: Payment success/failure
    MR-->>CH: Notifies purchase status
```

![bg right:65% 50%](mmds/sequence.mmd.svg)

---

## Flowchart
```mermaid
graph TD;
    A[Start] --> B[Visit Online Store];
    B --> C[Browse Products];
    C --> D{Product Found?};
    D -->|Yes| E[Add to Cart];
    D -->|No| C;
    E --> F{More Items?};
    F -->|Yes| C;
    F -->|No| G[Proceed to Checkout];

```

![bg right:50% 30%](mmds/flow.mmd.svg)

---
## State Diagram

```mermaid
stateDiagram
    [*] --> Solid
    Solid --> Liquid : Melting
    Liquid --> Solid : Freezing
    Liquid --> Gas : Vaporization
    Gas --> Liquid : Condensation
    Solid --> Gas : Sublimation
    Gas --> Solid : Deposition
    Gas --> [*]
```

![bg right:50% 100%](mmds/state.mmd.svg)

---

## Example Diagrams for Product Managers and Business Analysts

--- 

## Product Roadmap

![bg 60%](mmds/product-roadmap.mmd.svg)

---
## User Journey Maps
![bg 60%](mmds/journey.mmd.svg)


---
## Decision Trees
![bg 60%](mmds/decision-trees.mmd.svg)


---
## Business Process Diagrams 

![bg 50%](mmds/business-process.mmd.svg)

---


## Timelines 

![bg 60%](mmds/timeline.mmd.svg)

---

## Example Diagrams for Developers and Architects

--- 

## System Architecture Diagrams
![bg 60%](mmds/system-architecture.mmd.svg)

--- 

## Database Schema Visualization
![bg 25%](mmds/database.mmd.svg)

--- 

## API Interaction Diagrams
![bg 30%](mmds/api.mmd.svg)

--- 

## Git Graph
![bg 60%](mmds/git.mmd.svg)

---



## Demo
### `Mermaid + Draw.io`

---
Copy the snippet
`Draw.io -> Arrange -> Insert -> Advanced -> Mermaid`

```mermaid
graph TD;
    A[Start] --> B[Visit Online Store];
    B --> C[Browse Products];
    C --> D{Product Found?};
    D -->|Yes| E[Add to Cart];
    D -->|No| C;
    E --> F{More Items?};
    F -->|Yes| C;
    F -->|No| G[Proceed to Checkout];
```



---
## Demo
### `Mermaid + Chat GPT`

---
### Prompt

```
I'd like you to generate a sequence diagram for the following payment transaction workflow:

Actors: Cardholder, Merchant, Payment Gateway, Card Network, Tokenization Service

Workflow:
1. The Cardholder initiates a payment transaction with the Merchant.
2. The Merchant sends the card data (e.g., card number, expiry date, CVV) to the Payment Gateway.
3. The Payment Gateway initiates the tokenization process by sending a request to the Tokenization Service.
4. The Tokenization Service generates a unique token for the provided card data and sends it back to the Payment Gateway.
5. The Payment Gateway receives the token from the Tokenization Service and forwards it to the Merchant.
6. The Merchant processes the payment using the tokenized card data (without storing the actual card details).
7. At a later point, when needed (e.g., for refunds or disputes), the Payment Gateway requests the de-tokenization of the payment data from the Tokenization Service.
8. The Tokenization Service retrieves the original card data associated with the token and sends it back to the Payment Gateway.
9. The Payment Gateway receives the de-tokenized card data and completes the payment transaction with the Merchant using the original card data.

Additional Notes:
* You can simplify the diagram by omitting details like specific message formats or error handling.
* Generate the diagram in mermaid syntax. 
* Add short aliases for the Actors.
```
---

## Thank You!

