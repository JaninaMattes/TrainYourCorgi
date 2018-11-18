# Train Your Corgi

This project aims to explore _reinforcement learning_ as a strategy to guide an ml-agent in a mixed reality application. Mixed reality applications allow virtual content to interact with an environment as detected by sensors, such as a smartphone camera. This poses the challenge of finding algorithms that can cope with a variety of uncontrollable environments. Machine learning gives here a way to adapt and overcome this challenge. In this project reinforcement learning is used to provide the framework for defining the behavior of a Non-Player-Character. The NPC can be trained by providing it with rewards when it achives the desired goal and completes a task correctly. This is showcased by a mixed reality mobile game for Android where a user can play fetch with a dog in a virtual scene placed on a real world environment. 

### Introduction

Augmented reality detects the environment and extracts its features from sensor data. Most commonly, camera data is used and the detected features, such as floor, ceiling and obstacles used to form an environment for the virtual content. In this project we will showcase the approach of modelling agents, which are bound into a virtual environment by Mesh.Bounds within a real environment. 

### Selecting reinforcement learning as the machine learning paradigmn

Three main paradigms exist in machine learning: _Supervised learning_, _unsupervised learning_ and _reinforcement learning_. _Supervised learning_ uses labeled datasets to learn. Although it is the most commonly studied kind of machine learning in current research, it is not suitable for learning from interaction. Whilst _Unsupervised learning_ has the advantage of not relying on examples of correct behaviour. Although identifying uncovering structure in an agent’s experience can certainly be useful but it does not address the problem of maximizing a reward signal by itself. In _reinforcement learning_, the system is only given a reward function. By showing different behaviours, it is either rewarded or punished, depending on the outcome.

### Game structure and interaction

An agent, represented by a gameobject, in this case a corgi dog model is placed onto a virtual scene in a real environment. The interaction between user and the pre-trained model contains that a user can play fetch with a dog in a virtual scene. The user can start the game by throwing a stick to the dog and swiping on the screen. The dog then finds the target object and throws it back. Further the dogs motion is iself driven by the physics engine. This means for instance that the motion of the corgi can be affected by surrounding RigidBodies. The trained gameobject learns to walk, run, jump and fetch the stick using reinforcement learning.

The images below demo the game in action:

![TrainYourCorgi](TraingYourCorgi1.jpg)

![TrainYourCorgi](TraingYourCorgi2.jpg)

### Implementation and prerequisites

The application is delivered as an Android app. The app itself is created in Unity game engine with the _MLAgents plugin_ as a central framework, _TensorFlow_ and _Python_ as a machine learning API and Google’s AR Core for environment scanning and interpretation. It combines an ARCore and MlAgent and compiles and deploys to Android. Multiple scenes need to be brought to one scene and the agent's brain is trained. Another solution would be to import the brain from another trained agent. This is also added to the ARScene.

#### Modelling the environment with ARCore

ARCore is Google’s framework for augmented reality. Programming against this API enables us to easily extract terrain features such as obstacles from the camera stream.

See further information under [ARCore Overview](https://developers.google.com/ar/discover/)

#### Unity Machine Learning Agents Toolkit
The Unity Machine Learning Agents Toolkit (ML-Agents) is an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents. Agents can be trained using reinforcement learning, imitation learning, neuroevolution, or other machine learning methods through a simple-to-use Python API. 

See further information under [Unity Machine Learning Agents Toolkit](https://github.com/Unity-Technologies/ml-agents)

#### Using TensorFlow and Python for reinforcement learning

TensorFlow is Google’s primary machine learning framework. We use the Python interface provided by the MLAgents framework to train agents with reinforcement learning.

## Deployment


## Built With

* [Unity](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [ARCore](https://maven.apache.org/) - Dependency Management
* [Tensorflow](https://rometools.github.io/rome/) - Used to generate RSS Feeds
* [Python](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

## Versioning

## Authors

* **Max Mustermann** - *Initial work* - [Puppo The Corgi](https://github.com/)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Inspiration
* Inspiration
* Inspiration
