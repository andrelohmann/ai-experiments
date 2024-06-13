# General explanaition of a neuron

```mermaid
    %%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
    flowchart TD
        subgraph Network
            direction TB
            style Network fill:#f9f
            subgraph Inputs
                direction LR
                I1((X1))
                I2((X2))
                I3((X3))
            end

            subgraph Neuron
                direction TD
                N1([Neuron])
                O((y))
            end

            I1 -- w1 --> N1
            I2 -- w2 --> N1
            I3 -- w3 --> N1

            N1 --> O

        end
```

([better visualize with other tools](https://github.com/ashishpatel26/Tools-to-Design-or-Visualize-Architecture-of-Neural-Network))
