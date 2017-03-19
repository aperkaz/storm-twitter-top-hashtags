# Twitter Top Hashtags

Stream processing pipeline that performs the real time analysis of top hashtags on Twitter.

This following repo contains the Storm topology code and the instructions to run it locally with [Local Mode](http://storm.apache.org/releases/0.10.0/Local-mode.html). This simulates the behavior of the topology as it was deployed into a cluster.

## Requirements

  * [Vagrant](https://www.vagrantup.com/) - virtual environment manager.
  * [Oracle VM VirtualBox](https://www.virtualbox.org/) - general purpose virtualizer .
  * SSH client, such as [PuTTY](http://www.putty.org/).

## Getting Started

  1. `git clone https://github.com/aperkaz/storm-twitter-top-hashtags.git`
  2. `cd /storm-twitter-top.hashtags`
  3. `vagrant up`
  4. Using SSH client, SSH `127.0.0.1:2222`
  4.1 Log in `vagrant:vagrant`
  5.