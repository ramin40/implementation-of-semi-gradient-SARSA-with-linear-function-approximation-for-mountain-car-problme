# implementation-of-semi-gradient-SARSA-with-linear-function-approximation-for-mountain-car-problme
this repository contains python code implementation of the semi-gradient SARSA algorithm using tilecoding and function approximation for the mountain car problem. I've created this repository for educational purposes and you can use, change or modify it.

<img src='https://user-images.githubusercontent.com/74808396/187072684-8a9244ea-6860-4514-b9f0-d1c71f05e4e9.png' width='400' height='200'>

# SARSA with function approximation
SASA is a model-free algorithm that estimates action state value using temporal difference learning. we can use SARSA with tabular or function approximation methods.
in tabular  SARSA  each state-action pair have an entry. this method theoretically is good but in large environments or environments with continuous action has no practical use. a replacement for tabular SARSA is function approximation with the function approximation method you represent each state or each state-action pair with some numerical features and calculate action state value function with matrix multiplication of the represented features and a learnable matrix named weight matrix then using gradient descent to update parameters of the value function (weight matrix).
this was brief introduction to SARSA with linear function approximation you can read chaptert 10 of [Barto's RL book]('http://incompleteideas.net/book/the-book.html'). 

# environment
<img src='https://user-images.githubusercontent.com/74808396/187074307-d9356789-3b88-425f-8467-2583de6612c9.png' width='400' height='200'>
our agent is in a valley, its goal is to reach out to the tip of the right mountain of its location. state of the agent determined by two scaler values consisting of velocity and location of agent on the X axis. in each state, the agent has three possible actions that are moving right, left, and no action.

# tile coding 
<img src='https://user-images.githubusercontent.com/74808396/187074704-432acfac-53d1-4f38-9328-a1811ab4ae41.png' width='400' height='300'>

as I mentioned for using function approximation we have to represent our state with some numerical featuers. for mountain car problem we represent our satates with tile coding method. tile coding coonverts each state to a binary vector. I've used python code implemented in [this repository](https://github.com/MeepMoop/tilecoding) by [MeepMoop](https://github.com/MeepMoop) for tile coding.

# how to run code
- clone [this repository](https://github.com/MeepMoop/tilecoding).
- run `semi-gradient sarsa` notebook.
- have fun 😉
