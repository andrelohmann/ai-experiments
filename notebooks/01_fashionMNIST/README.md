# Fashion MNIST

* https://github.com/zalandoresearch/fashion-mnist

We are training our model with a bunch of closing pictures, to be able to categorize fashion items by their 28x28 pixel image.

## Network

We will create a Neural Network with 784 Inputs (28x28 Pixels), one hidden Layer with 100 Neurons (sigmoid) and 10 outputs (one for each category).

```mermaid
    %%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
    flowchart TD
        subgraph Network
            direction TB
            style Network fill:#f9f
            subgraph Inputs
                direction LR
                I1((Input1)):::round
                I2((Input2)):::round
                Ix((...)):::round
                I783((Input783)):::round
                I784((Input784)):::round
            end

            subgraph HiddenLayer
                direction LR
                N1([Neuron1]);
                N2([Neuron2]);
                Nx([...]);
                N99([Neuron99]);
                N100([Neuron100]);
            end

            subgraph Outputs
                direction LR
                O1((Output1)):::round
                O2((Output2)):::round
                Ox((...)):::round
                O9((Output9)):::round
                O10((Output10)):::round
            end

            I1 --> N1 & N2 & Nx & N99 & N100
            I2 --> N1 & N2 & Nx & N99 & N100
            Ix --> N1 & N2 & Nx & N99 & N100
            I783 --> N1 & N2 & Nx & N99 & N100
            I784 --> N1 & N2 & Nx & N99 & N100

            N1 --> O1 & O2 & Ox & O9 & O10
            N2 --> O1 & O2 & Ox & O9 & O10
            Nx --> O1 & O2 & Ox & O9 & O10
            N99 --> O1 & O2 & Ox & O9 & O10
            N100 --> O1 & O2 & Ox & O9 & O10

            classDef round padding:100px

        end
```

(Chart is not optimal visiulized)

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
