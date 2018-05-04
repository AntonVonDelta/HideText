# HideText
Encodes visible text in invisble zero-width unicode characters. Append the secret data to a message and send it away. Decode it using same tool.


### Purpose
This tools helps people to hide their important text in a visible message. The secret data consists of special unicode characters that aren't visible on a screen. By appending the encoded data at the end of a message the secret can be transferred with no problem. The receiver can decode using same tools which scans for the special hidden text.

### Use
Copy the sensitive text to the first textarea. Click `Encode` to encode the text with invisible unicode. The result will be inserted into the second textarea. Although it looks empty there's the entire text. Press `Ctrl+a` and `Ctrl+c` to copy it all. You cand then add this hidden text at end of any message you want or text document.

If you receive some sort of special message containing encoded text , insert it into the seond textarea and click `Decode` to filter out the visible text and to see the hidden data.
