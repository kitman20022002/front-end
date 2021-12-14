# Coding Standarded

## Folder structure

- app 
	- model: ORM, database schema  
	- controller/api/v1/clients : 
	- middlware: such as authorztion 
	- database: as it says
	- loaders: such as express or logger stuff
	- tests: as it says
	- services: business logic
	- utils: as it says 
	- validation: as it says
	- config: configuation related setup
	- routes/v1 : as it says
	
## Restful standarded 

|Verb | Path | Action | Route Name |
|-----|------|--------|-------|
| GET |	/photo | index	| photo.index
| GET |	/photo/create | create | photo.create
| POST | /photo | store | photo.store
| GET | /photo/{photo} | show | photo.show
| GET |	/photo/{photo}/edit | edit | photo.edit
| PUT/PATCH	| /photo/{photo} | update | photo.update
| DELETE | /photo/{photo} | destroy | photo.destroy

### Respsonse 
- Who object for example user return the whole user object 

### Bad partices
- Just return the Id: cause error when we have many to many relationship, beacuse I need more than 1 id 

## Comon Status code
- 200: OK. The standard success code and default option.
- 201: Object created. Useful for the store actions.
- 204: No content. When an action was executed successfully, but there is no content to return.
- 206: Partial content. Useful when you have to return a paginated list of resources.
- 400: Bad request. The standard option for requests that fail to pass validation.
- 401: Unauthorized. The user needs to be authenticated.
- 403: Forbidden. The user is authenticated, but does not have the permissions to perform an action.
- 404: Not found. This will be returned automatically by Laravel when the resource is not found.
- 422: Unprocessable Entity
- 500: Internal server error. Ideally you're not going to be explicitly returning this, but if something unexpected breaks, this is what your user is going to receive.
- 503: Service unavailable. Pretty self explanatory, but also another code that is not going to be returned explicitly by the application.


## Reference

- https://laravel.com/docs/5.1/controllers

