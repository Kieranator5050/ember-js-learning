- Guide from the website - https://guides.emberjs.com/release/getting-started/
- Finished Guide Website Repo - https://github.com/ember-learn/super-rentals/tree/super-rentals-tutorial-output

# Notes
- The `application.hbs` template is the base template that runs for all routes.

## Routing
- Define routes in `router.js`. A route name maps to a template name.
- For providing links to routes use the ember component `<LinkTo/>` over `<a/>` tags.

## Testing
- Run the test server with ember t -s

### Acceptance Tests
- `ember generate acceptance-test {test-name}`
- These test the app from the user's perspective. 
- An automated way of just "clicking around and finding out"

### Component Tests
- `ember generate component-test {component-name}`
- Used to test single components.