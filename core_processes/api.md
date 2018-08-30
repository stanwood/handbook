# API

## Background

The decision for an API can have tremendous implications for the overall effort (and pain) of developing frontend. We have seen projects exploding 10x because of APIs we had no control over.

## Preferred solution: 100% control

### 1. Own API

When we have the need for a complex backend, our fearless backend team build a rock solid, high performance, super scalable, 100% unit tested and monitored thing of beauty on Google App Engine in Python.

### 2. Firebase

For smaller projects and prototypes that only need light weight auth, data or file storage we use firebase.

**Upsides**

- Do not need an backend developer to build things
- Real time database can function as a mock API (supports most HTTP methods including POST, PUT and DELETE)
- Changes can be monitored in real time
- Super easy integration
- Real time data base

**Downsides**

- Firebase has no build in server side logging and makes debugging a pain
- Changing data models is virtually impossible
- Data can be broken super fast - esp. on production
- Analytics on data structure is hard

## Third party APIs

Should clients force us to use a 3rd party API or one they are building, we always build a proxy.

The frontend developers then draft the API as they would need it. 

The proxy then translates between the frontend API and the 3rd party API.

**Upsides**

- Frontend development get's a highly optimized API
- We can monitor the 3rd party APIs for errors and report that directly to the client.
- We can hit cache and prevent outages even when the client APIs breaks.

## Monitoring

We use stackdriver to monitor for outages, errors and speed of the API itself and runscope as well as postman to mimic user requests to do a full end-to-end test of the API every few minutes.