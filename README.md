# Talos

Script to check hardware health and system stats

This script is self-deleting, make sure to move it out of the directory you are modifying it in before you execute it, or you will lose all changes.
The byte size and checksum fields in the header must be updated before you run it, or it will stop the execution the main function.

To update the byte size field run the following command:

wc -c Talos_*.bash

To verify or update the checksum field run the following command after updating the byte size: 

sed -e 's/\(Checksum: \).*\(File name: \).*\(.bash\)/\1\2\3/' Talos_*.bash | md5sum
