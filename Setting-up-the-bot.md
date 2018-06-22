The bot consists of three components:

* Java/Kotlin bot
* Python neural network
* Python bot

The python bot isn't maintained. The Python neural network requires Python dependencies as per `requirements.txt`, and the Java/Kotlin bot has its dependencies defined in the build system (you don't need to download anything for the Java bot; Gradle does it automatically).

# Using the Java/Kotlin bot

The Java/Kotlin bot interfaces with the neural network, but isn't dependent on it. Pinging attempts to connect to the neural network, and returns a default "How can I help?" response including the defined trigger. `bot.properties` and `creds.properties` are the two files you need to change. Rename (while keeping the original if you intend to commit to Git) `creds.properties-example` to `creds.properties` and fill in the necessary values. They're documented, and if you don't fill all the necessary ones for a specific site, that site won't boot. Same with `bot.properties-example` - rename them and keep the original `bot.properties-example` around.
 
You can also disable sites by removing them from bot.properties.

If you plan on deploying, you'll need to run a gradle command. You don't need to boot an IDE, the wrapper is included in the project. CD into `/chatbot` (the location of the Gradle wrapper). Run `gradlew fatJar`. This will build a jar that will end up in `/chatbot/build/libs`, with all the dependencies. Note that the property files and the database is not a part of the jar. These are external.

# Using the neural net

The [Corell Movie Dialog Corpus](http://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) is the dataset the bot is designed for at the moment. There will be support for custom dataset (and conversation scrapping for personalized conversations), but that's an issue for later.

## Setup


The [Cornell Movie Dialog Corpus](http://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) is the dataset the bot is designed for at the moment. There will be support for custom dataset (and conversation scraping for personalized conversations), but that's an issue for later.

The text files in the cornell movie dialog corpus goes in a directory called `raw_data`. 

Rename `Config.py_example` to `Config.py` and fill in the necessary values. The bot is designed to run on all three sites, in addition to in the console, so there is currently no system to handle missing sites. You can of course run it in the console and not deal with websites and API's.

And finally, when all the data is added, run `bot.py`. It'll set up the necessary files and start training once it's done. Checkpoints are saved every epoch (and it overrides the past save).

## Training

CD into the root directory of the project. **Do not CD into `/Network`**. Run `python Network/bot.py --training true`.

## Using

### Command line

In the same directory as in the training step, run `python Network/bot.py --training false --mode 0`.

### Python chatbot

Note that the Python chatbot isn't maintained.

Run `python Network/bot.py --training false --mode 1`

### Flask server (for interaction with the Java bot or another bot)

Run `python Network/bot.py --training false --mode 2`. It'll take a while to come fully online. 