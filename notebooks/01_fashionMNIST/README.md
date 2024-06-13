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
                I1((Input___1)):::round
                I2((Input___2)):::round
                Ix((___...___)):::round
                I783((Input_783)):::round
                I784((Input_784)):::round
            end

            subgraph HiddenLayer
                direction LR
                N1([Neuron___1]);
                N2([Neuron___2]);
                Nx([____...___]);
                N99([Neuron__99]);
                N100([Neuron_100]);
            end

            subgraph Outputs
                direction LR
                O1((Output__1)):::round
                O2((Output__2)):::round
                Ox((___...___)):::round
                O9((Output__9)):::round
                O10((Output_10)):::round
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

            classDef round width:75px

        end
```

([better visualize with other tools](https://github.com/ashishpatel26/Tools-to-Design-or-Visualize-Architecture-of-Neural-Network))

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
