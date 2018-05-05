# HideText
Encodes visible text in invisble zero-width unicode characters. Append the secret data to a message and send it away. Decode it using same tool.
There are two tools provided. The second one is more complex and allows for more messages to be sent through text, includes xor encryption algorithm for data, ensures redundancy by storing the hidden data in various places of the provided text.

### Purpose
This tools helps people to hide their important text in a visible message. The secret data consists of special unicode characters that aren't visible on a screen. By appending the encoded data at the end of a message the secret can be transferred with no problem. The receiver can decode using same tools which scans for the special hidden text.

### Use
For the first tool:
Copy the sensitive text to the first textarea. Click `Encode` to encode the text with invisible unicode. The result will be inserted into the second textarea. Although it looks empty there's the entire text. Press `Ctrl+a` and `Ctrl+c` to copy it all. You can then add this hidden text at end of any message you want or text document.

If you receive some sort of special message containing encoded text , insert it into the seond textarea and click `Decode` to filter out the visible text and to see the hidden data.

For the second tool:
   The user must provide the algorithm with a simple text that will be used to camouflage the special secret data. The user can then copy the resulted text and send it. The secret data is placed in various places in the provided text to ensure a perfect recovery of the data.
   The user can also specify a password.
   An important aspect of the algorithm is that the result can be re-feeded to the system and by doing so, more messages can be encrypted and hidden.
