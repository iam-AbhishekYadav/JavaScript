# Control Flow

| if                   |  if , else              | if / else if / else                  | switch                  |
|----------------------|-------------------------|--------------------------------------|-------------------------|
|                      |                         |                                      |                         |
| if ( true ) {        |  if ( false ) {         |    if(false){                        |    switch(key){         |
|    execute code      |     not execute code    |         not execute code             |        case value:      |
| }                    |  } else {               |    } else if ( true ) {              |              code       |
|                      |       execute this      |          execute code                |              break;     |
|                      | }                       |    } else {                          |                         |
|                      |                         |         if(false),else if(false),    |       default:          |
|                      |                         |           execute code               |             code        |
|                      |                         |    }                                 |             break;      |
|                      |                         |                                      |     }                   |




```mermaid
graph TD
    A[JavaScript Control Statements] --> B[Conditional Control Statements]
    A --> C[break statement]
    A --> D[continue statement]
    A --> E[Looping/Iterative Control Statements]

    B --> F[If - Else Statements]
    B --> G[Switch Case Statements]

    E --> H[For Loop]
    E --> I[While Loop]
    E --> J[doWhile Loop]
    E --> K[for...in Loop]
```
