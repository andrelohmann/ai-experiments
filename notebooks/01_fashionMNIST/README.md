# Fashion MNIST

* https://github.com/zalandoresearch/fashion-mnist

We are training our model with a bunch of closing pictures, to be able to categorize fashion items by their 28x28 pixel image.

## Network

We will create a Neural Network with 784 Inputs (28x28 Pixels), one hidden Layer with 100 Neurons (sigmoid) and 10 outputs (one for each category).

```mermaid
    graph LR;
        subgraph Network
            direction LR
            style Network fill:#f9f

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
