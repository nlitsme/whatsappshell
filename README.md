# mdtest

Based upon the mdtest tool previously part of [whatsmeow](https://github.com/tulir/whatsmeow).

mdtest was deleted from the whatsmeow project in commit 9bd3fa0cc1c1a56c4e1ea324883b876c2c008c84

mdtest is a tool which connects to whatsapp using whatsmeow, and allows you to send most protocol messages
from an interactive shell.


## extensions

more commands:
 * a `help` command
 * a `jsonadd` command, which creates groups based on the specification in a json file.
 * a `addgroup` command, which creates a group specified on the cmdline.
 * `jsonadd` and `addgroup` also take care of inviting JIDS which fail the automatic add.
 * `checkuser` prints some more info for each jid checked.
 * `subscribepresence` is a bit more verbose.
 * corrected some typo's

other features:
 * all incoming images and videos are saved
 * the filename for images and video's contain the current time.

## Building

1. Clone the repository.
2. Run `go build` inside this directory.
3. Run `./mdtest` to start the program. Optionally, use `rlwrap ./mdtest` to get a nicer prompt.
   Add `-debug` if you want to see the raw data being sent/received.
4. On the first run, scan the QR code. On future runs, the program will remember you (unless `mdtest.db` is deleted). 

New messages will be automatically logged. To send a message, use `send <jid> <message>`


## Authors

 * The above extensions were added by Willem Hengeveld <itsme@xs4all.nl>
 * The main body of the mdtest tool was written by the [whatsmeow](https://github.com/tulir/whatsmeow) team.


