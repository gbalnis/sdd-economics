# Models

- Flow of work (closed-loop production system)
- Spec fidelity pipeline (information transformation)
- Resource allocation (capital / labor / tokens)
- Feedback control loop (learning + adaptation)

# Flow of Work
## Performance

Goal, Signal and Metrics:

What is the output of the system that we care about? Some combination of:
- speed
- quality
- predictability
- maintainability
- user satisfaction
- developer satisfaction
- cost (human effort + token consumption)
- capital

In a queuing network model of the flow watch for signals:
- Arrival rate
- Processing rate
- Work-in-progress
- Variability

## Derived Metrics
- Lead time = total latency (idea → value)
- Flow efficiency = active work / total time
- Queue accumulation = early signal of bottlenecks

# Spec Fidelity Pipeline
"Genius is one percent inspiration, ninety-nine percent perspiration." (Thomas Edison). Staff the one percent with humans and the ninety-nine percent with agents.

```text
Intent → Spec → Code → Behavior → Observed Outcome
```
Raw idea = high entropy (ambiguous)
Spec = reduced entropy (structured intent)
Code = low entropy (executable artifact)

- Information transformation from high-level intent to low-level executable artifacts.
- Fidelity levels: Conceptual → Logical → Physical
- Each transformation step can be manual, automated deterministically, or agent-assisted, or any mix thereof. The higher the entropy, the more likely it is to require human judgment and creativity, while lower-entropy steps are more amenable to automation.
- Tradeoffs between fidelity levels: higher fidelity can improve execution accuracy but may increase upfront effort and reduce flexibility.

# Resource Allocation
## Production function
Cobb-Douglas production function for SSD:

```text
Output = A * Labor^alpha * Capital^beta * Tokens^gamma
```
Where:
- A = Total Factor Productivity (technology, processes, culture)
- alpha = labour elasticity of output
- beta = capital elasticity of output
- gamma = token elasticity of output
- Diminishing returns: as we allocate more resources to one factor, the incremental output may decrease, especially if other factors are not scaled accordingly.
- Substitution effect: under certain conditions, we can substitute human effort with agent effort or tokens, but the effectiveness of substitution depends on the specific task and context.

## Theory of the Firm and Software Engineering
Software engineering presents unique challenges for human cognitive capabilities. It doesn't scale well with human labor alone due to the complexity and variability of software systems. This is where team production comes into play.
Some engineers propose that with the emergence of agentic workflows this dynamic is changing, and that software engineering can now scale mainly with token consumption. The individual becomes "the firm" and engages in market transactions on their own.

Indeed, TFP is the only reason for firm existence in the long run. We need to understand how to optimize TFP in the context of agentic software engineering, which includes organizational design, process optimization, and technology adoption. In simple terms: what it is about the firm that makes the production function more efficient, other inputs being equal?

# Feedback Control Loop
```text
Observe → Hypothesize → Change → Measure → Learn
```

- performance signals
  - lead time
  - deployment frequency
  - defect escape rate
  - rework ratio

- spec signals
  - spec churn rate
  - spec → code delta
  - clarification requests per cycle

- resource efficiency signals
  - labor hours per value unit
  - token usage per value unit
  - automation coverage