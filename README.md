# Twitter Top Hashtags

Stream processing pipeline that performs the real time analysis of top hashtags on Twitter, using [Apache Storm](http://storm.apache.org/).

This following repo contains the Storm topology code and the instructions to run it locally with [Local Mode](http://storm.apache.org/releases/0.10.0/Local-mode.html). This simulates the behavior of the topology as it was deployed into a cluster.

## Requirements

  * [Vagrant](https://www.vagrantup.com/) - virtual environment manager.
  * [Oracle VM VirtualBox](https://www.virtualbox.org/) - general purpose virtualizer .
  * SSH client, such as [PuTTY](http://www.putty.org/).

## Getting Started

  1. `git clone https://github.com/aperkaz/storm-twitter-top-hashtags.git`
  2. `cd /storm-twitter-top-hashtags`
  3. Spin up the VM: `vagrant up`
  4. Using SSH client, SSH `127.0.0.1:2222` <br/>
  4.1. Log in `vagrant:vagrant`
  5. Run the visualization web server <br/>
  5.1. Inside the VM: `cd /vagrant/visualization`<br/>
  5.2. `python app.py`
  6. Package the topology <br/>
  6.1. Inside the VM (open new SSH session): `cd /vagrant/topology` <br/>
  6.2. `mvn clean`<br/>
  6.3. `mvn package` - may take a while the first time.<br/>
  7. Execute the packaged topology <br/>
  7.1. Inside the VM: `cd /vagrant/topology` <br/>
  7.2. `storm jar target/storm-twitter-top-hashtags-0.0.1-SNAPSHOT-jar-with-dependencies.jar storm.TopNTweetTopology`
  8. Live generated results at `http://127.0.0.1:5000`.
