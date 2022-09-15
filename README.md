# cyberhi API

### Example Usage

If you just need access to types:

```typescript
import type { User } from 'cyberhi-api';
```

If you want to send requests:

```typescript
import { API } from 'cyberhi-api';

// Initialise a new API client:
const client = new API();

// or with authentication:
const client = new API({ authentication: { cyberhi: 'bot-token' } });

// Make requests with ease:
client.get('/users/@me')
    // Fully typed responses!
    .then(user => user.username);

// No need to worry about the details:
let channel_id = "some channel id";
client.post(`/channels/${channel_id}/messages`, {
    // Parameters given are fully typed as well!
    content: "some content"
});
```
