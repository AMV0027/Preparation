```mermaid
graph TD
  A1[Admin Portal - React] --> A2[Upload PDF]
  A2 --> A3[Backend - NodeJS]
  A3 --> A4[PDF Processor - Python]
  A4 --> A5[Generate Embeddings + Image Keys]
  A5 --> A6[Store in PostgreSQL and pgvector]

  U1[User Chat UI - React] --> U2[Enter Query]
  U2 --> U3[NodeJS Server - Auth + API]
  U3 --> U4[GCN - Get Similar PDFs]
  U4 --> U5[Vector Search - Get Content & Pages]

  U3 --> O1[Online Context Wrapper - Python]
  O1 --> O2[Generate Search Query]
  O2 --> O3[Scrape Top 5 Links (Playwright)]
  O3 --> O4[Extract Text, Images, Videos]

  U5 --> F1[AI Middleware - Combine Contexts]
  O4 --> F1
  U2 --> F1

  F1 --> R1[Generate Final Answer + Metadata]
  R1 --> R2[Send to Chat UI]
  R1 --> R3[Store in PostgreSQL - History]

  subgraph Admin Flow
    A1 --> A2 --> A3 --> A4 --> A5 --> A6
  end

  subgraph User Flow
    U1 --> U2 --> U3 --> U4 --> U5
    U3 --> O1 --> O2 --> O3 --> O4
    U5 --> F1
    O4 --> F1
    U2 --> F1
    F1 --> R1 --> R2
    R1 --> R3
  end
```
