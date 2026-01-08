# Formatting-Test

flowchart TD
  A((Start)) --> B[/Input N/]
  B --> C{Is N > 0?}
  C -- No --> D[/Output: "N must be positive"/] --> Z((End))

  C -- Yes --> E[Process: i=1, odd_sum=0, even_sum=0]
  E --> F{Is i <= N?}
  F -- No --> G[/Output: odd_sum, even_sum/] --> Z((End))

  F -- Yes --> H{Is i even? (i % 2 == 0)}
  H -- Yes --> I[Process: even_sum += i]
  H -- No --> J[Process: odd_sum += i]

  I --> K[Process: i = i + 1]
  J --> K
  K --> F
