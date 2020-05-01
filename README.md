# rpanchat 

This is a tiny, unofficial python module for streaming live comments from RPAN
(Reddit Public Access Network)

*Remember to always follow the Reddit API guidelines!*

### Example of usage:
```python
from rpanchat import RPANChat

chat = RPANChat(user_agent='Test app for private use (by u/redditusername)')
stream_id = input("Stream ID: ")
chat.connect(stream_id)
for comment in chat:
    print(comment.author + ': ' + comment.body)
```