# Security Assessment $PRODUCT

|     |     |
| --- | --- |
| Contact for product        | [@github](https://github.com/github) |
| Security responsible       | [@github](https://github.com/github) |
| Version number of product  |      |
| Dates of assessment        | 1970-01-01: Created DFD |
|                            | 1970-01-10: Discussion of threats |
|                            | 1970-01-25: Finalized assessment  |
| Status of assessment       | DRAFT/FINAL/RE-ASSESSMENT DRAFT |

## Product Description

Short description of the main functionality in two to three sentences.

### Important Links
* E.g., Documentation on GitHub and elsewhere, description of service, old assessments, connected repos

## Existing Security Controls

Primary controls implemented on product (or on specific aspect of product):

* xxx – description
* yyy – description

## Data Flow Diagram (DFD)

```mermaid
%% ----------------------
%% -- BEST PRACTICES ----
%% ----------------------
%% .
%% === OUT OF SCOPE ====
%% mark out of scope elements with ":::oos", e.g., backend_process(("Backend")):::oos
%% mark out of scope data flows as dotted links, e.g., A -. "text" .-> B
%% .
%% === MOVING STUFF AROUND ====
%% Use hidden links to force mermaid.js to reposition some elements, e.g., A ~~~ B
%% Use hidden subgraphs to position elements closely together by naming the subgraph `_hidden`
%%     subgraph _hidden
%%       process((Process))
%%       interactor[Interactor]
%%       process --> interactor
%%     end
%% For nested, hidden subgraphs, use: _hidden, _hidden1, _hidden2, _hidden3

%% ----------------------
%% -- START DFD ---------
%% ----------------------

flowchart
%% replace `flowchart` with `flowchart LR` for a left-to-right oriented flowchart

  ext_interactor["External \n Interactor"]
  ext_interactor2["External \n Interactor 2"]:::oos

  subgraph "Trust Boundary"
    process(("Process"))
    data_store[|borders:tb|"Data Store \n PostgreSQL"]
    process -- "Data" --> data_store
  end

  ext_interactor -- "Input:\nData (e.g., User Data)\nProtocol (e.g., HTTP)" --> process
  ext_interactor2 -. "Out of scope \n data flow" .-> ext_interactor

%% ----------------------
%% -- END DFD -----------
%% ----------------------

classDef cluster fill:transparent,stroke:#d66,stroke-width:2px,stroke-dasharray: 10 6;
classDef node fill:#fafafa,stroke:#222;
classDef edgeLabel background-color:#ffffffaa,display:inline-block;
classDef oos fill:#fff,stroke:#888,color:#888,stroke-dasharray: 5 5,stroke-width:1px;
linkStyle default stroke:#222,stroke-width:1px;
%%{init:{'theme':'neutral', 'themeCSS':'#_hidden,#_hidden1,#_hidden2,#_hidden3{display:none;}.edge-pattern-dotted{stroke:#888!important;stroke-width:1px!important;stroke-dasharray: 6 5!important;}'}}%%
```

Place for additional information on data flows and the data flow diagram. The following list may be used as a guidance and should not be included into the final version of the assessment.

Key Information Needed for DFD:
* Interactor
* Target of Interaction
* Interaction Description
* Session Management (Token, Lifetime, Type, etc.)
* Input Validation Controls
* Availability Controls (e.g. rate limiting, pod resiliency, etc.)
* Zone Type (cloud, container, etc.)
* Access Rights available
* Access Type 
* Sensitive Data in interaction?
* Network Protocol
* Encryption (TLS, algorithm, key length)
* Authentication
* Credential Storage
* Logging

### Changes compared to last Security Assessment

Mention date of last security assessment (if not already done in the header of the document) and changes to the architecture and security controls since the last assessment.

## Threats & Risks
All identified, exploitable threats and risks must be reported via **GitHub security advisories** using the *Security* tab in GitHub. See also SECURITY.md in the root of this repo. Links to GitHub security advisories may be added to this document.

Non-critical threats and findings may be submitted as issues, instead, and should be linked from this document.
