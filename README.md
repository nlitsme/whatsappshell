# mdtest

Based upon the tool previously part of whatsmeow.

mdtest was deleted from the whatsmeow project in commit 9bd3fa0cc1c1a56c4e1ea324883b876c2c008c84

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
 * video's are also saved
 * the filename for images and video's now contains the current time.

## Building

1. Clone the repository.
2. Run `go build` inside this directory.
3. Run `./mdtest` to start the program. Optionally, use `rlwrap ./mdtest` to get a nicer prompt.
   Add `-debug` if you want to see the raw data being sent/received.
4. On the first run, scan the QR code. On future runs, the program will remember you (unless `mdtest.db` is deleted). 

New messages will be automatically logged. To send a message, use `send <jid> <message>`
