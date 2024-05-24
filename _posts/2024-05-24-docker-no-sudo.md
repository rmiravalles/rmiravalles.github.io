---
layout: post
title: "Running Docker commands without the sudo"
---
# Don't forget sudo!

This is going to be a super short one.

You may have noticed that all my Docker commands had the `sudo` in front of them. Without it, Docker would tell me I didn't have the permissions to run such commands. I had to remember to put the `sudo` in front of all the Docker commands all the time.

It happens to all of us. We keep forgetting to type `sudo`. It happens to me all the time. There's this super command, however, that always comes to my aid. It's arguably the most important command in Linux! I love it!

If you forget to write `sudo` in front of a command, and you get the *unauthorized* response, then you simply need to type this: `sudo !!`

This awesome command will execute that last thing you wrote in the terminal with `sudo` in front of it.

# Trust Docker

But that's not what I wanted to talk about.

Docker didn't trust me, and I had to type `sudo` all the time I had to run a Docker command. Not that it's too tragic, but I wanted to avoid it. [Nigel Poulton](https://nigelpoulton.com/), the famed Docker captain and Kubernetes helmsman enlightened me. I saw the way out in his **Docker Deep Dive** book. The solution is to add your user account to the **docker** Unix group.

I searched for this group in the `/etc/group` file and it wasn't there. I lost hope and thought that something was wrong, that the group wasn't there because of some serious and unsolvable problem. How stupid I was! We need to actually create this group!

This is how you create the `docker` group:

`sudo groupadd docker`

And this is how you add your own user to this group:

`sudo usermod -aG docker $USER`

The `usermod` command modifies the user account. The `-aG` flag is to add a user to a group. The `a` stands for **append**.

With that, the docker group is created and added to the `/etc/group` file.

You may need to restart the machine for the changes to take effect. I had to do it.

Here I am, inside the group.

![/etc/group](../assets/images/etcgroup.png)

And now I can run Docker commands without the need to type `sudo` and save a fraction of a second every time I do it!


