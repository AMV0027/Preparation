```mermaid
graph TD
  A1[Admin Portal - React] --> A2[Upload PDF]
  A2 --> A3[Backend NodeJS]
  A3 --> A4[PDF to Text + Image Extractor (Python)]
  A4 --> A5[Custom Embeddings Generator]
  A5 --> A6[Vector + Metadata Storage<br/>PostgreSQL + pgvector]

  U1[User Chat UI - React] --> U2[Enter Query]
  U2 --> U3[NodeJS Server - Auth + Middleware]
  U3 --> U4[GCN Algorithm Fetches Similar PDFs]
  U4 --> U5[Vector Search for Similar Contexts]
  U5 --> U6[Get Page Numbers + Content]

  U3 --> O1[Online Context Wrapper - Python FastAPI]
  O1 --> O2[Generate Search Query]
  O2 --> O3[Playwright - Scrape Top 5 Results]
  O3 --> O4[Extract Text, Images, Videos]

  U6 --> F1[AI Middleware API - Python]
  O4 --> F1
  U2 --> F1

  F1 --> R1[Final Answer + Metadata]
  R1 --> R2[Send to Frontend Chat]
  R1 --> R3[Store in PostgreSQL<br/>History + Results]

  subgraph Admin Flow
    A1 --> A2 --> A3 --> A4 --> A5 --> A6
  end

  subgraph User Flow
    U1 --> U2 --> U3 --> U4 --> U5 --> U6
    U3 --> O1 --> O2 --> O3 --> O4
    U6 --> F1
    O4 --> F1
    U2 --> F1
    F1 --> R1 --> R2
    R1 --> R3
  end
```
