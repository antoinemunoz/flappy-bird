# [PYTORCH] Deep Q-learning for playing Flappy Bird

## how it work

so you can train you model

the training logic is quite simple, i m using deep q learning, with some cool stuff fpr exemple

Action Selection: Implements epsilon-greedy strategy for action selection (exploration vs exploitation).
Environment Interaction: Performs an action in the game environment and observes the reward and next state.
Memory Update: Stores the transition in replay memory and removes old memories if the memory size exceeds the limit.
Sample Batch from Replay Memory: Randomly samples a batch of experiences for training.
Compute Target Q-Values: For each sampled experience, calculates the target Q-value using the Bellman equation.
Model Update: Performs a gradient descent step to update the model's weights.

this is simply my main boucle of training, for the structure of the model i simply do this
self.conv1, self.conv2, self.conv3: These are convolutional layers (nn.Conv2d) designed to process 2D data (like images). Convolutional layers are effective in extracting features from images. Each layer is followed by a ReLU activation function (nn.ReLU) which introduces non-linearity, allowing the network to learn complex patterns.
self.fc1, self.fc2: These are fully connected (or linear) layers (nn.Linear). After convolutional layers extract features, these layers are used for final decision making or regression tasks. The first linear layer reduces the dimensionality to 512, and the second to 2, which could be the number of actions in a reinforcement learning environment.

in resume, i choose a structure who are optimized for image processing, and i use a convolutional layer for extract feature from the image, and i use a linear layer for the final decision making, plus i use non linear function for the activation function, and i use a relu function for the activation function, because it's the best for image processing

## Requirements

* **python 3.6**
* **pygame**
* **cv2**
* **pytorch**
* **numpy**
