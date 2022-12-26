# CTF Starter
A template for deploying challenges to ACM Cyber's [CTF platform](https://github.com/uclaacm/cyber-platform) for Cyber Academy &amp; CTF After Dark. For more information, please see [https://github.com/uclaacm/cyber-platform](https://github.com/uclaacm/cyber-platform).

## Deploying
In order to begin deploying this to the ACM Cyber platform, start by updating ```ctf.toml```. Notice the example fields below.

```
start = 2022-05-18T18:00:00-06:00
stop = 2022-05-25T18:00:00-06:00
```

These indicate the starting and stopping time of the CTF. The platform will not accept flags if the stop time has passed so its important to update this. Be sure to match the correct formatting of the times (here is a resource that can help [convert times](http://www.timestamp-converter.com/)).

Once this is updated, make sure that all of the events and challenges within their corresponding folders pass the TOML checker. With that, you are ready to deploy the [platform](https://github.com/uclaacm/cyber-platform)!

## Challenges
Follow the format of the ```challenges/example/challenge.toml``` to create a challenge!

### Creating Challenges
Each challenge should correspond to a directory within the `challenges/` directory. Make sure to push both source and compiled Linux executable. Also check that the executable runs on the SEASnet servers.

Regarding `challenge.toml`, follow this [example](https://github.com/uclaacm/cyber-academy-s20/blob/update_main/encompress/challenge.toml). Some things to keep in mind:
* Aim for `value` to range between 10 and 100.
* If you're presenting the next week, set `enabled` to true; otherwise, false.
* Your first tag should signify which workshop the challenge comes from. For example, "file" for File Analysis, "packet" for Packet Captures, "memory" for Memory Forensics.
* `files` should contain relative paths, `description` should link by filename.

## Events
Follow the format of the ```events/example/events.toml``` file to create an event!

### Event Creation
Each event should correspond to a directory within the `events/` directory. Make sure to include an ```icon.svg``` within every event folder!

Regarding `event.toml`, follow this [example](https://github.com/uclaacm/cyber-academy-s22/blob/main/events/boba-run/event.toml).

## Credits
This template is maintained by ACM Cyber at UCLA. Please contact uclacyber@gmail.com for any concerns or simple create an issue on this repository.
