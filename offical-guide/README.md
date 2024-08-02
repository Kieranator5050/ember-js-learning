- Guide from the website - https://guides.emberjs.com/release/getting-started/
- Finished Guide Website Repo - https://github.com/ember-learn/super-rentals/tree/super-rentals-tutorial-output

# Notes
- The `application.hbs` template is the base template that runs for all routes.

## Routing
- Define routes in `router.js`. A route name maps to a template name.
- For providing links to routes use the ember component `<LinkTo/>` over `<a/>` tags.
- _model hook in a route file fetches and prepares the data into a model object that is returned

## Components
- `ember generate component {component-name} --with-component-class`

### Component Classes
- `ember generate component-class rental/image`
- Usually will use the @glimmer/component class but can see @ember/components class in older apps.

## Services
- Define with `@service serviceName` or to change its reference name `@service('serviceName') referencedName`

## Models / EmberData
- `ember generate model {model-name}` or create a test with `ember generate model-test {model-name}`
- In order to make the store service available we create the following: `app/services/store.js` and add `export { default } from 'ember-data/store';`
- When we have custom urls we need to specify a namespace in `app.js` and also update the request-manager in `app/services/request-manager`. 
  - The store service will also need to be updated with the new request manager.

## Testing
- Run the test server with ember t -s

### Acceptance Tests
- `ember generate acceptance-test {test-name}`
- These test the app from the user's perspective. 
- An automated way of just "clicking around and finding out"

### Component Tests
- `ember generate component-test {component-name}`
- Used to test single components.

### Mocking/Stubbing Services
- Check how this is done in share-button-test.js
- Use the `beforeEach` hook to register a mock service for each test