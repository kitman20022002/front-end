# Middleware

## PRIOR KNOWLEDGE

## Key points

- Middleware have access to request object, response object and the next function
- Middleware function can be perform the following tasks
  - Make changes to request to response object
  - End the Request-response lifecycle
  - Call the next middleware in the stack
- 5 Types of middleware (5 ways to use middleware)
  - Application-level
  - Router-level middleware
  - Error-handling middleware
  - Built in middleware
  - Third-parth middleware
- Examples are Auth,Logger

## Types (Differnet ways of using middleware)

### Application middleware

- app.use()

```
app.use(function (req, res, next) {
  console.log('Time:', Date.now())
  next()
})

```

### Router middlware

- router.use

- This code is executed for every request to the router

```
router.use(function (req, res, next) {
  console.log('Time:', Date.now())
  next()
})
```

- Only executed when you call /user/:id request

```
router.use('/user/:id', function (req, res, next) {
  console.log('Request URL:', req.originalUrl)
  next()
}, function (req, res, next) {
  console.log('Request Type:', req.method)
  next()
})
```

- Onions model ????
- Middleware order is important due to onions model
