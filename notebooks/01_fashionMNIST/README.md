# Fashion MNIST

* https://github.com/zalandoresearch/fashion-mnist

We are training our model with a bunch of closing pictures, to be able to categorize fashion items by their 28x28 pixel image.

## Network

We will create a Neural Network with 784 Inputs (28x28 Pixels), one hidden Layer with 100 Neurons (sigmoid) and 10 outputs (one for each category).

```mermaid
    %%{ init: { 'flowchart': { 'curve': 'linear', "defaultRenderer": "elk" } } }%%
    flowchart LR
        subgraph Network
            direction LR
            style Network fill:#f9f
            linkStyle default interpolate basis
            %%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
            I0 --> N0 & N1 & N98 & N99
            I1 --> N0 & N1 & N98 & N99
            I782 --> N0 & N1 & N98 & N99
            I783 --> N0 & N1 & N98 & N99
            subgraph Inputs
                direction TB
                I0((Input0));
                I1((Input1));
                I782((Input782));
                I783((Input783));
            end
            N0 --> O0 & O1 & O2 & O7 & O8 & O9
            N1 --> O0 & O1 & O2 & O7 & O8 & O9
            N98 --> O0 & O1 & O2 & O7 & O8 & O9
            N99 --> O0 & O1 & O2 & O7 & O8 & O9
            subgraph HiddenLayer
                direction TB
                N0([Neuron0]);
                N1([Neuron1]);
                N98([Neuron98]);
                N99([Neuron99]);
            end
            subgraph Outputs
                direction TB
                O0((Output0));
                O1((Output1));
                O2((Output2));
                O7((Output7));
                O8((Output8));
                O9((Output9));
            end
        end
```

(Chart is not optimal visiulized)

```mermaid
graph TD
    %% Input Layer
    subgraph Input Layer
        direction LR
        I1[Input 1]
        I2[Input 2]
        I3[Input 3]
        I4[...]
        I784[Input 784]
    end
    
    %% Hidden Layer
    subgraph Hidden Layer
        direction LR
        H1[Neuron 1]
        H2[Neuron 2]
        H3[Neuron 3]
        H4[...]
        H100[Neuron 100]
        style H1 fill:#f9f,stroke:#333,stroke-width:4px
    end
    
    %% Output Layer
    subgraph Output Layer
        direction LR
        O1[Output 1]
        O2[Output 2]
        O3[Output 3]
        O4[...]
        O10[Output 10]
        style O1 fill:#ff9,stroke:#333,stroke-width:4px
    end
    
    %% Connecting Input Layer to Hidden Layer
    I1 --> H1
    I1 --> H2
    I1 --> H3
    I1 --> H4
    I1 --> H100
    I2 --> H1
    I2 --> H2
    I2 --> H3
    I2 --> H4
    I2 --> H100
    I3 --> H1
    I3 --> H2
    I3 --> H3
    I3 --> H4
    I3 --> H100
    I4 --> H1
    I4 --> H2
    I4 --> H3
    I4 --> H4
    I4 --> H100
    I784 --> H1
    I784 --> H2
    I784 --> H3
    I784 --> H4
    I784 --> H100
    
    %% Connecting Hidden Layer to Output Layer
    H1 --> O1
    H1 --> O2
    H1 --> O3
    H1 --> O4
    H1 --> O10
    H2 --> O1
    H2 --> O2
    H2 --> O3
    H2 --> O4
    H2 --> O10
    H3 --> O1
    H3 --> O2
    H3 --> O3
    H3 --> O4
    H3 --> O10
    H4 --> O1
    H4 --> O2
    H4 --> O3
    H4 --> O4
    H4 --> O10
    H100 --> O1
    H100 --> O2
    H100 --> O3
    H100 --> O4
    H100 --> O10
```

## Dependencies

Install the dependencies by running 00_install_dependencies

## Load training data

### Labels
Each training and test example is assigned to one of the following labels:

| Label | Description |
| --- | --- |
| 0 | T-shirt/top |
| 1 | Trouser |
| 2 | Pullover |
| 3 | Dress |
| 4 | Coat |
| 5 | Sandal |
| 6 | Shirt |
| 7 | Sneaker |
| 8 | Bag |
| 9 | Ankle boot |
