README.md

### :rotating_light: Building a very basic consumer application that reads records from Kafka :rotating_light:

## Table of contents
1. [Project Structure](#project-structure)
2. [Download and set up the Confluent CLI](#download-and-set-up-the-confluent-cli) 
3. [Connect to your cluster](#connect-to-your-cluster) 
4. [Configuring the project](#configuring-the-project) 
5. [Unix Commands Reference table](#unix-commands-reference-table)

---

### Project Structure
<p> Let us create our project structure by initializing a directory called <code>kafka-consumer-application</code> and moving into it.<br> <p></p> Run the following command: <code> mkdir kafka-consumer-application && cd kafka-consumer-application </code> </p>

<p>Copy the cluster information and paste in a file called <code>ccloud.properties</code> inside the configuration folder.</p>

<p>
By now we should have the following structure:

> └── configuration
> <br> &nbsp;&nbsp;&nbsp;&nbsp;    └── ccloud.properties
</p>

### Download and set up the Confluent CLI
<p>
To install Confluent CLI run the following command <code>brew install confluentinc/tap/cli</code>

<p>If you don't have Homebrew already installed you can do so by going here https://brew.sh/ . </p>
</p>

### Connect to your cluster

Let us connect to our Confluent Cloud by running <code>confluent login --save</code> the <code>-- save</code> is just a flag and will save your credentials and log you back in if session expires.

We are now connected and in order to view a list of active environments run <code>confluent environment list</code>.

Select the environment by running <code>confluent environment use `<env-id>` </code>.

Get the cluster ID previously created at the beginning of the lab by running <code>confluent kafka cluster list</code>.

Select the appropriate cluster by running <code> confluent kafka cluster use `<cluster-id>` </code> .

If you created your API key using the CLI on another machine or using the UI you need to store it by runnig <code>api-key store `<api-key>` `<api-secret>` --resource `<resource-id>`</code> 

If by any chance one was already stored previously we need to ooverride it by using the <code>--force</code> flag at the end of your command <code>api-key store `<api-key>` `<api-secret>` --resource `<resource-id>` `--force`</code> .

Finnaly set API key to use by running <code>confluent api-key use `<api-key>` </code> and you can now run the Confluent CLI commands against the specified cluster.

</p>

### Creating a topic
<p>
If you already have a topic already created you can view it by running <code>confluent kafka topic list</code> .
</p>

### Configuring the project
<p>
Create the following file <code>build.gradle</code> inside the root of your directory.

So by now we should have the following structure:
> ├── build.gradle
> ├── configuration
> <br> &nbsp;&nbsp;&nbsp;&nbsp;│   └── ccloud.properties
> ├── gradle
> <br> &nbsp;&nbsp;&nbsp;&nbsp;│   └── wrapper
> <br> &nbsp;&nbsp;&nbsp;&nbsp;│       ├── gradle-wrapper.jar
> <br> &nbsp;&nbsp;&nbsp;&nbsp;│       └── gradle-wrapper.properties
> ├── gradlew
> └── gradlew.bat

</p>






### Unix Commands Reference table

| Unix Command| Description |
| ----------- | ----------- |
| <code>mkdir</code>       | This command is used to create a new directory|
| <code>cd</code>   | This command is used to change to a directory        |
| <code>touch</code>   | This command is used to create an empty file        |


