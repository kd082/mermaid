```mermaid
graph TD
    A[Start] --> B{EL9 = Direct Transport CX OR Small BCO CX?};
    B -- No --> F[""];
    B -- Yes --> C{EB9 contains "KC", "RW", or "ICX"?};
    C -- Yes --> G[Return EB9];
    C -- No --> D{ED9 contains "KC", "RW", or "ICX"?};
    D -- Yes --> H[Return ED9];
    D -- No --> E{EE9 contains "KC", "RW", or "ICX"?};
    E -- Yes --> I[Return EE9];
    E -- No --> J{EG9 contains "KC", "RW", or "ICX"?};
    J -- Yes --> K[Return EG9];
    J -- No --> F;
