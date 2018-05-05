# HideText
Encodes visible text in invisble zero-width unicode characters. Append the secret data to a message and send it away. Decode it using same tool.
There are two tools provided(each stored in index.html and secure.html). The second one is more complex and allows for more messages to be sent through text, includes xor encryption algorithm for data, ensures redundancy by storing the hidden data in various places of the provided text.

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


## Technical:
   The unicodes that are being used are U200B and U200C. They are used to represent the binary version of the input chracters( need to change this:find more hidden unicodes to increase the storage per character space-currently 1 ASCII chr=8 UNICODES; need to use 7 bit ascii not 8bit.)
   In the second tool uses a small header to clasify and correct messages. The header has 3 ints: ID of message-a way of filtering out the other copies included in the text for redundancy- (1byte=8 unicode characters)  +  SIZE-of stored ascii data-  +  CHECKSUM.
   The encryption algorithm is XOR bsed.
   
## NOTES
There are some limits of the current code: The coverage text should not exceed ~300 characters, the secret data ~1000 characters. 
If the resulted text is refed into the code too many times the ability of the hidden data to be recovered even when the text is partially damaged will diminish.
The resulted text can become very large in size if the encoded data is too big.
