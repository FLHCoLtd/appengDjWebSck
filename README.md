# Django/Channels/Redis on GAE and MemoryStore Redis

This sample code is following the tutorial on [Django-Channels](https://channels.readthedocs.io/en/stable/tutorial/index.html),
with additional GAE Flexible Env. configuration.

## Notice
+ [Why ASGI not WSGI?](https://asgi.readthedocs.io/en/latest/introduction.html#what-s-wrong-with-wsgi)
+ Support WebSocket by using [`daphne`](https://pypi.org/project/daphne/) instead of [`gunicorn`](https://pypi.org/project/gunicorn/)
+ [Use GAE Flexible Env. in order to support WebSocket persistant connection.](https://cloud.google.com/appengine/docs/flexible/python/using-websockets-and-session-affinity)
+ [GCP MemoryStore for Redis](https://cloud.google.com/memorystore/docs/redis/redis-overview) instance is accessible for GAE instance.
+ GCP `us-west` region is often lack of resource for GAE Flexible Env. to setup. (`groddkeeper` project)
+  Current python package version dependency is limited by `channel-redis`. (Django==3.2, channels==3.0.4, channels-redis==3.3.1)+  
