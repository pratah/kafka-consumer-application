README.md

### :rotating_light: Building a very basic consumer application that reads records from Kafka :rotating_light:

## Table of contents
1. [Project Structure](#project-structure)
2. [Download and set up the Confluent CLI](#download-and-set-up-the-confluent-cli) 
3. [Creating a topic](#creating-a-topic) 
4. [Adding Graddle](#adding-graddle) 
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

<p>If you don't have Homebrew already installed you can do so by going here </p>[Homebrew](https://brew.sh/)


If you are using Apple designed chips you may be require to add Homebrew to your <code>$PATH</code> and to do so type <code>vim .bash_profile</code> and add the lines given to you at the end of the installation process.

Install Confluent CLI by running <code>brew install confluentinc/tap/cli</code> and confirm if the installation was successful by running <code>confluent --version</code>, you should get something like <code>confluent version v3.64.0</code> as an output.
</p>

<p>
Let us connect to our Confluent Cloud by running <code>confluent login --save</code> the <code>-- save</code> is just a flag and will save your credentials and log you back in if session expires.

We are now connected and in order to view a list of active environments run <code>confluent environment list</code>.

Select our environment by running <code>confluent environment use `<env-id>` </code>.

Get the cluster ID previously created at the beginning of the lab by running <code>confluent kafka cluster list</code>
Do not create another API key as we cannot override the one we created when we first instantiated our cluster.
</p>

### Creating a topic



### Adding Graddle






### Unix Commands Reference table

| Unix Command| Description |
| ----------- | ----------- |
| <code>mkdir</code>       | This command is used to create a new directory|
| <code>cd</code>   | This command is used to change to a directory        |
| <code>touch</code>   | This command is used to create an empty file        |


