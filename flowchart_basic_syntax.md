# Mermaid Flowchart Syntax Guide

## Basic Syntax

```mermaid
flowchart TD
    A[Start] --> B[Process]
    B --> C{Decision}
    C -->|Yes| D[Option 1]
    C -->|No| E[Option 2]
    D --> F[End]
    E --> F
```

## Direction Options

- `TD` or `TB` - Top to bottom (default)
- `BT` - Bottom to top
- `LR` - Left to right
- `RL` - Right to left

```mermaid
flowchart LR
    A --> B --> C
```

## Node Shapes

### Rectangle
```mermaid
flowchart TD
    A[This is a rectangle]
```

### Rounded Rectangle
```mermaid
flowchart TD
    B(This has rounded edges)
```

### Stadium Shape
```mermaid
flowchart TD
    C([This is a stadium shape])
```

### Subroutine
```mermaid
flowchart TD
    D[[This is a subroutine]]
```

### Database
```mermaid
flowchart TD
    E[(This is a database)]
```

### Circle
```mermaid
flowchart TD
    F((This is a circle))
```

### Diamond (Decision)
```mermaid
flowchart TD
    G{This is a decision}
```

### Hexagon
```mermaid
flowchart TD
    H{{This is a hexagon}}
```

### Parallelogram
```mermaid
flowchart TD
    I[/This is a parallelogram/]
    J[\This is a parallelogram alt\]
```

### Trapezoid
```mermaid
flowchart TD
    K[/This is a trapezoid\]
    L[\This is a trapezoid alt/]
```

## Arrow Types

### Solid Arrow
```mermaid
flowchart LR
    A --> B
```

### Dotted Arrow
```mermaid
flowchart LR
    A -.-> B
```

### Thick Arrow
```mermaid
flowchart LR
    A ==> B
```

### Line Without Arrow
```mermaid
flowchart LR
    A --- B
```

### Arrow with Text
```mermaid
flowchart LR
    A -->|Text on arrow| B
    C ---|Text on line| D
```

## Complete Example

```mermaid
flowchart TD
    Start([Start Process]) --> Input[/User Input/]
    Input --> Validate{Valid Data?}
    Validate -->|Yes| Process[Process Request]
    Validate -->|No| Error[Display Error]
    Error --> Input
    Process --> CheckDB{Record Exists?}
    CheckDB -->|Yes| Update[(Update Database)]
    CheckDB -->|No| Insert[(Insert into Database)]
    Update --> Success[/Show Success Message/]
    Insert --> Success
    Success --> End([End])
```

## Subgraphs

You can group nodes together:

```mermaid
flowchart TD
    A[Start] --> B[Process]
    
    subgraph Processing
        B --> C[Step 1]
        C --> D[Step 2]
    end
    
    D --> E[End]
```

## Styling

Add custom styles to nodes:

```mermaid
flowchart LR
    A[Normal] --> B[Highlighted]
    style B fill:#f9f,stroke:#333,stroke-width:4px
```

## Tips

- Use descriptive IDs (A, B, C or meaningful names)
- Keep diagrams simple and readable
- Use appropriate node shapes for different types of steps
- Add labels to decision branches for clarity
- Group related processes using subgraphs