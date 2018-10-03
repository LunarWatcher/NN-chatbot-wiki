## Operating System Compatibility
NN-chatbot is built in Java and Python with no specific  operating system (OS) formatting. The program is designed to be universally compatible with any OS platform, but has only been validated in Windows.

Volunteers interested in OS platform validation are needed and appreciated! Review the contribution guidelines in the CONTRIBUTING.md file. To report compatibility errors, open an issue on the NN-Chatbot Github page [here](https://github.com/LunarWatcher/NN-chatbot/issues).

## Chatbot Prerequisites
Click on the program name to be redirected to the respective download/installation page.

#### [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* Git must be available from a command prompt for the revision command to work.
* Recommended: Install and add Git to the PATH environment variable.

#### [Gradle](https://gradle.org/install/)
* This is the build tool designed to automate the build process and support multi-language development.
* See the [Gradle Github page](https://github.com/gradle/gradle) or the [Gradle website](https://gradle.org) for more details.

#### [IntelliJ](https://www.jetbrains.com/idea/download/#section=windows)
* Supports Python editing with the [Python plugin](https://www.jetbrains.com/help/idea/plugin-overview.html).
* IntelliJ IDEA projects can be synchronized with Gradle projects, and IntelliJ IDEA can configure a Gradle composite build. For more information, click [here](https://www.jetbrains.com/help/idea/gradle.html).
* **NOTE:** [PyCharm](https://www.jetbrains.com/pycharm/download/#section=windows) is a viable alternative to IntelliJ if the Java port is not used, but it cannot synchronize with Gradle. Also, the Python plugin for IntelliJ IDEA has the same functionality as the community edition of PyCharm, so it is possible to continue working from IntelliJ even without the Java port. This is why using IntelliJ in conjunction with Gradle is preferable.

#### [Python 3.6+](https://www.python.org/downloads/) ####
* **NOTE:** Python 3.6+ is only necessary if the NN module/Python bot is used.

#### [Java 10](http://jdk.java.net/10/)
* **NOTE:** Java 10 is only necessary if the Java port is used. The project builds around OpenJDK. 



## Clone the Repository
#### Clone by Command Prompt
Use the command prompt to clone the repository and cd into the NN-chatbot directory.
```
git clone https://github.com/LunarWatcher/NN-chatbot.git
cd NN-chatbot
```
## Dependencies

```
discord.py
numpy
tensorlayer
tensorflow
sklearn
tensorboard
asyncio
nltk
```

**NOTE:** TensorLayer has several prerequisites which may require the `pip install` command to complete installation of all dependencies.
* See the TensorLayer [official installation guide](http://tensorlayer.readthedocs.io/en/latest/user/installation.html) for details.

**NOTE:** There are two versions of TensorFlow: TensorFlow with CPU support only and TensorFlow with GPU support (aka: tensorflow-gpu). TensorFlow with GPU support is better suited for neural networks and/or machine learning, but both versions are acceptable.
* See the TensorFlow [official installation guide](https://www.tensorflow.org/install/) for details.

## Dataset

The [Cornell Movie-Dialogs Corpus](http://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html)
* Download the ZIP file and extract the dialogue text files into the `raw_data` directory. The directory does into the project root. 

## Ready?
Once all programs/dependencies are downloaded and installed, proceed to the bot setup.
<!--Unsure if they should be redirected to the Setting-up-the-bot wiki page or the Readme. Add a link later.-->
