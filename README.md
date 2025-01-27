# buzzline-02-stonerogers
Streaming Data, Project 2
Melissa Stone Rogers, [GitHub](https://github.com/meldstonerogers/buzzline-02-stonerogers)

## Introduction

This is a professional project using Apache Kafka, Python Version 3.11, and Git for version control. We will write producers to send data to topics, and also write consumers to read from those topics.
This project was forked from Dr. Case's project repository found [here](https://github.com/denisecase/buzzline-02-case). Much of the detailed instructions in this README.md were borrowed from Dr. Case's project specifications, and updated for my machine.
Commands were used on a Mac machine running zsh.   

## Task 1. Install and Start Kafka (using WSL if Windows)

Before starting, ensure you have first completed the setup tasks in Dr. Case's introductory [repository](https://github.com/denisecase/buzzline-01-case) on this topic. 
Python 3.11 is required. 

In this task, we will download, install, configure, and start a local Kafka service. 

1. Install Windows Subsystem for Linux (Windows machines only)
2. Install Kafka Streaming Platform
3. Start the Zookeeper service (leave the terminal open).
4. Start the Kafka service (leave the terminal open).

For detailed instructions, see:

- [SETUP-KAFKA](docs/SETUP-KAFKA.md) (all machines)


## Task 2. Copy This Example Project & Rename

Copy/fork this project into your GitHub account and create your own version of this project to run and experiment with. 
Name it `buzzline-02-yourname` where yourname is something unique to you.
Follow the instructions in [FORK-THIS-REPO.md](https://github.com/denisecase/buzzline-01-case/blob/main/docs/FORK-THIS-REPO.md).
    

## Task 3. Manage Local Project Virtual Environment

Follow the instructions in [MANAGE-VENV.md](https://github.com/denisecase/buzzline-01-case/blob/main/docs/MANAGE-VENV.md) to:
1. Create your .venv
2. Activate .venv
3. Install the required dependencies using requirements.txt.

### Initial Project Commit 
Turn on the autosave function in VS Code. Push changes to GitHub freqently to effectively track changes. Update the commit message to a meaningful note for your changes. 
```zsh
git add .
git commit -m "initial"                         
git push origin main
```

## Task 4. Start a Kafka Producer

Producers generate streaming data for our topics.

In VS Code, open a terminal.
Use the commands below to activate .venv, and start the producer. 

```zsh
source .venv/bin/activate
python3 -m producers.kafka_producer_stonerogers
```

## Task 5. Start a Kafka Consumer

Consumers process data from topics or logs in real time.

In VS Code, open a NEW terminal in your root project folder. 
Use the commands below to activate .venv, and start the consumer. 

```zsh
source .venv/bin/activate
python3 -m consumers.kafka_consumer_stonerogers
```

## Customize Your Producer and Consumer Files 

Modify the Kafka producer file to produce custom messages, and then also customize you consumer file. For this project, I utilized [OpenWeather API](https://openweathermap.org/api) to request real-time data to write events to Kafka. I then adjusted the consumer file to ensure the consumer can receive messages related to the noted topic. 

## Later Work Sessions
When resuming work on this project:
1. Open the folder in VS Code. 
2. Start the Zookeeper service.
3. Start the Kafka service.
4. Activate your local project virtual environment (.env).

## Save Space
To save disk space, you can delete the .venv folder when not actively working on this project.
You can always recreate it, activate it, and reinstall the necessary packages later. 
Managing Python virtual environments is a valuable skill. 

## Complete Your Project
Save your project and push back to your repository. 
```zsh
git add .
git commit -m "final"                         
git push origin main
```

## License
This project is licensed under the MIT License as an example project. 
You are encouraged to fork, copy, explore, and modify the code as you like. 
See the [LICENSE](LICENSE.txt) file for more.
