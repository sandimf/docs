---
icon: laravel
description: By default, broadcasting is not enabled in new Laravel applications.
---

# Broadcasting

### Laravel Broadcasting

{% embed url="https://laravel.com/docs/11.x/broadcasting#introduction" %}

### Laravel reverb

{% embed url="https://laravel.com/docs/11.x/reverb#main-content" %}

### Installation <a href="#installation" id="installation"></a>

&#x20;You may enable broadcasting using the `install:broadcasting` Artisan command:

```bash
php artisan install:broadcasting
```

Behind the scenes, the `install:broadcasting` Artisan command will run the `reverb:install` command, which will install Reverb with a sensible set of default configuration options. If you would like to make any configuration changes, you may do so by updating Reverb's environment variables or by updating the `config/reverb.php` configuration file.



### Application Credentials <a href="#application-credentials" id="application-credentials"></a>

In order to establish a connection to Reverb, a set of Reverb "application" credentials must be exchanged between the client and server. These credentials are configured on the server and are used to verify the request from the client. You may define these credentials using the following environment variables:

```php
REVERB_APP_ID=my-app-id
REVERB_APP_KEY=my-app-key
REVERB_APP_SECRET=my-app-secret
```



### Setup

1. **Rename the file** from `echo.js` to `echo.ts`.
2. **Update the content of the `echo.ts` file** as follows:

```
import Echo from 'laravel-echo';

import Pusher from 'pusher-js';
window.Pusher = Pusher;

window.Echo = new Echo({
    broadcaster: 'reverb',
    key: import.meta.env.VITE_REVERB_APP_KEY,
    wsHost: import.meta.env.VITE_REVERB_HOST,
    wsPort: import.meta.env.VITE_REVERB_PORT ?? 80,
    wssPort: import.meta.env.VITE_REVERB_PORT ?? 443,
    forceTLS: (import.meta.env.VITE_REVERB_SCHEME ?? 'https') === 'https',
    enabledTransports: ['ws', 'wss'],
});

```

3. **After updating `echo.ts`**, import it in `app.tsx` like this:

```
import "./echo";
```

4. **After completing the setup**, run the following command to start the Laravel Reverb server:

```
php artisan reverb:start
```

This step will start the Reverb server to handle the WebSocket connections.
