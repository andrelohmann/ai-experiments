# Fashion MNIST single output

* https://github.com/zalandoresearch/fashion-mnist

We are training our model with a bunch of closing pictures, to be able to categorize fashion items by their 28x28 pixel image.

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

## Dependencies

Install the dependencies by running 00_install_dependencies

## Load training data

Load the training by running 01_load_training_data

## Network

### T-Shirt or not T-Shirt

We will create a first Neural Network with 784 Inputs (28x28 Pixels), one hidden Layer with 100 Neurons (sigmoid) and 1 output Neuron. The network will be simplified to only learn if an image is a t-shirt or not.

```mermaid
    %%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
    flowchart TD
        subgraph Network
            direction TB
            style Network fill:#f9f
            subgraph Inputs
                direction LR
                I1((Input___1))
                I2((Input___2))
                Ix((___...___))
                I783((Input_783))
                I784((Input_784))
            end

            subgraph HiddenLayer
                direction LR
                N1([Neuron___1]);
                N2([Neuron___2]);
                Nx([____...___]);
                N99([Neuron__99]);
                N100([Neuron_100]);
            end

            subgraph Output
                direction TB
                ON([OutputNeuron])
                O((Output))
            end

            I1 --> N1 & N2 & Nx & N99 & N100
            I2 --> N1 & N2 & Nx & N99 & N100
            Ix --> N1 & N2 & Nx & N99 & N100
            I783 --> N1 & N2 & Nx & N99 & N100
            I784 --> N1 & N2 & Nx & N99 & N100

            N1 --> ON
            N2 --> ON
            Nx --> ON
            N99 --> ON
            N100 --> ON

            ON ---> O

            classDef round width:75px

        end
```

([better visualize with other tools](https://github.com/ashishpatel26/Tools-to-Design-or-Visualize-Architecture-of-Neural-Network))

### Run the network

Run the neural network by running 02_neural_network
