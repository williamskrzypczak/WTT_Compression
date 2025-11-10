# Alert Flow Overview

© 2025 Bulldog Ventures Inc. All rights reserved.

This diagram illustrates how the `WTT_Compression` indicator detects a doji, confirms breakout direction, and fires alerts when enabled.

```mermaid
flowchart TD
    A[New bar] --> B{Valid data?}
    B -->|No| Z[Stop]
    B -->|Yes| C{Body <= threshold?}
    C -->|No| Z
    C -->|Yes| D{Prior bar doji?}
    D -->|No| Z
    D -->|Yes| E{Break above high?}
    E -->|Yes| F[isBullBreakout]
    E -->|No| G{Break below low?}
    G -->|Yes| H[isBearBreakout]
    G -->|No| Z
    F --> I{enableAlerts?}
    H --> J{enableAlerts?}
    I -->|Yes| K[alert bull]
    I -->|No| Z
    J -->|Yes| L[alert bear]
    J -->|No| Z
    K --> Z
    L --> Z
```
