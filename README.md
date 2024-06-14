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
<p> Let us create our project structure by initializing a directory called <code>kafka-consumer-application</code> and moving into it.
> mkdir kafka-consumer-application && cd kafka-consumer-application
 <br></p> <br>

<p> To achieve that head over to the Environments section, select yours and go through the cluster creation steps.  </p> <br>

<p>Moving on let us create our project structure, we will interact with the terminal by issuing a few commands which will be explained as we move forward:
<ol>
  <li>Create a directory to store our project by running <code>mkdir kafka-consumer-application</code></li>
  <li>Next move into the above created directory by running <code>cd kafka-consumer-application</code></li>
  <li>Now that we are inside our main directory and we will create a new directory by running <code>mkdir configuration</code></li>
</ol>  
</p> <br>

<p>
Fom within Confluent Cloud navigate to the kafka previously created and perform the below tasks:
<ol>
  <li>Clients from the left hand navigation pannel</li>
  <li>Select New Client</li>
  <li>Choose Java</li>
  <li>Give your topic a name</li>
  <li>Download the kafka API key, copy the configuraton file generated right next to it and paste in a file called <code>ccloud.properties</code> inside the configuration directory created earlier.</li>
</ol>  
</p>

### Download and set up the Confluent CLI
<p>
In order to download the Confluent CLI the easiest option is to use Homebrew as it simplifies software installation.

From the terminal run <code> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" </code>

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


