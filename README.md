cloned from payload. Some issues solved here. Can `run` or `build` on `docker` without any issues
## Development

To spin up the project locally, follow these steps:

1. First clone the repo
2. Then `cd YOUR_PROJECT_REPO && cp .env.example .env`
3. Next `yarn && yarn dev` (or `docker-compose up`, see [Docker](#docker))
4. Now `open http://localhost:3000/admin` to access the admin panel
5. Create your first admin user using the form on the page

That's it! Changes made in `./src` will be reflected in your app.

### Docker

Alternatively, you can use [Docker](https://www.docker.com) to spin up this project locally. To do so, follow these steps:

1. Follow [steps 1 and 2 from above](#development), the docker-compose file will automatically use the `.env` file in your project root
2. Next run `docker-compose up`
3. Follow [steps 4 and 5 from above](#development) to login and create your first admin user

That's it! The Docker instance will help you get up and running quickly while also standardizing the development environment across your teams.

## Production

To run Payload in production, you need to build and serve the Admin panel. To do so, follow these steps:

1. First invoke the `payload build` script by running `yarn build` or `npm run build` in your project root. This creates a `./build` directory with a production-ready admin bundle.
2. Then run `yarn serve` or `npm run serve` to run Node in production and serve Payload from the `./build` directory.

